---
title: proactor和reactor
date: 2019-06-27 10:33:58
tags:
---

reactor: 事件就绪，通知用户处理，用于同步IO(IO多路复用)
proactor: 用户交给内核一段内存buff，事件就绪数据会放到buff内，用户直接可读，用于异步IO

[proactor和reactor模型](https://www.jianshu.com/p/96c0b04941e2)
[IO设计模式：Reactor和Proactor对比](https://segmentfault.com/a/1190000002715832)he