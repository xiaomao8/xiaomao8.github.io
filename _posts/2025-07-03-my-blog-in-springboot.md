---
layout: single
title: "一站式SpringBoot环境配置指南（JDK+Gradle+IDEA）"
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

>**半个小时带你搞定Java + SpringBoot + IDEA + Gradle的环境配置**

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

安装完成后，会默认安装到C盘的`C:\Program Files\Java\jdk-23`

接下来点击我的电脑-属性-高级系统设置-选择环境变量

![](/assets/img/1751522870742.png)

进来应该是这样子的，我们点击新建

![](/assets/img/1751522959339.png)

点击新建之后页面应该是这样的，我们随便命名一个名称，然后找到刚刚下载JDK的路径

在这里我命名的名称为`Java_Home`

![](/assets/img/1751523205409.png)

创建成功之后，我们还需要添加`Path`的配置，找到`Path`点击编辑,在`Path`里面新建环境变量

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

输入`java -version`看看有没有显示JRE的版本

输入`javac -version`看看有没有显示JDK的版本

然后我们接下来需要安装Java23

[官方网站](https://www.oracle.com/java/technologies/javase/jdk23-archive-downloads.html)

下载完成之后一路下一步就可以了

如果都有显示代表我们第一步Java的环境配置成功了

### 三、如何配置Gradle

我们首先下载IDEA

[官方网站](https://www.jetbrains.com/idea/)

下载完成之后一路继续即可

安装完成之后，我们现在开始下载Gradle

>**注意，IDEA和他的JB全家桶是需要付费的开发工具，新用户可免费享受三十天，三十天一到就需要付费**



我们现在来创捷一个SpringBoot项目

![](/assets/img/1751537886304.png)

选择SpringBoot,JDK选择我们刚刚下载的23,因为现在SpringBoot并不支持24及以上的版本

Java我们选择23，然后开始构建项目，构建过程中他会自己下载

进入这个页面之后我们选择JDBC API,我们目前是先构建一个示例项目，所以暂时不选其他的

![](/assets/img/1751538130735.png)

这里他自动下载会很慢，我们可以选择进入他[官方网站](https://services.gradle.org/distributions/)下载

或者是使用复制网址放到迅雷里面下载

 https://services.gradle.org/distributions/gradle-8.14.2-bin.zip

下载完成之后放入这个文件夹里面

`C:\Users\123\.gradle\wrapper\dists\gradle-8.14.2-bin\2pb3mgt1p815evrl3weanttgr`

就是c盘，你的用户文件夹里面,这个一片乱码可能不一样，但是大概的路径就是这样

接下来重启IDEA,然后等待一会

![](/assets/img/61b1d43c0672fb078af99e73ba4267e.png)

下面显示已完成而且上面绿了就代表我们已经配置成功了

