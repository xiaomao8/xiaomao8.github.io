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
read_time: true    #显示时间
header:
  teaser: /assets/img/logo.png    
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

**注意！接下来所有教程都建立在你已经拥有GitHub账户的基础上，如果没有请先注册一个**

#### 1：打开[GitHub Pages](https://pages.github.com/)，直接点击GitHub repository

点击右上角的+号，新建一个仓库(New repository)

点击之后，我们可以看到如下的页面

![GitHub 设置示意图](/assets/img/1750774629307.png)

在这个页面中填入自己想自定义的网址，比如我，就填入xiaomao8.github.io，这个.github.io前面的是可以自定义的域名名称

接下来，我会讲两种本地克隆文件夹的方式，如使用命令行的，则跳转到3


#### 2：使用GitHub Desktop这个软件来克隆我们已经创建好的项目

[GitHub Desktop下载链接](https://desktop.github.com/download/)

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

![](/assets/img/1750817056232.png)

推送完成之后，我们可以在仓库的这里看到我们的上传历史记录

![](/assets//img/1750817402102.png)

最后，打开你的用户名.github.io，就可以看到Hello World了

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

创建完毕后，我们来进行提交和推送，输入以下命令

{% highlight bash %}
git add --all
git commit -m “初始提交”
git push -u origin main
{% endhighlight %}

稍等一会，输入你的用户名.github.io，就可以看到Hello World

如你完成了以上步骤，恭喜你，你已经成功建立了由GitHub Page托管的个人主页了

### 四、使用Jekyll来部署你的个人主页

>**注意，接下来的步骤的前提是你已经部署好了Jekyll的环境了，如果你还没有部署**
>**请看我的[配置Jekyll环境](https://xiaomaowu.github.io/教程/jekyll/2025/06/24/>my-blog-in-ruby-jekyll.html)**

#### 1.搭建框架

进入你的项目文件夹，右键选择用终端(Powershell)打开

或者是直接打开Powershell输入

{% highlight bash %}
cd 你的项目文件夹路径
{% endhighlight %}

在项目文件夹内初始化你的项目

{% highlight bash %}
jekyll new 你的项目名称
{% endhighlight %}

<!-- {% highlight bash %}
gem install jekyll bundler
{% endhighlight %} -->

如果在初始化项目的过程中出现了一直卡在这段的情况

![](/assets/img/1750911446161.png)

那么我们就先Ctrl+C终止我们的初始化进程

来输入命令跳过他的自动bundle install

{% highlight bash %}
jekyll new 你自己的项目名称 --skip-bundle --fource
cd my-site
bundle install  # 手动安装依赖
{% endhighlight %}

**为什么会出现这种情况呢?**

因为他自动引用国外的网站配置依赖，如果网不好的话或者是因为国内的防火墙都会导致他压根连不上国外的网站导致他需要连接国外源的时候配置的时候压根连接不上导致卡死

完成之后呢，应该能在我们项目名称的文件夹下看到以下几个文件

{% highlight bash %}
_config.yml
Gemfile
index.md
about.md
_posts/
{% endhighlight %}

为了确认他是否安装成功我们输入命令

{% highlight bash %}
bundle exec jekyll serve
{% endhighlight %}

如果他显示这样子就代表他搭建成功了,出现的警告可以不用管，要是想消除后面会说

![](/assets/img/1750912061612.png)

接下来，我们来验证他是否初始化，我们按住Ctrl点击这个127.0.0.1:4000这个网址

![](/assets/img/1750912139362.png)

显示出来了这个初始页面就说明初始化成功了，接下来我们需要构建html发布网页,输入命令

{% highlight bash %}
bundle exec jekyll build
{% endhighlight %}

只要没弹Error或者一大堆英文就代表构建成功了，接下来我们来使用当下最受欢迎的自定义模板来建我们的个人博客

#### 2.套用模板

好的，现在我们已经初始化成功了，现在来套用当下最受欢迎的Minimal Mistakes开源模板来自定义我们的主页

[项目仓库和示例文档链接](https://github.com/mmistakes/mm-github-pages-starter)

**套用有两种方法，我这里只展示本地套用，适用于网络不好的用户**

把他项目里面的文件克隆到本地

{% highlight bash %}
git clone https://github.com/mmistakes/minimal-mistakes.git
{% endhighlight %}

然后把这个文件夹克隆到本地，打开他的文件夹复制这四个文件进入你的项目文件夹

{% highlight bash %}
├── _includes/     ← 从 minimal-mistakes 复制
├── _layouts/      ← 从 minimal-mistakes 复制
├── _sass/         ← 从 minimal-mistakes 复制
├── assets/        ← 从 minimal-mistakes 复制
{% endhighlight %}

然后我们需要修改_config,找到根目录的_config文件使用VsCode打开

把他原来全部删除，添加以下的行

{% highlight bash %}
title: "我的博客"
email: "your-email@example.com"
description: >-
  这是一个用 Minimal Mistakes 搭建的博客，支持本地部署，无需依赖网络。
baseurl: ""  # 留空，表示部署到根路径
url: "http://localhost:4000"  # 本地测试地址

repository: 你的仓库名/你的仓库名.github.io  # 可选，如果将来部署到 GitHub Pages

# 不用 remote_theme，也不用 theme，使用本地主题文件夹
# theme: minima
# remote_theme: mistakes/minimal-mistakes

# 插件设置
plugins:
  - jekyll-feed
  - jekyll-seo-tag
  - jekyll-sitemap
  - jekyll-include-cache

# 启用语言、导航等功能（Minimal Mistakes 支持）
locale: zh-CN
minimal_mistakes_skin: "default" # 可选皮肤名，例如 dark, air, neon
markdown: kramdown
highlighter: rouge

# 导航菜单示例（可根据你的实际页面调整）
nav:
  - title: "首页"
    url: /
  - title: "关于"
    url: /about/

# 作者信息（可在页面中引用）
author:
  name   : "你的名字"
  avatar : "/assets/images/avatar.png"
  bio    : "这里写简介，比如：程序员，写博客，爱开源。"
  location: "China"
{% endhighlight %}

**自己按需修改**

然后在Gemfile里面添加这四行，如果打开的时候让你选择怎么打开直接选择使用记事本打开

{% highlight bash %}
gem "jekyll-seo-tag"
gem "jekyll-sitemap"
gem "jekyll-include-cache"
gem "webrick", "~> 1.7" 
{% endhighlight %}

添加完之后直接

{% highlight bash %}
bundle install
{% endhighlight %}

如果一直卡着，大概率就是网络导致的，这时候我们来修改他的镜像源

{% highlight bash %}
bundle config mirror.https://rubygems.org https://mirrors.tuna.tsinghua.edu.cn/rubygems
{% endhighlight %}

然后重新安装

{% highlight bash %}
bundle install
{% endhighlight %}

安装完之后运行

{% highlight bash %}
bundle exec jekyll serve
{% endhighlight %}

按Ctrl点击网页

如果显示这样就代表成功了

![](/assets/img/1750918718579.png)

这样子我们的基础搭建就完成了，接下来的篇章我们会讲如何使用这个minimal-mistakes来自定义自己的个人博客