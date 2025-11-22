---
layout: home
title: Projects
permalink: /projects/
---

Below is a gallery of projects. Click any card to view the project detail page.

<div class="projects-grid" style="margin-top:1rem">
{% for project in site.projects %}
  <a href="{{ project.url }}" class="project-card">
    <img src="{{ project.image | default: '/assets/images/projects/default.png' }}" alt="{{ project.title }}">
    <div class="meta">
      <strong>{{ project.title }}</strong>
      <div style="color:#666;font-size:.9rem">{% if project.tags %}{{ project.tags | array_to_sentence_string }}{% endif %}</div>
    </div>
  </a>
{% endfor %}
</div>
