---
layout: "post"
title: "markdown to pdf"
date: "2016-11-11 11:09"
category: tool
tags: markdown2pdf
comments: true
keywords:
description:
---

## 1. Atom编写md文档并转为pdf（转自[here](http://www.joomla178.com/joomla-share/front-end/649-edit-md-files-by-atom-transfer-to-pdf.html)）

#### 安装插件

> 根据我们实际需要，仅需安装md转pdf的插件（`markdown-themeable-pdf`）即可，
Atom的插件是可以使用`apm`命令来进行在线安装，实际因为一些原因，我们只能使用`npm`进行安装，所以我们需要先安装`nodejs`

### 安装NodeJS

前往`NodeJS`官网下载：[https://nodejs.org/en/
](https://nodejs.org/en/)

安装完成之后也是因为一些原因，需要将`npm`源改为国内淘宝源，方法如下：

```
npm config set registry http://registry.npm.taobao.org/
```

### 安装md转pdf的插件

前往GitHub下载该插件的压缩包：[https://github.com/cakebake/markdown-themeable-pdf
](https://github.com/cakebake/markdown-themeable-pdf)

将压缩包解压至目录`C:\Users\yourname\.atom\`

用管理员方式打开`Windows`的命令行提示符，进入插件目录

```
cd C:\Users\yourname\.atom\packages\markdown-themeable-pdf-master
```

输入`npm install`，等待安装完成，用`Atom`打开`md`文档，右击文档任意处，选择Markdown to PDF，等待片刻完成转换，如下图：

![markdown to pdf](http://www.joomla178.com/images/multithumb_thumbs/3498346a5a3a541ca192560e51b3bdf5.png)

更多问题关注[官网](：https://github.com/cakebake/markdown-themeable-pdf)

## 2. 为知笔记插件---笔记导出为pdf插件
下载地址：http://app.wiz.cn/
其他格式的导入导出可以具体做法可以参考：http://test.smzdm.com/pingce/p/1850/
安装插件后，找到右上角的设置三角按钮，点击`设置>文件>制作pdf`

![mark](http://ofqh7nchg.bkt.clouddn.com/blog/20161101/225221695.png)

## 3. 利用chrome浏览器

首先安装插件 `markdown preview`使chrome浏览器可以预览markdown效果，然后点打印，目标，选本地另存为pdf即可。看图：
![mark](http://ofqh7nchg.bkt.clouddn.com/blog/20161101/225826996.png)
这样保存的PDF非常完美，基本上你在chrome里预览是什么格式，保存完就是什么格式。

总体来说，更推荐方法2，因为方法1可能会有中文问题，方法3可能会因为pdf自带的格式的影响，但是多实践才知道。
