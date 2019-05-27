---
layout: page
title: Fresh Links
permalink: /fresh-links/
---
{% assign linksByYearMonthDay = site.links | group_by_exp:"link", "link.date | date: '%B %d, %Y'"  %}
{% for yearMonthDay in linksByYearMonthDay %}
  <h3>{{ yearMonthDay.name }}</h3>
  {% for item in yearMonthDay.items %}
  <a href="{{ item.link }}"><b>{{ item.title }}</b></a><br/>
  {{ item.description }}
  <br/>  
  {% endfor %}
{% endfor %}

