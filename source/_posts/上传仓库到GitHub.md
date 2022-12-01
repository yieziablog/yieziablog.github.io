---
title: 上传仓库到GitHub
tags:
  - GitHub
  - Git
abbrlink: c4fb6f2f
date: 2022-11-27 21:20:16
description: 利用Git将本地文件上传到GitHub远程仓库
cover: /files/mirrors-starry.jpg
---

# GitHub和Git什么关系
GitHub是世界上最大的同x……不是，代码托管平台。顾名思义，就是个放代码的地方。Git是Linux祖师爷林纳斯开发的版本控制程序，GitHub用Git做版本控制。Git是软件，GitHub是平台。代码托管平台不止GitHub一个，依靠Git的平台也不止GitHub一个，而GitHub最有名。

# 在GitHub上创建远程仓库
打开[GitHub网站](https://github.com)
1. 注册Github账号
只需要一个可以接收验证码的邮箱，没有可以去申请一个outlook邮箱。打开GitHub网站，点击sign up按钮，剩下就按照提示来就行，不详细说了。
2. 创建新仓库
中间【Start a new repository】里的框中输入任意仓库名，选择Public，然后点击【Create a new repository】。仓库就创建好了。

# 将本地代码上传到GitHub仓库
## 安装Git
1. Linux用户
自行解决
2. Windows用户
建议在MSYS2中安装Git。MSYS2中科大镜像源[下载地址](https://mirrors.ustc.edu.cn/msys2/distrib/)。安装完成后在MSYS2中输入命令
```bash
pacman -Syu git # 更新所有软件包并安装git
```
并回车。完成之后执行命令
```bash
git --version
echo $? 	# 结果为0就说明运行成功
```
可以将MSYS2当作命令行工具，也可以将MSYS2 PATH加入系统PATH。使能够在PowerShell或cmd中运行Git。

## 开始上传
新建仓库后你就会发现页面上显示着一些代码

```bash
echo "# 仓库名" >> README.md 		# 创建README文件
git init 				# 初始化仓库
git add README.md 			# 添加README文件
git commit -m "first commit" 		# 提交改动
git branch -M main 			# 将主分支改名为main
git remote add origin <仓库地址> 	# 关联到远程仓库
git push -u origin main 		# 上传仓库
```

这不就是上传仓库的步骤么。根据这些步骤一步步来就行，中途可能需要输入用户名与邮箱。
上述代码的前四行就是创建并提交README文件的过程，如果想要提交其他文件，也需要add再commit。

## push入远程GitHub仓库
进行这个步骤时可能会提示输入用户名密码。用户名当然是Github用户名了，而密码其实是token，需要在Github上先创建。
话不多说，直接上步骤：
1. 点击头像->Settings->Developer Settings->Personal access tokens->Tokens(classic)->Gernerate new token。
2. Note随便填，下面全部勾选，点击Gernerate token就完成了。
3. 复制token并保存，就是push所需的密码。
