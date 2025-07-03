---
layout: single
title: "五分钟搞定Java的环境配置"
date: 2025-06-24 10:00:00 +0800
author: default
categories: [教程, Jekyll]
tags: [目录, markdown, 博客]
toc: true          # ✅ 开启目录
toc_sticky: true   # ✅ 目录固定在侧边栏
toc_label: "目录"  # ✅ 可自定义标题，如 Table of Contents
toc_icon: "list-ul"
comments: true     # ✅ 如果你开启了评论系统
read_time: true    #显示时间
header:
  teaser: /assets/img/logo.png    
---

>**五分钟带你搞定Java+SpringBoot+IDEA+SpringBoot的环境配置**

---

## 一、什么是Java？
Java是一种**跨平台的，面向对象的编程语言**，由Sun Microsystems（现为Oracle）于1995年发布  

他的特点是
-- **一次编写，到处运行**：得益于JVM(Java虚拟机)，Java的程序可以在任何的操作系统上运行
-- **丰富的生态**：广泛运用于企业开发，安卓开发，大数据等领域

## 二、如何配置Java环境？

### 1.下载JDK

[官方网站](https://jdk.java.net/24/)

[清华大学镜像站](https://mirrors.tuna.tsinghua.edu.cn/Adoptium/21/jdk/x64/windows/)

[华为云镜像](https://mirrors.tuna.tsinghua.edu.cn/Adoptium/21/jdk/x64/windows/)

下载下来之后一路确认即可

### 2.配置全局环境变量

安装完成后，会默认安装到C盘的`C:\Program Files\Java\jdk1.8.0_211`

接下来点击我的电脑-属性-高级系统设置-选择环境变量

![](/assets/img/1751522870742.png)

进来应该是这样子的，我们点击新建

![](/assets/img/1751522959339.png)

点击新建之后页面应该是这样的，我们随便命名一个名称，然后找到刚刚下载JDK的路径

在这里我命名的名称为Java_Home

![](/assets/img/1751523205409.png)

创建成功之后，我们还需要添加`Path`的配置，找到`Path`点击编辑,在Page里面新建环境变量

![](/assets/img/1751523671714.jpg)

变量1:%Java_Home%\bin

变量2:%Java_Home%\jre\bin

下面这个变量1和2要看自己的变量名称，我这里是Java_Home

新建完成后给这两个上移到顶部

![](/assets/img/1751523840087.png)

现在再配置CLASSPATH

返回前面，点击新建

![](/assets/img/1751524105059.png)

添加配置

变量名：`CLASSPATH`
变量值：`.;%JAVA_HOME%\lib\dt.jar;%JAVA_HOME%\lib\tools.jar;`

![](/assets/img/1751524196105.png)

点击确定

现在我们来验证是否配置成功

### 3.验证环境

按键盘上的`Win + R` 两个一起按，再输入`Enter` 回车

输入`java -version`看看有没有显示版本

输入`javac -version`看看有没有显示版本


如果都有显示代表我们第一步Java的环境配置成功了