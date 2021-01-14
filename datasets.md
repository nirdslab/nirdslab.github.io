---
layout: default
title: "Datasets"
---


<!-- <ul>
  {% for dataset in site.datasets %}
    <h3>
      <a href="{{ dataset.url }}">{{ dataset.title }}</a>
    </h3>
  {% endfor %}
</ul> -->

<div class="card-columns">
  {% for dataset in site.datasets %}
    <div class="card">
      <div class="card-body">
        <h5 class="card-title"><a href="{{ dataset.url }}">{{ dataset.title }}</a></h5>
        <p class="card-text">
          {{ dataset.excerpt | strip_html | strip_newlines | truncate: 200}}
          <a href="{{ dataset.url }}">Read more..</a>
        </p>
      </div>
    </div>
  {% endfor %}
</div>
