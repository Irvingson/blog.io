---
layout: post
title: how to build a blog
date: 2017-10-22
categories: blog
tags: [总结、知识管理]
description: 我还真是可爱呢
---

# 听说网络组有个作业，叫做在github上写一下我搭建博客的流程

### 我就很为难

### 为什么呢

### 因为我也是像个傻*一样跟着教程一步一步来的啊

### 说得好像我自己就能建一个blog一样的

### 我也很绝望的呀

[首先的首先来贴一下我看的教程（反正你们也有哼）](http://www.cnfeat.com/blog/2014/05/10/how-to-build-a-blog/)

然后就来回忆一下我之前到底怎么整的，哇我真的不记得了啊

## 那么进入正题

[首先是在Godaddy上买一个域名，有钱人可以尝试](https://sg.godaddy.com/zh?cvosrc=ppc.baidu.Title&matchtype=Exact&mkwid=OdF1WcMU_pkw_Title_pmt_Exact_)

反正我是没有买嘻嘻，毕竟人穷 有钱人可以接济我一下，请我吃饭就行了

在经过一番短暂的预算计算之后，决定不买域名的我就进入了下一个环节

### 安装准备软件

- [Node.js](https://nodejs.org/en/)
- [git](https://git-scm.com/)

其实雨田学姐群里有发，反正我不是在这两个网站上下的

然后就是打开Git，这里只发Windows系统的（说得好像我买得起Mac一样）
![](http://upload-images.jianshu.io/upload_images/8613291-1b5bf91e392eb334.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
之后按照他给的指示，把该勾的选项勾了，坐等装完就行了
但是听了学长讲的课之后感觉好像这个玩意儿没啥用

## [之后注册一下你的GitHub](http://www.GitHub.com/)
相信凭借你高超的智商这点问题一定可以轻松解决的！

## 然后是配置SSH keys
### 检查SSH keys的设置
`$ cd ~/.ssh 检查本机的ssh密钥`
用的就是你之前下的那个 Git Bash
###生成新的SSH keys

![大概就是长这样的界面](http://upload-images.jianshu.io/upload_images/8613291-054ca08868827b86.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

然后系统会要求你输入密码
```
Enter passphrase (empty for no passphrase):<输入加密串>
Enter same passphrase again:<再次输入加密串>
```
最后你看到这个反正你也看不懂的东西就成功了科科

![我还真是可爱呢](http://upload-images.jianshu.io/upload_images/8613291-7349657c3c05ef47.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

##然后就是添加SSH keys 到github
在本机设置 SSH Key 之后，需要添加到 GitHub上，以完成 SSH 链接的设置。
- 1、打开本地 id_rsa.pub 文件（ 参考地址 C:\Documents and Settings\Administrator.ssh\id_rsa.pub）。此文件里面内容为刚才生成的密钥。如果看不到这个文件，你需要设置显示隐藏文件。准确的复制这个文件的内容，才能保证设置的成功。
- 2、登陆 GitHub 系统。点击右上角的 Account Settings—>SSH Public keys —> add another public keys
- 3、把你本地生成的密钥复制到里面（ key 文本框中）， 点击 add key 就ok了
![这个就是成果图 假装这就是我自己的](http://upload-images.jianshu.io/upload_images/8613291-8cdb8b47408b9491.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


输入下面这个指令可以测试一下你有没有设置成功
`$ ssh -T git@GitHub.com`
如果你看到了这个
`The authenticity of host 'GitHub.com (207.97.227.239)' can't be established. RSA key fingerprint is 16:27:ac:a5:76:28:2d:36:63:1b:56:4d:eb:df:a6:48. Are you sure you want to continue connecting (yes/no)? `

不要紧张，输入 yes 就好，然后会看到：
`Hi xxx! You've successfully authenticated, but GitHub does not provide shell access.`

那么就恭喜你成功了呢嘻嘻

现在你已经可以通过 SSH 链接到 GitHub 了，还有一些个人信息需要完善的。

Git 会根据用户的名字和邮箱来记录提交。GitHub 也是用这些信息来做权限的处理，输入下面的代码进行个人信息的设置，把名称和邮箱替换成你自己的，名字必须是你的真名，而不是GitHub的昵称。

## 修改个人信息
```
$ git config --global user.name "cnfeat"//用户名
$ git config --global user.email  "cnfeat@gmail.com"//*填写自己的邮箱*
```

## Fork别人的仓库 然后你可以很臭不要脸的删掉他发的东西嘿嘿

![点上面这个settings](http://upload-images.jianshu.io/upload_images/8613291-a81c8f910ec76173.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


![就改红圈这个名字](http://upload-images.jianshu.io/upload_images/8613291-579589e94786728d.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)




然后你到浏览器里面搜一下你的仓库的名字 就比如xxx.github.io看看能不能搜得到

这个也是看脸的 欧洲人可能就一下子出来了一个页面，比如我
![](http://upload-images.jianshu.io/upload_images/8613291-730ccdc3949b9e77.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
非洲人那可能就要等个一两天的嘻嘻
玄不改非，氪不改命哦
 ![](http://upload-images.jianshu.io/upload_images/8613291-c63e38b16ffa8f52.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


> 刘帅这个人天真可爱活泼聪明机智可爱积极向上人见人爱花见花开
                                                                                        ——沃·兹基硕德
