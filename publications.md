---
layout: default
title: "Publications"
---
{% for pubs in site.data.publications %}
<h3 style="margin-top: 1em;">{{ pubs.type }}</h3>
<ul style="text-align: justify;">
    {% for pub in pubs.items %}
    <li>
        {% if pub.authors != "" %}
            {{pub.authors}},
        {% endif %}
        {% if pub.title != "" %}
            <strong>{{pub.title}}</strong>,
        {% endif %}   
        {% if pub.info != "" %}
            <i>{{pub.info | markdownify}}</i>,
        {% endif %}
        {% if pub.date != "" %} 
            <i>{{pub.date}}</i>
        {% endif %}    
        {% if pub.publisher != "" %}
            ({{pub.publisher}})
        {% endif %}
        {% if pub.link != "" %}
            {% assign link = pub.link %}
            <a href="{{pub.link}}" target="_blank">[Link]</a>
        {% endif %}    
    </li>
    {% endfor %}
</ul>
{% endfor %}