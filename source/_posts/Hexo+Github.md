---
title: Hexo+Github搭建个人静态博客(MAC版)
date: 2018-09-05 20:02:49
categories: 
- web
---
本文主要用于测试静态博客的搭建方式以及设置。
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
$ git clone github.com/username/username.github.io
$ git checkout -b hexo
$ hexo init
$ npm install hexo-deployer-git --save
$ hexo new "newpost"
$ hexo clean
$ hexo generate -d
```

