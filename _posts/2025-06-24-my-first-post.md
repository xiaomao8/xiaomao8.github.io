---
layout: single
title: "讲讲我建这个个人博客的过程"
date: 2025-06-24 10:00:00 +0800
author: default
categories: [教程, Jekyll]
tags: [目录, markdown, 博客]
toc: true          # ✅ 开启目录
toc_sticky: true   # ✅ 目录固定在侧边栏
toc_label: "目录"  # ✅ 可自定义标题，如 Table of Contents
toc_icon: "list-ul"
comments: true     # ✅ 如果你开启了评论系统
read_time: true
---

> ✨ 这篇文章教大家如何搭建一个由GitHub Page托管的博客

---

## 📝 正文内容开始

### 一、Github Page 是什么？

[GitHub Pages](https://pages.github.com/) 是 GitHub 提供的一项 **免费的网站托管服务**，专门用于托管静态网页（如博客、项目文档、作品集等）。

它支持绑定自定义域名、HTTPS 安全访问，并且与 GitHub 仓库紧密结合，**每次推送代码就能自动部署网站**，是非常适合开发者使用的建站方式。

### 二、为什么要用GitHub Page托管？

#### 1：建站成本低

首先，如果想建个人主页需要租VPS,一个月几十甚至上百的租金对于学生或者普通人是一笔巨大的支出

而GitHub Pages 完全免费，而且支持自定义域名，比如我的[xiaomao8.github.io](https://xiaomao8.github.io/)就是一个完全自定义的域名加上了github.io的后缀
，非常适合个人或者小型项目使用

#### 2：技术门槛低

使用GitHub Pages不用学习前后端交互等复杂技术，只需学习以下几种技术就可以快速掌握自己的个人博客

| 技术名         | 简要说明 |
|----------------|----------|
| **Git**        | 分布式版本控制系统 |
| **GitHub Pages** | 托管静态网页的服务 |
| **Jekyll**     | 静态网站生成器 |
| **Liquid**     | 模板语言，控制页面结构 |
| **YAML**       | 用于配置和数据结构 |




只需学习这五种技术就可以快速上手一个使用开源模板的博客，支持很多功能

### 三、如何使用GitHub Page托管来做一个自己的博客

#### 1：打开[GitHub Pages](https://pages.github.com/)，直接点击GitHub repository

点击右上角的+号，新建一个仓库(New repository)

点击之后，我们可以看到如下的页面

![GitHub 设置示意图](/assets/img/1750774629307.png)

在这个页面中填入自己想自定义的网址，比如我，就填入xiaomao8.github.io，这个.github.io前面的是可以自定义的域名名称

接下来，我会讲两种本地克隆文件夹的方式，如使用命令行的，则跳转到3


#### 2：使用GitHub Desktop这个软件来克隆我们已经创建好的项目


首先，点击文件，找到克隆在线仓库，点第三个网址克隆

如果你的软件是英文的话，就点左边第一个，点击然后点击第三个，在弹出的窗口选择最右边的那个

点击之后，我们可以看到如下的页面

![](/assets/img/1750775677372.png)

在上面的框中来输入我们的仓库网址，仓库网址可以在这里看到

![](/assets/img/1750775927853.png)

点击最右边的图标进行复制，复制完毕之后在这个窗口的第一个框中Ctrl+V粘贴，点击克隆，即可克隆到你在下面选择的文件路径下了

进入你的项目文件夹中，添加一个txt格式文本，双击文本复制粘贴以下代码

{% highlight bash %}

<!DOCTYPE html>
<html>
<body>
<h1>Hello World</h1>
<p>I'm hosted with GitHub Pages.</p>
</body>
</html>

{% endhighlight %}

然后返回文件夹，将文件夹名称重命名为index.html

如果改名之后还是文本，看这个文章[Windows电脑显示扩展名](https://blog.csdn.net/weixin_52799373/article/details/133306908)

改完名应该显示这样子

![](/assets/img/1750776815682.png)

**好的，我们已经创建好了一个网页，接下来我们需要将这网页上传到GitHub上面**

打开GitHub Desktop，如图

![](/assets/img/1750816537050.png)

我们在这下面随便输入点什么，然后点击提交，如图

![](/assets/img/1750816537051.png)

提交完之后，我们点击上面的推送或主页显示的推送

![]()

如上面步骤全部完成，恭喜你，你已经成功建立了由GitHub Page托管的主页了



#### 3：使用命令行来克隆我们已经创建好的项目


**打开仓库，找到自己的仓库链接，复制下来**

![](/assets/img/1750775927853.png)

然后在需要把项目克隆的文件夹下，右键点击打开终端


或者Win+R,输入powershell,在这里面输入cd (你要克隆项目的文件夹)

比如我要克隆到我的示例文件夹下，那么就cd E:\示例，结果如下

![](/assets/img/1750815613257.png)

在文件夹右键点击打开终端的效果也是一样的

打开终端之后，我们输入以下命令

{% highlight bash %}
git clone 你刚刚在上面复制下来的仓库链接
{% endhighlight %}

输入之后，如下图，就表示你已经克隆成功了

![](/assets/img/1750815977147.png)

接下来我们创建一个初始网页,输入以下命令

{% highlight bash %}
cd 你的用户名.github.io
echo “Hello World” > index.html
{% endhighlight %}

<!-- {% highlight bash %}
gem install jekyll bundler
{% endhighlight %} -->