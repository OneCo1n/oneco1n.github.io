### 利用hexo博客框架搭建个人博客
#### 一、前置步骤：首先安装Node.js（其中包括npm）   

1. 直接去官网下载安装https://nodejs.org/这个安装比较简单，选定安装位置，一直下一步就行。
打开终端，在终端进行下一步操作
Windows系统：
（1）运行cmd。
（2）node -v和npm -v命令可以查看Node.js是否安装好。
2. Mac OS：
（1）打开终端    
（2）切换到root用户    
（3）node -v和npm -v命令可以查看Node.js是否安装好。

#### 二、安装hexo：
**1. 利用npm安装cnpm**

>* 安装命令：`npm install -g cnpm --registry=https://registry.npm.taobao.org`，（registry设置镜像源，通过cnpm安装比较快，Windows和Mac命令一样）。   
>* 安装完成输入`cnpm -v`可以查看。
>
**2.安装hexo**
>* 输入命令：`cnpm install -g hexo-cli`，会自动安装hexo，安装结束可以输入hexo -v查看。
>* 创建一个文件夹mkdir blog（也可以叫其他名字），进入blog目录中
>* 输入命令生成hexo博客：`sudo hexo init` （Mac）   ` hexo init `（Windows）


**3.启动hexo博客**    
>* 命令：`hexo s`    会生成一个本地的连接，复制到浏览器就可以访问博客了。

#### 三、写博客步骤：

* `hexo n` "文章名" --生成一篇新文章。   
* 编辑文章   
* ` hexo clean`
* `hexo g` --生成文章

#### 四、将博客部署到GitHub上
* 登录GitHub新建一个仓库，仓库名字最好为：你的GitHub昵称.github.io（之后访问博客的连接地址）
* 打开命令行终端，安装git部署的插件，切换到之前建的blog目录下，输入命令：`cnpm install hexo-deployer-git`安装结束后，设置 **_config.yml**文件，在文件的最后![e1ac04484843585789c20274f09def24.png](en-resource://database/573:1)
* 添加type和仓库地址之后保存关闭。
![9b473a441a1c66a61cefa26ef258db26.png](en-resource://database/575:1)
* 修改完之后输入命令：`hexo d`部署到远端，然后输入GitHub帐号和密码，就成功了。

#### 修改博客主题
 **下载主题**
* `git clone` 主题链接.git 克隆到的文件夹
**配置主题**
* 修改_config.yml文件，找到theme，改为刚才下载主题的文件夹![194da9b2e5d91501de13521a61127220.png](en-resource://database/577:1)
* 之后清理`hexo clean`并重新生成`hexo g`、`hexo s`本地没问题推到GitHub hexo d

##### 参考链接：
[https://www.bilibili.com/video/BV1Yb411a7ty?from=search&amp;seid=11498560501175574686](https://www.bilibili.com/video/BV1Yb411a7ty?from=search&amp;seid=11498560501175574686)
