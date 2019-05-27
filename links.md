---
layout: page
title: Links
permalink: /links/
---
{% for item in site.links %}
  <a href="{{ item.link }}"><b>{{ item.title }}</b></a><br/>
  {{ item.description }}
{% endfor %}