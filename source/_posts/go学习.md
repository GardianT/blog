---
title: go学习
date: 2019-03-14 09:57:29
tags: go
---

<iframe frameborder="no" border="0" marginwidth="0" marginheight="0" width=330 height=86 src="//music.163.com/outchain/player?type=2&id=427016661&auto=1&height=66"></iframe>

[深入解析go](https://tiancaiamao.gitbooks.io/go-internals/content/zh/)

[what are the differences between goroutines and bthreads](https://github.com/apache/incubator-brpc/issues/45)

- bthread的work steal是从其他runqueue的队尾偷取一个，go偷取一半
- go有一个全局的runqueue防止starvation