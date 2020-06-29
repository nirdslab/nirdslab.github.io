---
layout: default
title: 'Team'
---

<a class="btn btn-primary" href="#faculty" role="button" style="margin-bottom: 5px; background-color: #337ab7;
    border-color: #2e6da4; ">Faculty</a>
<a class="btn btn-primary" href="#phd-students" role="button" style="margin-bottom: 5px; background-color: #337ab7;
    border-color: #2e6da4;">PhD Students</a>
<a class="btn btn-primary" href="#masters-students" role="button" style="margin-bottom: 5px; background-color: #337ab7;
    border-color: #2e6da4;">Masters Students</a>
<a class="btn btn-primary" href="#undergraduate-students" role="button" style="margin-bottom: 5px; background-color: #337ab7;
    border-color: #2e6da4;">Undergraduate Students</a>
<a class="btn btn-primary" href="#visitors" role="button" style="margin-bottom: 5px; background-color: #337ab7;
    border-color: #2e6da4;">Vistors</a>

{% for team in site.data.team %}

<div class="col-lg-12">

<h2 class="page-header" style="padding-bottom: 9px;
    margin: 40px 0 20px;
    border-bottom: 1px solid #eee;border-bottom: 1px solid #eee; font-family: inherit; font-weight: 500; line-height: 1.1;
    color: inherit;">{{ team.category }}<a href="#" class="page-top" style=" float:right; color: #337ab7; "><i class="fas fa-chevron-circle-up"></i></a></h2>

</div>
<div class="row p-2">
    {% for member in team.members %}
    {%- include person.html member=member -%}
    {% endfor %}
</div>
{% endfor %}
