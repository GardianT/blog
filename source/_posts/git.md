---
title: git
date: 2019-03-13 15:23:04
tags: git
---

<iframe frameborder="no" marginwidth="0" marginheight="0" width=330 height=86 src="//music.163.com/outchain/player?type=2&id=22743825&auto=1&height=66"></iframe>

## git 切换账号后 push出错

现象是配置过`git config --global user.name`等信息，但是更改过。  
push的时候显示denied，账户仍显示原来的账户。但是git log看committer已经是新账户的提交了。

操作：

- 如果存在 `~/.git-credential` 这个文件的话，删掉。
- 在mac上，删掉钥匙串保存的github信息。或者更改也可以。

https://stackoverflow.com/questions/21615431/git-pushes-with-wrong-user-from-terminal