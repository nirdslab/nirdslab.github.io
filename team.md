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
{% for team in site.data.team %}
<a class="btn btn-info m-1" href="#{{ team.category }}" role="button">{{ team.category }}</a>
{% endfor %}
</div>

{% for team in site.data.team %}

<div class="col-lg-12" id="categories">

<h2 id="{{team.category}}" class="pt-3 pb-2 mx-2 category-header">{{ team.category }}
<a href="#" class="up-icon"><i class="fas fa-chevron-circle-up"></i></a></h2>

</div>
<div class="row p-2">
    {% for member in team.members %}
    {%- include person.html member=member -%}
    {% endfor %}
</div>
{% endfor %}
