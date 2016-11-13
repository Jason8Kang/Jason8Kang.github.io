---
layout: "post"
title: "画出神经网络结构"
date: "2016-11-13 11:09"
category: tool
tags: visualize
comments: true
keywords:
description:
---

### 1.利用python

参考https://github.com/gwding/draw_convnet
只需两步，`git clone`和`python draw_convert.py`

![mark](http://ofqh7nchg.bkt.clouddn.com/blog/20161113/123219972.png)

有人还基于此进行改进：支持任意长宽比例的kernel和feature map，支持更深的网络结构：
https://github.com/HugoFeng/draw_convnet。
效果图：

![mark](http://ofqh7nchg.bkt.clouddn.com/blog/20161113/150016999.png)

### 2.利用graphviz

```
digraph G {

        rankdir=LR
	splines=line
        nodesep=.05;

        node [label=""];

        subgraph cluster_0 {
		color=white;
                node [style=solid,color=blue4, shape=circle];
		x1 x2 x3;
		label = "layer 1";
	}

	subgraph cluster_1 {
		color=white;
		node [style=solid,color=red2, shape=circle];
		a12 a22 a32 a42 a52;
		label = "layer 2";
	}

	subgraph cluster_2 {
		color=white;
		node [style=solid,color=red2, shape=circle];
		a13 a23 a33 a43 a53;
		label = "layer 3";
	}

	subgraph cluster_3 {
		color=white;
		node [style=solid,color=seagreen2, shape=circle];
		O1 O2 O3 O4;
		label="layer 4";
	}

        x1 -> a12
        x1 -> a22
        x1 -> a32
        x1 -> a42
        x1 -> a52

        x2 -> a12
        x2 -> a22
        x2 -> a32
        x2 -> a42
        x2 -> a52

        x3 -> a12
        x3 -> a22
        x3 -> a32
        x3 -> a42
        x3 -> a52

        a12 -> a13
        a22 -> a13
        a32 -> a13
        a42 -> a13
        a52 -> a13

        a12 -> a23
        a22 -> a23
        a32 -> a23
        a42 -> a23
        a52 -> a23

        a12 -> a33
        a22 -> a33
        a32 -> a33
        a42 -> a33
        a52 -> a33

        a12 -> a43
        a22 -> a43
        a32 -> a43
        a42 -> a43
        a52 -> a43

        a12 -> a53
        a22 -> a53
        a32 -> a53
        a42 -> a53
        a52 -> a53

        a13 -> O1
        a23 -> O1
        a33 -> O1
        a43 -> O1
        a53 -> O1

        a13 -> O2
        a23 -> O2
        a33 -> O2
        a43 -> O2
        a53 -> O2

        a13 -> O3
        a23 -> O3
        a33 -> O3
        a43 -> O3
        a53 -> O3

        a13 -> O4
        a23 -> O4
        a33 -> O4
        a43 -> O4
        a53 -> O4
}
```

效果图：

![mark](http://ofqh7nchg.bkt.clouddn.com/blog/20161113/123110753.png)

### 3.利用caffe，mxnet

### 4.利用ppt，visio工具

以下是贾扬清大神的回答：
>说真的，试一下powerpoint，很好使的。
如果你用Mac的话，keynote免费。
如果你能翻墙，Google docs也免费。
以上三个基本上是大众画图神器。记得导出成矢量PDF，然后就到处可以用了，包括pdflatex。
如果你想小众一点，GoogleNet那个图我是用pydot+graphviz画的，但是这些东西需要手调的地方多一些。
如果你要剑走偏锋一点，2010年的CVPR上Marc Aurelio Ranzato有一个全手绘的poster，想来当年参会的人都会有点印象吧。
