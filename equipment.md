---
layout: default
title: "Equipment"
---

{% for group in site.data.equipment %}

<h3 class="py-3">{{ group.type }}</h3>
<div class="row row-cols-1 row-cols-lg-3 row-cols-md-2 g-4">
  
  {% for item in group.items %}
    <div class="col">
    <div class="card h-100">
      <img class="card-img-top py-3 mx-auto w-50" src="{{ site.baseurl }}{{ item.src }}" alt="{{ item.name }}">
      <div class="card-body">
        <h5 class="card-title">{{ item.name }} ({{ item.type }})</h5>
        <h6 class="card-subtitle mb-2 text-muted">{{ item.manufacturer }}</h6>
        <p class="card-text">
          {{ item.description | strip_html | strip_newlines }}
        </p>
      </div>
    </div>
    </div>
  {% endfor %}

</div>

{% endfor %}