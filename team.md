---
layout: default
title: "Team"
---
{% for team in site.data.team %}
## {{ team.category }}
<div class="row p-2">
    {% for member in team.members %}
    {%- include person.html member=member -%}
    {% endfor %}
</div>
{% endfor %}