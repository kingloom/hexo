---
title: 利用hexo搭建个人博客
date: 2016-11-29 01:01:19
tags: [hexo,blog]
---

## 前言

很多有Geek范儿的朋友都希望能够搭建一个自己的网站，根据自己的想法，打造成自己想要的样子。Hexo无疑是其中最方便快捷的一个工具。
不知道Hexo是什么？不要紧，唐三藏也是上路之后才遇上孙猴子的。这里你只要直到Hexo能帮助我们已最快捷的方式搭建一个个人博客就够了，其余的，等我们一步步实现，自然就明白了。

<!--more-->

***本人使用的系统版本是Ubuntu14.04，以下内容均基于此版本。***

## 所需工具

- [Node.js](http://nodejs.org/)
- [Git](http://git-scm.com/)


## 安装工具

### 安装Git

- Windows: 下载并安装[git](https://git-scm.com/download/win)
- Linux(Ubuntu, Debian): `sudo apt-get install git-core`
- Linux(Fedora, Red Hat, CentOS): `sudo yum install git-core`

### 安装Node.js

1. 通过命令行安装
官方给的安装方式如下：

```bash
$ curl -sL https://deb.nodesource.com/setup_6.x | sudo -E bash -
$ sudo apt-get install -y nodejs
```

2. 下载Node.js源码包，手动编译安装：

- 下载地址：[https://nodejs.org/dist/v6.9.1/node-v6.9.1.tar.gz](https://nodejs.org/dist/v6.9.1/node-v6.9.1.tar.gz)

```bash
$ tar -xvzf node-v6.9.1.tar.gz
$ cd node-v6.9.1
$ ./configure
$ make
$ sudo make install
```
## 部署Hexo

使用npm安装Hexo

```bash
$ npm install -g hexo-cli
```

到此为止，Hexo我们算是安装完成了，接下来就是利用Hexo搭建我们的个人博客了。

## 搭建博客

新建一个目录，用来存放博客，如：`/root/blog/`，以后的操作都是在这个目录中进行。

```bash
$ mkdir /root/blog
$ cd /root/blog/
```

执行`hexo init`操作，将会在当前目录生成个人博客的架构，目录，配置文件等。

```bash
$ hexo init
$ ls
_config.yml  node_modules  package.json  scaffolds  source  themes
```

简单说下这些文件目录的作用

- _config.yml ： 全局配置文件，部署完后需要修改下这里面的配置。
- package.json：数据库保存在这个里面。
- source: md格式的源文件都在这里面。
- public: 这个文件夹还没有生成，网页都在这里面。
- themes：博客的主题保存路径，每个文件夹一个主题。

至此，我们的博客就搭建完毕了。对，就这么简单。
那如何通过浏览器查看我的博客呢？我们首先通过`hexo server`命令启动博客。

```bash
$ hexo server
INFO  Start processing
INFO  Hexo is running at http://localhost:4000/. Press Ctrl+C to stop.
```

在浏览器输入链接：`http://localhost:4000/`，即可访问我们刚才搭建的博客了。
