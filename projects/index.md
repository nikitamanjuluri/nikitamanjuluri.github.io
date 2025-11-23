---
layout: projects
title: Projects
permalink: /projects/
---

## Projects

<div class="projects-grid">
{% for project in site.projects %}
  <a href="{{ project.url }}" class="project-card">
    <div class="project-image">
      <img src="{{ project.image | default: '/assets/images/projects/default.png' }}" alt="{{ project.title }}">
    </div>
    <div class="project-meta">
      <h3>{{ project.title }}</h3>
      <p>{{ project.excerpt | strip_html | truncatewords: 20 }}</p>
    </div>
  </a>
{% endfor %}
</div>
