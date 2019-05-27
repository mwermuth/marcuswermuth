---
layout: page
title: Links
permalink: /links/
---
{% assign linksByYearMonthDay = site.links | group_by_exp:"link", "link.date | date: '%B %d, %Y'"  %}
{% for yearMonthDay in linksByYearMonthDay %}
  <h3>{{ yearMonthDay.name }}</h3>
  <ul>
  {% for item in yearMonthDay.items %}
    <li><a href="{{ item.link }}"><b>{{ item.title }}</b></a><br/>
      {{ item.description }}</li>
  {% endfor %}
  </ul>
{% endfor %}

