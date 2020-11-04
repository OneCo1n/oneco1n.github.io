---
title: Windows配置git环境——生成ssh公钥私钥
date: 2020-09-03 15:44:23
tags:
---
## Windows配置git环境生成ssh公钥私钥

1. 进入git bash，切换到用户目录cd ~
2. 第一条命令：`ssh-keygen -t rsa -b 4096 -C "your_email@.com"`，之后回车就行。
3. 第二条命令：`eval $(ssh-agent -s)`
4. 第三条命令：`ssh-add ~/.ssh/id_rsa`，之后`ls .ssh`就可以看到有文件目录了`id_rsa`(私钥)和`id_rsa.pub`(公钥)
5. 打开`id_rsa.pub`，复制文本内容，进入GitHub账户，进入setting，new ssh key选择SSH and GPG keys，粘贴到Key中，title可以标记一下。

###### 测试SSH链接

输入命令：`ssh -T git@github.com`

###### github使用ssh密钥的好处与原因
git使用https协议，每次pull, push都要输入密码，相当的烦。
使用git协议，然后使用ssh密钥。这样可以省去每次都输密码。

###### 参考链接

https://blog.csdn.net/love_fdu_llp/article/details/38752365
http://www.bilibili.com/video/BV1x7411F7HV
