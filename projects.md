---
layout: page
title: Projects
description: The projects Carmen is building.
---
## Projects

The real work, in public.

{% for project in site.pages %}
  {% if project.url contains '/projects/' and project.title %}
  <div class="project-card">
    <h3><a href="{{ project.url | relative_url }}">{{ project.title }}</a></h3>
    {% if project.status %}<span class="status">{{ project.status }}</span>{% endif %}
    {% if project.description %}<p>{{ project.description }}</p>{% endif %}
  </div>
  {% endif %}
{% endfor %}
