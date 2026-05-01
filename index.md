---
layout: page
title: 首页
---

<section class="hero">
  <h2>你好，我是 userliubl</h2>
  <p>这里记录学习、项目和生活，专注于把复杂问题讲清楚。</p>
</section>

<nav class="quick-links">
  <a href="/archive/">全部文章</a>
  <a href="/about/">关于我</a>
  <a href="https://github.com/userliubl">GitHub 主页</a>
</nav>

## 最新文章

{% if site.posts.size > 0 %}
<div class="post-grid">
  {% for post in site.posts limit: 6 %}
  <article class="post-card">
    <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
    <p>{{ post.excerpt | strip_html | truncate: 120 }}</p>
    <div class="post-meta">{{ post.date | date: "%Y-%m-%d" }}</div>
  </article>
  {% endfor %}
</div>
{% else %}
还没有发布文章，先去 `_posts` 新建一篇吧。
{% endif %}
