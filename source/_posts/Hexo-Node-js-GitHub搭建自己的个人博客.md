---
title: Hexo+Node.js+GitHub搭建自己的个人博客
date: 2017-08-11 16:18:17
tags:
---
# 1. 前言
作为一名技术人员，很早之前就想搭建一个自己的个人博客了，但是由于种种原因一直搁置着，最近终于闲了下来，有时间去慢慢折腾了。拥有自己的个人博客是有很多好处的，包括：
* 总结自己的学习和成长
* 记录自己对于各种技术的收获
* 共享知识，方便其他人学习
* 包装自己，展示自我
* 练习文笔
* ...

还有很多的好处就不一一描述了，相信大家都有各种各样的动力去做一个博客。相对于早期的博客开发来说，现在搭建自己的个人博客是一件相对容易的事情，很多的框架和技术都已经把复杂的流程和操作封装起来，准备好环境之后只需要几条命令行即可完成本地博客的搭建。新博文的发布和编辑也是很好上手的。

选择一个自己喜欢的主题风格即可让自己的博客看起来有模有样的了，以下是搭建博客的准备工作。

# 2. 搭建环境准备
- Node.js的安装和准备
- Git的安装和准备
- GitHub账号的配置和仓库的新建
## 2.1 下载Node.js的安装文件
Node.js下载链接：
* [Windows Installer 32-bit](https://nodejs.org/dist/v4.2.3/node-v4.2.3-x86.msi "Node.js 32-bit") 
* [Windows Installer 64-bit](https://nodejs.org/dist/v4.2.3/node-v4.2.3-x64.msi "Node.js 32-bit") 

大家可以根据自己的windows版本下载安装相应的文件。

![](https://raw.githubusercontent.com/winnerchen/hexo/master/source/images/blog_4.png)
下载完毕之后，一路按next即可完成安装。

然后我们检查一下组件是否安装完毕，按下Win+R输入CMD打开命令行窗口。
![](https://raw.githubusercontent.com/winnerchen/hexo/master/source/images/blog_1.png) 
![](https://raw.githubusercontent.com/winnerchen/hexo/master/source/images/blog_2.png) 
在打开的命令行窗口中输入

```
node -v
npm -v
```
如果显示如下图，则表示安装正确，可以进行下一步安装。
![](https://raw.githubusercontent.com/winnerchen/hexo/master/source/images/blog_3.png) 

## 2.2 配置Git环境
下载[Git安装文件](https://git-scm.com/downloads "Git下载")

下载完成之后直接安装即可，安装过程无需解释了，next到结束即可。

安装完毕之后用命令来检查Git是否已经正确安装:
```
git --version
```
如果结果如下图所示，则说明安装正确，进入下一步安装。
![](https://raw.githubusercontent.com/winnerchen/hexo/master/source/images/blog_5.png) 

## 2.3 GitHub账号的注册和配置
### 2.3.1 GitHub账号的注册
前往[GitHub注册页面](https://github.com/)注册自己的个人账户
### 2.3.2 GitHub仓库的创建和配置
如下图所示，点击Your Profile - Repositories - New来创建新仓库
![](https://raw.githubusercontent.com/winnerchen/hexo/master/source/images/blog_7.png)
![](https://raw.githubusercontent.com/winnerchen/hexo/master/source/images/blog_6.png)



