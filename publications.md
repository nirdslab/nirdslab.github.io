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
            <strong>
            {% if pub.link %}
            <a style="color: darkgreen;" href="{{pub.link}}" target="_blank">{{pub.title}}</a>
            {% else %}
            <a style="color: darkgreen;" target="_blank">{{pub.title}}</a>
            {% endif %}
            </strong>,
        {% endif %}   
        {% if pub.in != "" %}
            In <i style="color: darkblue;">{{ pub.in }}</i>,
        {% endif %}
        {% if pub.date != "" %} 
            {{pub.date}},
        {% endif %}    
        {% if pub.publisher != "" %}
            {{pub.publisher}}.
        {% endif %}
        {% if pub.extra != "" %}
            <span style="color: brown;">{{pub.extra}}</span>
        {% endif %}
    </li>
    {% endfor %}
</ul>
{% endfor %}