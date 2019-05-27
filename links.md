---
layout: page
title: Links
permalink: /links/
---
{% for item in site.links %}
  <a href="{{ item.link }}"><b>{{ item.title }}</b></a>
  {{ item.description }}
{% endfor %}