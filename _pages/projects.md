---
layout: page
title: projects
permalink: /projects/
description: Selected analytics, data engineering, data science, and software projects by Alex Tran.
nav: true
nav_order: 1
horizontal: true
---

These projects show how I work from ambiguous questions and messy source data through reliable pipelines, analysis, validation, and decision-ready outputs. Each case study explains the problem, my contribution, the tradeoffs I made, and the measurable result.

<div class="projects">
  {% assign sorted_projects = site.projects | sort: "importance" %}
  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
      {% for project in sorted_projects %}
        {% include projects_horizontal.liquid %}
      {% endfor %}
    </div>
  </div>
</div>
