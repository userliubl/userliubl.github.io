---
layout: page
title: 首页
---

欢迎来到我的博客，这里记录学习、项目和生活。

## 快速导航

- [全部文章](/archive/)
- [关于我](/about/)
- [GitHub 主页](https://github.com/userliubl)

## 最新文章

{% if site.posts.size > 0 %}
{% for post in site.posts limit: 6 %}
### [{{ post.title }}]({{ post.url | relative_url }})

{{ post.excerpt | strip_html | truncate: 120 }}

`{{ post.date | date: "%Y-%m-%d" }}`
{% endfor %}
{% else %}
还没有发布文章，先去 `_posts` 新建一篇吧。
{% endif %}
