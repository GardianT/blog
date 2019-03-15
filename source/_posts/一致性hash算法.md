---
title: 一致性hash算法与负载均衡
date: 2019-03-14 20:41:33
tags: 
    - 一致性hash
    - 负载均衡
---

## 一致性hash

### consistent hashing

[consistent_hashing](https://github.com/apache/incubator-brpc/blob/master/docs/cn/consistent_hashing.md)

- 把所有server的处理区间视为一个环。比如[0, 1000)这样一个range，1000和0相连
- 每个server会扩充v倍形成虚拟节点，随机的插入到range内。如果有n个server，那就是vn个虚拟节点。
- 插入到range内是随机的；也就是说consistent hashing的虚拟节点 **并不保证就能均匀分割区间了。**。但是扩充的越大，区间就越可能趋近于均匀。比如[0, 1000)，如果你扩充出来1000个虚拟节点，那就一定均匀了。
但是扩充太多同样影响查找的性能。在brpc里这个数字是100，也就是每个server扩充100个虚拟节点。
- 查找比较简单，就是计算hash值，寻找虚拟节点vector的bound。如果bound到了边界，返回边界的节点（形成环）。
- hash算法（比如murmurhash）可以保证哪怕输入有规律的情况下，hash也是随机的。所以就可以保证请求散落全环。

### Rendezvous hashing

## 负载均衡

[locality-aware load balancing](https://github.com/apache/incubator-brpc/blob/master/docs/cn/lalb.md)
