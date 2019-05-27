---
layout: page
title: Links
permalink: /links/
---
{% for item in site.links %}
    {% capture day %}{{ item.date | date: '%m%d%Y' }}{% endcapture %}
    {% capture nday %}{{ item.next.date | date: '%m%d%Y' }}{% endcapture %}

    {% if day != nday %}
        <h5 class="date">{{ item.date | date: "%A, %B %e, %Y" }}</h5>
    {% endif %}
    <a href="{{ item.link }}"><b>{{ item.title }}</b></a><br/>
    {{ item.description }}
    <br/>
    <hr>
{% endfor %}

