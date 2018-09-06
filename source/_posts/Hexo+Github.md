---
title: Hexo+Github搭建个人静态博客(MAC版)
date: 2018-09-05 20:02:49
categories: 
- web
---

  这篇文章主要是初次通过Hexo和GitHub建设个人静态博客的一些尝试和试验。建博客的动机是因为最近不小心把移动硬盘给整坏了，没有多余的备份，丢失了很多代码、数据以及工作记录，很是肉疼。
<!-- more -->

## 搭建流程

### 注册Github
新建repository，name：username.github.io

### 环境准备
安装Git，node以及Hexo,推荐用Homebrew进行安装，如果Homebrew安装出错，可以直接去[node官网](https://nodejs.org/en/)下载mac版安装包。

```bash
$ brew install git
$ brew install node
$ nmp install -g hexo
```

### 部署
```bash
$ git clone github.com/username/username.github.io #把仓库拉取到本地
$ git checkout -b hexo # 建立hexo分支，方便文件区分，发布博客与设置博客样式都在该分支下进行
$ hexo init
$ npm install hexo-deployer-git --save
$ hexo new "newpost"
$ hexo clean
$ hexo generate -d
```

