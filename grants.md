---
layout: default
title: "Grants"
---
{% for group in site.data.grants %}
<h3>{{ group.type }}</h3>
<table class="table table-striped table-bordered table-responsive">
    <thead class="thead-dark">
        <tr>
            <td scope="col">Year</td>
            <td scope="col">Amount</td>
            <td scope="col">Topic</td>
            <td scope="col">Source</td>
            <td scope="col">PI</td>
        </tr>
    </thead>
    <tbody>
    {% for grant in group.grants %}
    <tr>
        <td>{{grant.year}}</td>
        <td>{{grant.amount}}</td>
        <td><strong>{{grant.topic}}</strong></td>
        <td>{{grant.from}}</td>
        <td>{{grant.to}}</td>
    </tr>
    {% endfor %}
    </tbody>
</table>
{% endfor %}