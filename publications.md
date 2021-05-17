---
layout: default
title: "Publications"
---

{%- for groups in site.data.publications -%}
{% assign pubcount = 1 %}
{%- for group in groups -%}
<div class="card my-3">
  <div class="card-header"><h5 class="py-1 my-0">{{ group.type }}</h5></div>
  <div class="card-body">
    <ol style="text-align: justify; font-size: 0.9em; margin-bottom: 0;" start="{{pubcount}}">
      {%- for pub in group.items -%}
      <li>
        {%- if pub.authors != "" -%}
          {{ pub.authors }}
        {%- endif -%}
        {%- if pub.title != "" -%}
          ,&nbsp;<strong>
          {%- if pub.link -%}
          <a style="color: darkgreen;" href="{{pub.link}}" target="_blank">{{pub.title}}</a>
          {%- else -%}
          <a style="color: darkgreen;" target="_blank">{{pub.title}}</a>
          {%- endif -%}
          </strong>
        {%- endif -%}   
        {%- if pub.in != "" -%}
          ,&nbsp;In <i style="color: darkblue;">{{ pub.in }}</i>
        {%- endif -%}
        {%- if pub.date != "" -%} 
          ,&nbsp;{{pub.date}}
        {%- endif -%}    
        {%- if pub.publisher != "" -%}
          ,&nbsp;{{pub.publisher}}
        {%- endif -%}
        {%- if pub.extra != "" -%}
          .&nbsp;<span style="color: brown;">{{pub.extra}}</span>
        {%- endif -%}
      </li>
      {% assign pubcount = pubcount | plus: 1 %}
      {%- endfor -%}
    </ol>
  </div>
</div>
{%- endfor -%}
{%- endfor -%}