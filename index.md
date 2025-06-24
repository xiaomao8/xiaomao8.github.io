---
layout: home
title: 欢迎访问
author_profile: true
permalink: /
---

<h2>👋 欢迎访问</h2>
<p>这是我写的首页内容。</p>

<h2>📰 最近文章</h2>
<ul>
  {% for post in site.posts limit:5 %}
    <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>

