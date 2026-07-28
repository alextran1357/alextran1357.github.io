---
layout: page
permalink: /blog/
title: writing
nav: true
nav_order: 3
description: Writing by Alex Tran about data analysis, analytics engineering, and software development.
---

{% if site.posts.size == 0 %}

I am keeping this space for future writing about data analysis, analytics engineering, and lessons from building reliable software. There are no published posts yet.

{% else %}

<ul class="post-list">
  {% for post in site.posts %}
    <li>
      <h3><a class="post-title" href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
      <p>{{ post.description }}</p>
      <p class="post-meta">{{ post.date | date: "%B %d, %Y" }}</p>
    </li>
  {% endfor %}
</ul>

{% endif %}
