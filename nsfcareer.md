---
layout: default
title: "NSF CAREER"
---

<h3>Introduction</h3>

<h3>Recent News</h3>

<h3>Publications</h3>


{%- for groups in site.data.careerpublications -%}
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

<h3>Selected Press Coverage</h3>
<ul>
  <li><a href="https://www.odu.edu/news/2021/5/sampath_jayarathna#.YKaGK51KhPZ">https://www.odu.edu/news/2021/5/sampath_jayarathna#.YKaGK51KhPZ</a></li>
</ul>


<h3>Datasets</h3>

<h3>Software</h3>

<h3>Invited Talks</h3>

<h3>Students</h3>

<ul>
  <li>Bathsheba Farrow - PhD student</li>
  <li>Yasith Jayawardana - PhD student</li>
  <li>Gavindya Jayawardena - PhD student</li>
  <li>Bhnauka Mahanama - PhD student</li>
  <li>Ibrokhim Iskandarov - MS student</li>
  <li>James Owens - Undergraduate student</li>
  <li>Kayla Pineda - Undergraduate student</li>
</ul>

<h3>Outreach</h3>
<ul>
  <li>Teacher Professional Development Workshop, Summer 2021</li>
  <li>Data Science Summer Camp for Hampton Roads High School Students, Summer 2021</li>
</ul>

<h3>Curriculum Modification and Development Providing Interdisciplinary Emphasis</h3>

<h3>Special Thanks</h3>
Andrew Duchowskie (Clemson), Michael Nelson (ODU), Michele Weigle (ODU), Anne Michalek (ODU)
