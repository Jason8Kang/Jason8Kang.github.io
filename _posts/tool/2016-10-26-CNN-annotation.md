---
layout: "CNN annotation"
date: "2016-10-26 12:09"
category: tool
tags: CNN
comments: true
keywords:
description:
---

这篇小文章并没有限定什么范围，只要是深度学习相关的就行。这反倒让人烦恼，就和人生一样，选择太多了也是一种烦恼。因为最近工作有空之余正在学习**斯坦福的课程CS231N，Convolutional Neural Networks for Visual Recognition**。这个课程非常好，除了详尽的slides和notes，最值得一提的就是它的作业。每个作业包含完整的模型，比如CNN、LSTM，所有的模型的代码都只是用最简单的python代码实现，而不是用现成的库比如TensorFlow/Theano/Caffe。纸上得来终觉浅，绝知此事要躬行。很多理论，光听课看slides，似乎觉得自己懂了，其实还是一知半解，真正要掌握，就得自己动手，最好是全部自己实现。但是全部自己实现需要花的时间太多，而且从实际工作的角度来说，大部分开发者肯定都是用TensorFlow这样的工具。而这个课程的好处就是：把一些琐碎的与核心代码不相关的部分包括学习的框架都已经实现了，然后用IPython notebook把关键的代码的函数的输入和输出都描述的非常清楚，学习者只需要实现一个一个这样的函数就行了，而且每个函数都会有类似单元测试的检测代码正确性的数据，从而保证我们的每一步都是在朝着正确的方向前进。

因此这篇小文章打算讲一讲其中的Assignment3的Image Caption Generation部分。目的是想通过一个具体的任务来给大家介绍深度学习的一些知识，让大家对深度学习有一些概念和兴趣。选择Image Caption Generation的原因，一来这个任务挺有意思的；第二就是它涉及到很多深度学习流行的模型如CNN，RNN/LSTM，Attention。
首先来介绍一下什么叫做Image Caption Generation。

对于计算机视觉相关的任务，图片分类和定位大家可能比较熟悉。图片分类就是给定一张图片，让计算机告诉我们它是一只猫还是一只狗；而图片定位除了告诉我们这是一张狗的图片，还需要用用一个矩形框把狗的位置标识出来。当然还有要求更高的Image Segmentation，需要告诉我们哪一些像素属于狗，而另外一些属于背景。

图1就是这些任务的例子：
![](\public\img\10\25\1.png)
