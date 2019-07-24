---
layout: page
title: Writing
permalink: /writing/
---
<div class="archive">

   {% for post in site.posts %}
       {% assign currentDate = post.date | date: "%Y" %}
       {% if currentDate != myDate %}
           {% unless forloop.first %}</ul>{% endunless %}
           <h1>{{ currentDate }}</h1>
           <ul>
           {% assign myDate = currentDate %}
       {% endif %}
       {% if post.subtitle == blank %}
              <li><a href="{{ post.url }}"><span><i>{{ post.date | date: "%B %-d, %Y" }}</i></span> - {{ post.title }} - {{ post.subtitle }}</a></li>
       {% else %}
              <li><a href="{{ post.url }}"><span><i>{{ post.date | date: "%B %-d, %Y" }}</i></span> - {{ post.title }}</a></li>
       {% endif %}
       {% if forloop.last %}</ul>{% endif %}
   {% endfor %}

</div>