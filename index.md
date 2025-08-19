---
layout: default
title: "Welcome"
permalink: /
---

# 🚀 Welcome to My Blog

Here I share reflections on financial markets, legendary investors, and hidden trading signals.

---

## 📰 Latest Posts
<ul>
{% for post in site.posts limit:5 %}
  <li>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    <small> — {{ post.date | date: "%Y-%m-%d" }}</small>
  </li>
{% endfor %}
</ul>
