---
layout: page
title: Links
permalink: /links/
---
{% for item in site.links %}
  <a href="{{ item.link }}"><b>{{ item.title }}</b></a><br/>
  {{ item.description }}
  <br/>
{% endfor %}

{% for link in site.links %}
  {% capture currentdate %}{{post.date | date: "%A, %B %d, %Y"}}{% endcapture %}
  {% if currentdate != thedate %}
    <h3>{{ currentdate }}</h3>
    {% capture thedate %}{{currentdate}}{% endcapture %} 
  {% endif %}
  <a href="{{ item.link }}"><b>{{ item.title }}</b></a><br/>
  {{ item.description }}
  <br/>
{% endfor %}