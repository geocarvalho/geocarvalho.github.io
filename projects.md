---
layout: page
title: Projects
permalink: /projects/
---

A selection of projects I've worked on.

<div class="project-list">
{% for project in site.data.projects %}
<div class="project-card">
  <h3>{{ project.name }}</h3>
  <p>{{ project.description }}</p>
  <p class="project-tech">{{ project.tech }}</p>
  <div class="project-links">
    {% if project.github != "" %}
      <a href="{{ project.github }}">GitHub</a>
    {% endif %}
    {% if project.url != "" %}
      <a href="{{ project.url }}">Live Demo</a>
    {% endif %}
    {% if project.paper %}
      <a href="{{ project.paper }}">Paper</a>
    {% endif %}
    {% if project.blog_post %}
      <a href="{{ project.blog_post | relative_url }}">Read More</a>
    {% endif %}
  </div>
</div>
{% endfor %}
</div>
