---
layout: page
title: Projects
permalink: /projects/
description: Selected analytics, data engineering, data science, and software projects by Alex Tran.
nav: true
nav_order: 1
---

Browse more of my work on [GitHub](https://github.com/alextran1357).

<style>
  .projects .github-icon {
    margin-left: 0.9375rem;
  }
</style>

<div class="projects">
  {% assign sorted_projects = site.projects | sort: "importance" %}
  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
      {% for project in sorted_projects %}
        {% include projects.liquid %}
      {% endfor %}
    </div>
  </div>
</div>
