---
layout: page
title: Blog
description: Writing from Carmen Bertucci.
---
## Blog

{% for post in site.pages %}
  {% if post.url contains '/blog/' and post.title and post.date %}
  <div class="post-card">
    <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %-d, %Y" }}</time>
    <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
    {% if post.description %}<p>{{ post.description }}</p>{% endif %}
  </div>
  {% endif %}
{% endfor %}
