---
layout: page
title: Links
permalink: /links/
---
{% for item in site.links %}

    {% capture day %}{{ post.date | date: '%m%d%Y' }}{% endcapture %}
    {% capture nday %}{{ post.next.date | date: '%m%d%Y' }}{% endcapture %}

    {% if day != nday %}
        <h5 class="date">{{ post.date | date: "%A, %B %e, %Y" }}</h5>
    {% endif %}
    <a href="{{ item.link }}"><b>{{ item.title }}</b></a><br/>
    {{ item.description }}
    <br/>
    <hr>

{% endfor %}

