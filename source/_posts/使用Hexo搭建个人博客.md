---
title: 使用Hexo搭建个人博客
abbrlink: 32e4259a
date: 2022-11-27 22:34:32
tags:
	- Hexo
	- 网站
categories: 网站
description: 使用Hexo和GitHub Pages搭建个人博客
cover: /files/life-song.jpg
---

这个网站是怎么做的？
当然是用HTML+CSS一个字母一个字母敲出来的。
详见文档[MDN Web开发教程](https://developer.mozilla.org/zh-CN/docs/Learn/Getting_started_with_the_web)

___

啊那怎么可能。
在有限的精力与能力下，当然要学会站在巨人的肩上。

> Hexo 是一个快速、简洁且高效的博客框架。Hexo 使用 Markdown（或其他渲染引擎）解析文章，在几秒内，即可利用靓丽的主题生成静态网页。
> <p align="right">——官网抄的</p>

[文档在这里](https://hexo.io/zh-cn/docs/)，通过阅读就可以了解一切你想知道的。

# 建立一个网站需要什么？
域名，服务器，一些必要的程序等。
GitHub Pages几乎将所有这些准备好了。

# GitHub Pages
[GitHub网站]("https://github.com")
[GitHub Pages文档，英文的]("https://pages.github.com")
只需要在GitHub上新建一个名为“__userneme__.github.io”（__username__ 为GitHub用户名）的仓库。添加HTML，CSS等文件，就可以在域名 __username__.github.io中打开你做的网站了。

# Hexo
需要的软件Node.js。
Windows下下载地址[Node.js](https://nodejs.org/zh-cn/download/)。
Linux用户自行解决。

## 初始化
任意位置打开命令行工具（比如Windows下win+r输入cmd回车打开cmd）。
执行以下命令安装Hexo
```bash
npm install hexo-cli -g
```
假设你的博客文件夹为folder，建立并初始化博客文件夹。
```bash
hexo init folder	# 建立博客文件夹
cd folder		# 进入文件夹
npm install		# 初始化
```

## 预览
将网页部署在本地
```bash
hexo g	# 生成静态页面
hexo s	# 启动服务
```
看到下面信息即部署成功
```plaintext
INFO  Hexo is running at http://localhost:4000 . Press Ctrl+C to stop.
```
浏览器打开[http://localhost:4000](http://localhost:4000)即可查看刚刚建立的网站

# 在Github Pages上部署Hexo
将文件夹上传到 __username__.github.io仓库。
剩下的下次再写吧。[文档](https://hexo.io/zh-cn/docs/github-pages)讲得挺详细的。
