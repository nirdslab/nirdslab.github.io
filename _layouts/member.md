---
layout: default
---

<h1>{{ page.name }}</h1>

{{ content }}


{% for project in site.projects %}
  {% for member in project.team %}
    {% if page.name == member %}
      <a href="{{project.url}}">{{ project.title}}</a>
    {% endif %}
  {% endfor %}
{% endfor %}
