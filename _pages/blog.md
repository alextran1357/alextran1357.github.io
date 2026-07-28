---
layout: page
permalink: /blog/
title: Insights
nav: true
nav_order: 3
description: Insights from Alex Tran about data analysis, machine learning, and analytics engineering.
---

Selected LinkedIn posts where I explain the decisions, tradeoffs, and lessons behind my analytics and machine-learning projects.

{% for insight in site.data.insights %}

  <article>
    <h2>{{ insight.title }}</h2>
    <p class="post-meta">{{ insight.date }}</p>
    <p>{{ insight.summary }}</p>
    <details>
      <summary><strong>Read full post</strong></summary>
      <div class="mt-3">{{ insight.body | markdownify }}</div>
    </details>
    <p><a href="{{ insight.url }}">View original on LinkedIn</a></p>
  </article>
  {% unless forloop.last %}<hr>{% endunless %}
{% endfor %}
