---
layout: default
title: 'Team'
---

<p style=" border-bottom: 1px solid #eee; font-family: inherit; font-weight: 500; line-height: 1.1; color: inherit;"></p>

<div >
{% for team in site.data.team %}
<a class="btn btn-primary" href="#categories" role="button" style=" background-color: #337ab7; border-color:#2e6da4;">{{team.category }}</a>
{% endfor %}
</div>

{% for team in site.data.team %}

<div class="col-lg-12" id ="categories">

<h2 class="page-header"  style="padding-bottom: 9px; margin: 40px 0 20px; border-bottom: 1px solid #eee;border-bottom: 1px solid #eee; font-family: inherit; font-weight: 500; line-height: 1.1; color: inherit;">{{ team.category }}
<a href="#" class="page-top" style=" float:right; color: #337ab7; "><i class="fas fa-chevron-circle-up"></i></a></h2>

</div>
<div class="row p-2">
    {% for member in team.members %}
    {%- include person.html member=member -%}
    {% endfor %}
</div>
{% endfor %}
