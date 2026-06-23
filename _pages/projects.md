---
layout: default
title: "Seamus Finn - Projects"
permalink: /projects/
---

# Projects

<div class="row">
{% assign sorted_projects = site.projects | sort: "order" %}

{% for project in sorted_projects %}
  <div class="col-md-6 mb-4">
    <div class="card h-100 project-card">
      {% if project.image %}
      <img
        src="{{ project.image | relative_url }}"
        class="card-img-top"
        alt="{{ project.imagealt | default: project.title }}"
      >
      {% endif %}

      <div class="card-body">
        <h2 class="card-title h4">{{ project.title }}</h2>
        <p class="card-text">{{ project.description }}</p>
        <a href="{{ project.url | relative_url }}" class="btn btn-primary">
          View Project
        </a>
      </div>
    </div>
  </div>
{% endfor %}
</div>
