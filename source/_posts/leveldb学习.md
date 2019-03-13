---
title: levelDB学习
date: 2019-03-13 13:23:29
tags: levelDB
---

<iframe frameborder="no" border="0" marginwidth="0" marginheight="0" width=330 height=86 src="//music.163.com/outchain/player?type=2&id=28576476&auto=1&height=66"></iframe>

[浅析bigtable和leveldb的实现](https://draveness.me/bigtable-leveldb)

写的特别好的一篇文章。几乎所有都讲的很清楚了。不过文中有一些levelDB相关的知识没提到

- levelDB有个很重要的特性是全局有序，在memtable中使用了skip list的数据结构。该数据结构在redis中也有应用
- 如何快速判断一个key是否在sstable中存在，levelDB使用了bloomfilter这个方法。

所以可以结合下面的文章得到这些信息：

[levelDB实现分析](http://taobaofed.org/blog/2017/07/05/leveldb-analysis/)
[levelDB中的sstable](http://bean-li.github.io/leveldb-sstable-bloom-filter/)

levelDB就是bigtable中单机kv存储引擎。影响深远。当前社区使用的更广泛的是RocksDB，其实我会理解为是优化版本的levelDB。可以额外关注一下RocksDB对事务的支持。

[TransactionDB的介绍](https://zhuanlan.zhihu.com/p/39427559)

底层单机 + 实现上层的tabletServer等，就可以得到分布式的，全局有序的bigtable了。比如百度搜索主要使用的是[tera](https://github.com/baidu/tera/blob/master/doc/newcomer/tera_intro.md)。  
还有比较知名的如[TiDB](https://pingcap.com/blog-cn/tidb-internal-1/)，也在使用类似的单机kv引擎。