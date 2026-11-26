---
layout: default
title: 链接合集
---

# 文章列表

{% if site.posts.size > 0 %}
<ul class="post-list">
  {% for post in site.posts %}
    <li>
      <span class="post-date">{{ post.date | date: "%Y-%m-%d" }}</span> · 
      <a href="{{ post.url | relative_url }}"><strong>{{ post.title }}</strong></a>
      {% if post.description %}
        <div style="color: #586069; font-size: 15px; margin-top: 4px;">{{ post.description }}</div>
      {% endif %}
    </li>
  {% endfor %}
</ul>
{% else %}
<p>暂无已发布的日报内容，敬请期待。</p>
{% endif %}

{% include follow-card.html %}
