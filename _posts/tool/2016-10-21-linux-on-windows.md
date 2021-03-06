---
layout: post
title: "linux on windows"
date: "2016-10-21 12:09"
category: tool
tags: ubuntu
comments: true
keywords:
description:
---

# 如何在win10上运行linux(ubuntu14.0)?

> 控制面板>程序>启用或关闭windows功能>

![Paste_Image.png](http://upload-images.jianshu.io/upload_images/3078818-6462e4c69e5887be.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

在命令提示符或 *PowerShell* 中输入 *bash*，或者在开始菜单中查找打开*Bash on Ubuntu on Windows*，即可运行。
运行之后，可以发现使用的是 Ubuntu 14.04.4 LTS 版本，同时也可以使用 apt-get 更新或安装程序，如下图所示。此外。在 bash 当中，Windows 的分区被挂载于 **/mnt** 目录，可以使用其中存储的数据。

![Paste_Image.png](http://upload-images.jianshu.io/upload_images/3078818-df766db7dca6f4a8.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

## 命令参考

有两个命令 `bash.exe` 和 `lxrun.exe` 用于和 Windows Subsystem for Linux (WSL)进行交互。它们安装在 \Windows\System32 目录下，可以在命令行或 Powershell 中运行。

- bash.exe 启动 bash 环境并运行 /bin/bash
- lxrun.exe 用于管理 WSL，可以用来安装或卸载 Ubuntu 镜像

| 命令 | 描述 |
| :---- | :----- |
| bash	| 在当前目录启动 bash shell，如果 Bash 没有安装，这自动运行 lxrun /install |
| bash ~	| 启动 bash，并切换到用户的 Ubuntu 主目录，类似运行 cd ~ |
| bash -c  "command"	| 运行命令、打印输出并返回 Windows 命令行,例子： bash -c “ls”

```
df -h
lsb_release -a
uname -a
ls /mnt
```
运行结果如下：

![运行结果](/public/img/10/21/1.png)

还可以在两个系统内相互调用命令。

更多官网教程关注：
- https://msdn.microsoft.com/en-us/commandline/wsl/about
- how-to-geek中的教程：http://www.howtogeek.com/265900/everything-you-can-do-with-windows-10s-new-bash-shell/
