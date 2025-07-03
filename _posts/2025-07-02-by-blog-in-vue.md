---
layout: single
title: "Vue环境配置"
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


>**这篇文章我们来讲如何配置Vue环境**


---

## 正文内容开始

### 一、什么是Vue

Vue.js(通常成为Vue)是一个用于构建用户界面的渐进式网页框架，由尤雨溪(Evan You)创建,于2014年发布，现在已经成为了最流行的前端框架之一

### 二、Vue的主要用途

Vue主要用于创建单页用户

创建动态网页

开发复杂的交互式前后端应用

构建可复用的UI组件

### 三、如何安装

> **注意，我以下的教程全部都在Windows环境下，下次有机会会出一套Linux的教程**

#### 1.我们需要安装[Node.Js](https://nodejs.cn/download/)


选择Windows安装包(.msi) 64位(如使用32位电脑用户则选择32位)

输入这两个命令验证是否安装完成

{% highlight powershell %}
node -v
npm -v
{% endhighlight %}

如显示版本号则表示安装成功

![](/assets/img/1751459807604.png)

**常见问题**

> 如果出现以下这种报错信息，可以尝试使用管理员启动powershell或者是输入以下命令来提权

![](/assets/img/1751459430597.png)


**1.永久提权**

{% highlight powershell %}
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
{% endhighlight %}

**2.单次提权(仅限本次命令行窗口)**

{% highlight powershell %}
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
{% endhighlight %}

确认验证Node.Js安装完成之后,接下来我们开始安装Vue框架

#### 2.安装Vue框架

> **注意!安装Vue之前请确认你拥有VsCode,我们后续编辑都需要用到此软件，如未安装,点击[下载链接](https://code.visualstudio.com/)即可安装**

安装完成我们的Vue所依赖的Node.Js之后，我们现在开始来安装Vue框架

输入命令开始全局安装Vue/Cli,目的为了可以能一次性安装Vue框架和他的依赖

{% highlight powershell %}
npm install -g @vue/cli
{% endhighlight %}

初次安装可能需要比较长的时间，请耐心等待

安装完成之后输入命令验证是否安装完成

{% highlight powershell %}
vue --version
{% endhighlight %}

验证完成之后我们开始下一步部署

#### 3.部署项目

找到你想部署的文件夹，然后在命令行输入，我这里就以我C盘的123文件夹为例

{% highlight powershell %}
cd C:/123
{% endhighlight %}

进入这个文件夹之后，我们现在开始进行部署

我们创建一个项目

{% highlight powershell %}
vue create my-vue-app
{% endhighlight %}

进入这个页面之后选择第三个

![](/assets/img/1751465740288.png)

>为什么不选前两个呢，因为前两个默认是不带网页路由的，你可以理解为前两个是默认不带一本书中的目录的，你想自己配置非常麻烦，所以我们选择第三个

![](/assets/img/1751465903352.png)

进入这个页面我们使用键盘右边的上下键选择，选择到Router这个选项点击空格即可选择成功

然后我们按Enter确认

![](/assets/img/1751465983127.png)

在这个页面选择3.x,目前主流的不管是企业，个人项目都使用3.x,2.x已经被官方标记过时了，而且组件库也不如3.x丰富

后面的一路确认即可

到这一步，我们的部署已经全部完成了

#### 4.初始化项目

因为Vue默认是不带HTML网页的，所以我们先得给他初始化

{% highlight powershell %}
npm run build
{% endhighlight %}

初始化成功后我们现在来启用我们的项目

{% highlight powershell %}
npm run serve
{% endhighlight %}

启动后显示这个页面，按Ctrl点击`localhost:8080`

![](/assets/img/1751466528877.png)

点击就可以看到我们项目的初始页面了

到这里，我们的Vue环境部署就全部完成了
