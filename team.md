---
layout: default
title: 'Team'
---


<style>
    .btn-info {
        background-color: #337ab7;
        border-color: #2e6da4;
    }
    .category-header {
        border-bottom: 1px solid #eee;
        font-weight: 500;
    }
    .up-icon {
        float: right;
        color: #337ab7;
    }
</style>

<div class="py-2">
{% assign categories = site.data.members | group_by: 'category' %}
{% for category in categories %}
<a class="btn btn-info m-1" href="#{{ category.name }}" role="button">{{ category.name }}</a>
{% endfor %}
</div>

{% for category in categories %}

<div id="categories">
<h3 id="{{category.name}}" class="pt-3 pb-2 category-header">{{ category.name }}
<a href="#" class="up-icon"><i class="fas fa-chevron-circle-up"></i></a></h3>
</div>

<div class="row p-2">
    {% for member in category.items %}
    {%- include person.html member=member -%}
    {% endfor %}
</div>

{% endfor %}
