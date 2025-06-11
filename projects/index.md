---
layout: page
title: Projects
permalink: /projects/
---

<div class="projects-grid">
  {% for project in site.data.projects %}
  <div class="project-card">
    <img src="{{ project.image }}" alt="{{ project.title }}">
    <div class="content">
      <h3>{{ project.title }}</h3>
      <p>{{ project.description }}</p>
      <p>
        {% for tech in project.tech %}<span>{{ tech }}</span>{% unless forloop.last %}, {% endunless %}{% endfor %}
      </p>
      <p><a href="{{ project.link }}">View</a></p>
    </div>
  </div>
  {% endfor %}
</div>
