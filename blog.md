---
layout: default
title: Blog
permalink: /blog/
---

# Blog

<div class="blog-grid">
  {% for post in site.posts %}
    <div class="blog-tile">
      <h3><a href="{{ post.url | relative_url }}">{{ post.title | escape }}</a></h3>
      <p class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</p>
      <div class="post-excerpt">
        {{ post.excerpt | strip_html | truncatewords: 100 }}
      </div>
      <a href="{{ post.url | relative_url }}" class="read-more">[link to full post]</a>
    </div>
  {% endfor %}
</div>
