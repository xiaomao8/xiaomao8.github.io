---
layout: single
title: "配置Jekyll环境"
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
header:
  teaser: /assets/img/1750987258082.png
---

> ✨ 这篇文章我们来讲怎么配置Ruby和Jekyll环境

---

## 📝 正文内容开始

### 一、Jekyll 是什么？

Jekyll 是一个用于构建静态博客的网站生成器...

### 二、为什么要使用它？

Jekyll 是GitHub官方指定的静态网页托管页面，拥有 多种模板，涉及的技术栈不多，适合新手

### 三、Ruby是什么?

一种开源的动态编程语言，以简洁、易读为设计目标，适合快速开发。

### 四、为什么要使用它?

#### 1.Jekyll（静态博客工具）是用 Ruby 写的，必须安装 Ruby 才能运行。

#### 2.通过 gem（Ruby 的包管理器）安装和管理工具（如 jekyll）。

### 五、如何安装？

#### 1.我们需要来安装Ruby，因为Jekyll是基于Ruby上面的

**在以下几个链接都能获取到安装包**

RubyInstaller官网 https://rubyinstaller.org/downloads/

国内下载站 https://rubyinstaller.cn/

下载下来之后呢，会看到这个页面

![](/assets/img/1b6224b751db96dd23ce2dbed5479dc.png)

直接一路下一步即可

安装完成之后，会显示这个页面

![](/assets//img/微信图片_20250625163309.png)

**在这个页面中我们选择一和三，在下面输入1,3**

**由于2兼容性问题很多，我们在接下来不会选择2**

选择完成之后，按回车，等待一会就会出现如下的界面

![](/assets/img/ac7932a4e34b7b808769919347907ae.png)

一路下一步就可以了


我们接下来验证我们ruby有没有安装成功,输入以下命令来验证

{% highlight bash %}
ruby -v
{% endhighlight %}

![](/assets/img/1750841004137.png)

能看到这个说明ruby已经安装完成了

**接下来我们需要给ruby换源，因为ruby默认的源是国外网站，从国外网站下载会很慢，所有我们需要把他的源换为国内源**

输入命令

{% highlight bash %}
gem sources add https://gems.ruby-china.com/ 
gem sources remove https://rubygems.org/
{% endhighlight %}

然后输入命令验证是否已经把源换成了国内源

{% highlight bash %}
gem sources -l
{% endhighlight %}

如果显示这个就代表换源成功

{% highlight bash %}
*** CURRENT SOURCES ***

https://gems.ruby-china.com/
{% endhighlight %}

我们在ruby的步骤就全部完成了

#### 2.我们开始安装Jekyll

输入命令

{% highlight bash %}
gem install jekyll
{% endhighlight %}


如果出现了类似以下的报错

![](/assets/img/1750842234657.png)

输入命令修复DevKit包

{% highlight bash %}
ridk install
{% endhighlight %}

跟之前一样选择1,3

修复完之后重新输入命令

{% highlight bash %}
gem install jekyll
{% endhighlight %}

出现这个就是安装成功了

![](/assets/img/1750844508410.png)

#### 3.我们开始安装bundler(可选)

bundler是一个Ruby的依赖管理工具，用于确保项目使用的版本正确，一般不强制安装

输入以下命令

{% highlight bash %}
gem install bundler
{% endhighlight %}

出现这个就是安装成功了

{% highlight bash %}
Successfully installed bundler-2.6.9
1 gem installed
{% endhighlight %}

**好的，到这一步，我们的环境就已经配置完毕了**