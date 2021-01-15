---
layout: default
title: "Projects"
permalink: /projects/
---

<div class="card-columns">
  {% for project in site.projects %}
    <div class="card">
      <a href="{{ project.url }}">
        <img class="card-img-top p-3" src="{{ site.baseurl }}{{ project.image }}" alt="{{ project.title }}">
      </a>
      <div class="card-body">
        <h5 class="card-title"><a href="{{ project.url }}">{{ project.title }}</a></h5>
        <p class="card-text">
          {{ project.excerpt | strip_html | strip_newlines | truncate: 100}}
          <a href="{{ project.url }}">Read more..</a>
        </p>
      </div>
    </div>
  {% endfor %}
</div>
