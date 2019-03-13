---
title: hello world
---

<iframe frameborder="no" marginwidth="0" marginheight="0" width=330 height=86 src="//music.163.com/outchain/player?type=2&id=1293036&auto=1&height=66"></iframe>

在互联网没有普及的时候，人们获取知识的主要途径是书籍；互联网普及之后，人们开始在网上获取信息。
然而书分有好有坏，信息分有价值无价值。网络上的能获取的信息无穷无尽，无价值的信息却也更多。尤其做搜索相关，对这点更有感触。  
在网上搜东西会经常感触，需要很久才能找到真正有价值的信息，然后存到书签，日后回顾。后来想着搭个个人小站，用于记录这些对学习有帮助的信息。  
互联网进入快餐时代，搭建网站，app，都已经有成型的模板，极低的成本就可以快速原型。想想上学的时候还会练习用vue手写博客网站。而现在懒得只想用模板去做这种事情。

## 快速开始

### 选用模板：hexo

[hexo](https://hexo.io/zh-cn/docs/index.html)

文档比较全，几分钟就足够上手。其实可以直接把hexo理解为一个cli，写过node的话应该不会陌生这种东西。

### 选用主题：Material-T

[themes](https://hexo.io/themes/)

学习模板3分钟，选个主题3小时-。-  
按自己喜好选一个主题。自己做一个也比较容易，themes其实就是html，css，js的集合。hexo使用的模板是ejs，也是比较常见的模板。   
不过选主题还是推荐下载下来，看一眼。有一些主题已经失效，有一些主题不是很容易改。选一个比较好看自己不用太折腾的主题可能会多花一些时间。

配置好模板和主题后，可以运行`hexo server`观察下效果。


### 发布

可以直接借助github发布网站。首先配置个空repo [github pages](https://pages.github.com)，不用choose theme，repo成功建立且配置了site就可以了。后续可以

- 直接用hexo的命令发布上去[hexo deploy](https://hexo.io/zh-cn/docs/deployment.html)

然后在浏览器中访问你配置的那个site就可以访问到你的网站了
