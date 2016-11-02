### whaozl改进部分
1. 修改正文标题的尺寸问题
2. 文章写法模板详见位置 工具类别下的 markdown基本教程
3. 新增博客完美支持markdown下的latex公式 latex公式使用说明 工具类别下的 markdown完美支持latex
4. 在具体类别下的文章满屏时 出现滚动条 丑陋的问题 加入Perfect Scrollbar jquery插件
5. 字体更新为 微软雅黑
6. h1-h6标题 设置不同大小等级
7. h6 强制为图的标题 并设置格式为居中显示
8. 增加 博客的markdown 对 表格的 支持
9. markdown下 换行注意：**上下空1行** 或者  **段落后敲4个空格**
10. 博客头像下方 新增3个图标：github链接、博客园链接、新浪博客链接
11. 评论系统改为多说
12. 增加 不蒜子 为网站访问量统计工具
13. 增加 百度统计
14. 解决 pjax 异步刷新正文导致 网页访问量统计代码 失效问题 见base.js 最后js代码
15. 解决 pjax 异步刷新正文 没有正常渲染 latex公式问题 见base.js 最后js代码
16. 首页最新文章 只显示10篇
17. 在index.html中添加友情链接

##### blog书写注意
1. category和tag的命名不能相同，否则在tag标签中点击无响应，因他们的链接是相同的
2. book 和 love 里面 空格的空间个数要注意保持一致
3. 使用markdown 书写 博客 要经常性的 **敲空1行** 或者 **段落后4个空格**
4. latex公式 要注意 `转义的\alpha` 旁边要有空格 ，但是`$`的旁边不能有空格
5. \`输入的文字\`， \`旁边不能有空格

###jason修改部分
一个典型博客的基础目录结构：
>|-- _config.yml
|-- index.html
|-- _includes
|-- _layouts
|   |-- default.html
|   |-- post.html
|-- css
|-- js
|-- _posts
|   |-- 2015-04-27-Like-Kissing.md
|-- images
|   |-- Leah.png
|-- CNAME
|-- _404.html
|-- About.md
|-- feed.xml
|-- README.md

#####Description of The Catalog Document
目录文档详细说明。如下：

- _config.yml 博客配置文档（包括博客标题、favicon、博主 ID、头像、描述、联系方式等基本信息都在这个文档添加或修改）；
- index.html 博客架构文档；
- _includes 博客调用的网页模块（比如导航栏、底栏、博文内容显示、评论模块等），一般不需要管；
- _layouts 存放博客调用的页面模板文件（比如博客主页、具体博文页）的文件夹；
- css 存放博客系统的页面渲染文档文件夹，主要用于调节诸如标题字体、博文字体大小颜色之类；
- js 存放博客调用的 JS 文档文件夹
- _posts 博客正文存放的文件夹。命名有规定，必须为「日期 + 标题」的模式，即「2015-04-27-Like-Kissing.md」，才能发布到博客里；
- images 图片文件夹，存放博客相关素材，包括博客 favicon、博主头像等图片及博文贴图素材；（本文对图片处理参考[MPic-图床神器](https://suoyo.github.io/2016/08/29/Use-QiNiu/)和[七牛](https://portal.qiniu.com/)）
_七牛免费账户有10GB的存储空间，每月10GB的HTTP国内下载流量、10GB的HTTP海外下载流量、100万次GET请求和10万次PUT请求，一般用户足够使用了。_
- CNAME 用于绑定个人域名的文档；
- 404.html 「404 Not Found.」站点链接无法访问时的提示页面。
- About.html 博客中的个人说明文档（About Me），以 html、md 格式为主；
- feed.xml 博客的 RSS 订阅；
- README.md 项目说明文档。用于 Github 个人项目主页的说明（描述）。
- 除此之外，还有诸如 fonts 文件夹，存放博客用的字体文件，或有主题是将 css/js/fonts/images 等文件夹合并到 _assets 为名的主文件夹中。404.html/feed.xml/CNAME 文件并非必须，但一般架构完整的博客都有。

####Custom Configuration
自定义修改中，涉及到修改的文档包括：

_config.yml
About.html
CNAME
images

博客标题、博主 ID 一类都可以直接改。博客 favicon、博主 avatar 一类，还需要到 images 文件夹替换图片和配置文件的对应文件名。注意原图的尺寸，尽量与模板中的原图保持一致。

Notepad 用于打开 yml/THML 等文件并进行修改。Windows 用户就只有后者可选了…
damotou.com 在线制作（转换）用于 favicon（还不知道这是什么？瞧一下自己 Chrome 浏览器书签页左侧的小图标） 的 icon 图片，选择 32*32 像素的图片下载；
CNAME 文件，如果有独立域名请修改该文件；如果没有，则删掉该文件；

####如何写一篇博客
在文章最前面加上

---
layout: "post"
title: "test"
date: "2016-09-30 12:09"
category: tool
tags: markdown
comments: true
keywords:
description:
---

layout不用改；
title 一项是必须添加的；
categories 目录可以换，但如果不是要多重分类，这篇归档在 Blog 目录下；
Tags 可以自己按照文章主题添加，也可以不加，不同的 Tags 直接用英文逗号加半角空格间隔开；
description 博文概述，一句话概述，一般添加会好些。
