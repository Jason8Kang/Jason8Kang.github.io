---
layout: "post"
title: "install cntk"
date: "2016-11-15 12:09"
category: tool
tags: cntk
comments: true
keywords:
description:
---
# cntk安装
---

参考[官网](https://github.com/Microsoft/CNTK/wiki)

>官网安装说明如下：
You can install the complete source code of CNTK and build the binaries on your machine, but we also provide regular binary drops of the CNTK executables, including sample data and sample models.

也就是说建议初学者下载已经编译好的Binary版本直接上手实际操作。正所谓先上手了解，了解了之后再拆开看里面的机制。CSDN上有一系列文章的进而深入，带着大家从Github拉代码，手动编译，手动修改，自己实现对其扩展以及深入的探索里面的机制。如
[BorisJineman的专栏](http://blog.csdn.net/borisjineman/article/category/6094880)
- CNTK从入门到深入研究（1） - 一切都从介绍和环境搭建开始
- CNTK从入门到深入研究（2） - 研究CNTK配置文件
- CNTK从入门到深入研究（3） - Network Builders
- CNTK从入门到深入研究（4） - SGD随机梯度下降法
- CNTK从入门到深入研究（5） - Data Reader & Writer
- CNTK从入门到深入研究（6） - NDL简明教程
- CNTK从入门到深入研究（7） - 搭建CNTK开发环境
- CNTK从入门到深入研究（8） - CNTK工程结构（CNTK Core）
- CNTK从入门到深入研究（9） - CNTK工程结构（Extensibility&Reader)
- CNTK从入门到深入研究（10） - 为Python提供封装
- CNTK从入门到深入研究（11） - FAQ
- 如何导出CNTK网络节点训练结果？
- 通过CNTK处理自然语言模型

[zdy0_2004的专栏](http://www.cnblogs.com/sylvanas2012/p/5419264.html)

- 用 CNTK 搞深度学习 （一） 入门
- 用CNTK搞深度学习 （二） 训练基于RNN的自然语言模型 ( language model )

**注：本文选取最简单的[二进制安装](https://github.com/Microsoft/CNTK/wiki/CNTK-Binary-Download-and-Configuration)。**

>官网说明：
>###Download
>
>Download the required binary package from CNTK Releases page >and extract it to your machine.
>
>You will find installation instructions in the >Install-Windows.txt file in the root folder of the archive.
>
>For your convenience the same instructions are presented below >at this page.
>
>###Prerequisites
>
>Ensure that the following prerequisites are installed on your >system (you will find all required distribution packages, except >for NVIDIA drivers in the prerequisites folder of the archive; >you may also use the links below):
>
>Visual C++ Redistributable Package for Visual Studio 2013
>Visual C++ Redistributable Package for Visual Studio 2012
>Microsoft MPI of version 7 (7.0.12437.6). Note, that you need >run-time (file MSMpiSetup.exe) and not SDK. Also note, that CNTK >is currently tested with version 7 (7.0.12437.6). Using Version >7.1 may result in different compile and run-time errors
>For GPU systems ensure that you have the latest NVIDIA driver

###1.安装cntk包
从[CNTK Releases page](https://github.com/Microsoft/CNTK/releases)下载最新的cntk包，根据个人需要下载。
*注：下载的cntk包括

- Microsoft Computational Network Toolkit
- Microsoft 1-bit Stochastic Gradient Descent for the - Computational Network Toolkit
- NVIDIA CUDA Toolkit
- NVIDIA CUDA Deep Neural Network library (cuDNN)
- cuDNN License
- Open Source Computer Vision (OpenCV)
- zlib Library
- libzip Library
**由于cntk需要一些预安装环境**，即

- Visual C++ Redistributable Package for Visual Studio 2013
- Visual C++ Redistributable Package for Visual Studio 2012
- Microsoft MPI of version 7 (7.0.12437.6). Note, that you need run-time (file MSMpiSetup.exe) and not SDK. Also note, that CNTK is currently tested with version 7 (7.0.12437.6). Using Version - 7.1 may result in different compile and run-time errors
- For GPU systems ensure that you have the [latest NVIDIA driver](http://www.nvidia.com/drivers)
**注：在下载的cntk包的prerequisites里包括这些需要的工具前3个文件.**
本人由于尝试使用GPU，首先通过计算机管理中的图形显示器查看GPU型号为gefore 940m，从nvida官网下载相应的驱动。

###2.测试
添加环境变量以便使用，即path中增加cntk的路径。
在cmd界面切换路径方式为`D:`而不是`cd D:`，在D盘目录下可以`cd D:\cntk\Examples\Other\Simple2d`，最后`cntk configFile=Config/Simple.cntk currentDirectory=Data`
输出文档在路径`Simple2d/`
简单的配置
####CPU or GPU
修改cofig文件中的ConfigDir and ModelDir
To run on CPU set deviceId = -1, to run on GPU set deviceId to "auto" or a specific value >= 0.
####using a trained model
The Test (Simple_Demo_Test) and the Output (Simple_Demo_Output) commands specified in the config files use the trained model to compute labels for data specified in the SimpleDataTest.txt file. The Test command computes prediction error, cross entropy and perplexity for the test set and outputs them to the console. The Output command writes for each test instance the likelihood per label to a file outputPath = $OutputDir$/SimpleOutput. To use the Output command either set command=Simple_Demo_Output in the config file or add it to the command line. The model that is used to compute the labels in these commands is defined in the modelPath variable at the beginning of the file modelPath=$modelDir$/simple.dnn.
