---
layout: page
title: Projects
permalink: /projects/
# description: Selected analytics, data engineering, and applied data science projects by Alex Tran.
nav: true
nav_order: 1
---

Browse more of my work on [GitHub](https://github.com/alextran1357).

<div class="projects">
  {% assign sorted_projects = site.projects | sort: "importance" %}
  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
      {% for project in sorted_projects %}
        {% assign project_alt = project.title | append: " project preview" %}
        <div class="col">
          <article class="card h-100 hoverable">
            <a href="{{ project.url | relative_url }}" aria-label="View {{ project.title }} case study">
              {% include figure.liquid loading="eager" path=project.img title=project.title alt=project_alt class="card-img-top" sizes="250px" %}
            </a>
            <div class="card-body">
              <h2 class="card-title">{{ project.title }}</h2>
              <p>{{ project.description }}</p>
              <p class="mb-0">
                <a href="{{ project.url | relative_url }}">View case study</a>
                {% if project.github %}
                  · <a href="{{ project.github }}" target="_blank" rel="external nofollow noopener">Source code</a>
                {% endif %}
                {% if project.live %}
                  · <a href="{{ project.live }}" target="_blank" rel="external nofollow noopener">Live demo</a>
                {% endif %}
              </p>
            </div>
          </article>
        </div>
      {% endfor %}
    </div>
  </div>
</div>
