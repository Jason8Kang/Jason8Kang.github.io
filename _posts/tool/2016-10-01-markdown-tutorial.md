---
layout: "post"
title: "markdown tutorial"
date: "2016-10-01 12:09"
category: tool
tags: markdown
comments: true
keywords:
description:
---

# 1.标题

根据“#”设置标题级别，且*# 和「一级标题」之间建议保留一个字符的空格，这是最标准的 Markdown 写法。*

```
# 一级标题
## 二级标题
### 三级标题
#### 四级标题
##### 五级标题
###### 六级标题
```

# 一级标题

## 二级标题

### 三级标题

#### 四级标题

##### 五级标题

###### 六级标题


# 2.列表

【格式】：（*\\-\\+） + 空格 + 内容。

```
-  第一项
-  第二项
-  第三项
+  第一项
+  第二项
+  第三项
*  第一项
*  第二项
*  第三项
```

-  第一项
-  第二项
-  第三项
+  第一项
+  第二项
+  第三项
*  第一项
*  第二项
*  第三项

但如果希望有序

```
1. 文本1
2. 文本2
3. 文本3
```

1. 文本1
2. 文本2
3. 文本3

*注：-、1.和文本之间要保留一个字符的空格。*

# 3.插入链接和图片

插入链接不需要其他按钮，你只需要使用 
`
[显示文本](链接地址)。如[简书](http://www.jianshu.com)
`
[简书](http://www.jianshu.com)

添加图片的形式和链接相似，只需在链接的基础上前方加一个！
```
![我的头像.png](http://upload-images.jianshu.io/upload_images/3078818-45e2d9b3b07fbbf3.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
![](http://upload-images.jianshu.io/upload_images/3078818-17a8adc31d5a29ca.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
```

效果如下：

![埃菲尔铁塔](http://upload-images.jianshu.io/upload_images/3078818-45e2d9b3b07fbbf3.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![my—potrait](http://upload-images.jianshu.io/upload_images/3078818-17a8adc31d5a29ca.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

# 4.引用
在我们写作的时候经常需要引用他人的文字，只需要加上`>`

 ```
> 一盏灯， 一片昏黄； 一简书， 一杯淡茶。
```

> 一盏灯， 一片昏黄； 一简书， 一杯淡茶。

```
> 区块引用(区块在书写markdown时下方还要空1行) 
>> 嵌套引用
```

> 区块引用(区块在书写markdown时下方还要空1行) 
>> 嵌套引用

*注：需要和普通段落间存在空行，否则连续引用*

# 5.粗体和斜体
在强调内容两侧分别加上*或者_,，写法如下。
```
*斜体*，_斜体_ 

**粗体**，__粗体__

~~删除线~~
```

*一盏灯*， 一片昏黄；
**一简书**， 一杯淡茶。
~~删除线~~

# 6.代码引用
代码区块的建立是在每行加上**4个空格**或者**一个制表符**（如同写代码一样），最佳办法是写```，切记要和上一个普通段落之间**存在空行**。

    博客也有不错的流量，也没少参与CSDN举办的活动，获得了几本过时的技术书，但是仍感觉不爽，最痛苦的就是编辑，CSDN的在线编辑器做的不咋地，不太好用，而且经常写着写着就不动了，再刷新就啥都没了，

    需要引用代码时，如果引用的语句只有一段，不分行，可以用` 将语句包起来。如果引用的语句为多行，可以将```置于这段代码的首行和末行。

\`hello world\`

`hello world`

\``
abc
bcd
\``

``
abc
bcd
``

\```
a=1
print a
\```

```
a=1
print a
```
*注：反斜杠\相当于**反转义**作用。使符号成为普通符号*
# 7.表格
| Tables | Are | Cool |
| -------|:-------:| -----:|
| col 3 is | right-aligned | $1600 |
| col 2 is | centered | $12 |
| zebra stripes | are neat | $1 |
*注：实际上两个Tab键也是代码区块*

# 8.分割线
分割线
分割线仅需三个*或者三个_即可表示。
分割线1
***
分割线2
___  
以上是分割线

# 9反斜杠\
【格式】相当于**反转义**作用。使符号成为普通符号

# 10.公式

latex公式

$$ x=\frac{-b\pm\sqrt{b^2-4ac}}{2a} $$

Mathjax公式可以创建行内公式，例如：$\Gamma(n) = (n-1)!\quad\forall n\in\mathbb N$
或者块级公式，

$$ x = \dfrac{-b \pm \sqrt{b^2 - 4ac}}{2a} $$

# 11. 目录

[TOC]

###公式
#####分割线

# 12.流程图

  ```flow
st=>start: Start
e=>end: End
op1=>operation: My Operation
sub1=>subroutine: My Subroutine
cond=>condition: Yes or No?
io=>inputoutput: catch something...
st->op1->cond
cond(yes)->io->e
cond(no)->sub1(right)->op1
```

注意：
- 1. 关键词（start、end、operation、subroutine、condition和inputoutput）后的冒号后要紧跟一个空格。
- 2. 使用->来连接两个元素，对于condition类型，有yes和no两个分支，如示例中的cond(yes)和cond(no)。

更多关于流程图的语法说明：http://adrai.github.io/flowchart.js/
# 13. 时序图

```sequence
Alice->Bob: Hello Bob, how are you?
Note right of Bob: Bob thinks
Bob-->Alice: I am good thanks!
```

更多关于时序图的语法说明：[http://bramp.github.io/js-sequence-diagrams/](http://bramp.github.io/js-sequence-diagrams/)
 
##总结

 1. 最初只需要记住 # 标题一、## 标题二、1. 第一点、* 这一点，用这几个写写日志、需求文档、小文章，排版上足够了；
 2. 逐渐的你发现有些文字需要重点指出，那么还可以使用 **加粗**
、*斜体* 来对m文字做重点说明；
 3. 果你是名程序员，那么可以用 ``` 把代码块包起来，渲染后可以关键字高亮，用 > 可以做引用 ；
 4. 学生的话，就去了解一下 LaTex 吧，为知笔记 Markdown 支持 Mathjax 公式渲染哦~
