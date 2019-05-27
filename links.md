---
layout: page
title: Links
permalink: /links/
---
{% assign linksByYearMonth = site.links | group_by_exp:"link", "link.date | date: '%Y %b'"  %}
{% for yearMonth in linksByYearMonth %}
  <h3>{{ yearMonth.name }}</h3>
    <ul>
      {% for item in yearMonth.items %}
          <li><a href="{{ item.link }}"><b>{{ item.title }}</b></a><br/>
          {{ item.description }}
          </li>
      {% endfor %}
    </ul>
{% endfor %}

