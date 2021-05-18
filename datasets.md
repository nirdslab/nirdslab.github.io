---
layout: default
title: "Datasets"
---

<div class="row row-cols-1 row-cols-lg-3 row-cols-md-2 g-4">
  {% for dataset in site.datasets %}
    <div class="col">
      <div class="card">
        <div class="card-body">
          <h5 class="card-title"><a href="{{ dataset.url }}">{{ dataset.title }}</a></h5>
          <p class="card-text">
            {{ dataset.description | strip_html | strip_newlines | truncate: 200 }}
            <a href="{{ dataset.url }}">Read more..</a>
          </p>
        </div>
      </div>
    </div>
  {% endfor %}
</div>
