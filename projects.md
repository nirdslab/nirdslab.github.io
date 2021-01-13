---
layout: default
title: "Projects"
permalink: /projects/
---

<!-- <ul>
  {% for project in site.projects %}
    <h3>
      <a href="{{ project.url }}">{{ project.title }}</a>
    </h3>
    <p>
      {{ project.excerpt }}
    </p>
  {% endfor %}
</ul> -->



<div class="card-columns">
  {% for project in site.projects %}
    <div class="card">
      <a href="{{ project.url }}">
        <img class="card-img-top" src="{{ site.baseurl }}{{ project.image }}" alt="{{ project.title }}">
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
