---
layout: page
title: Portland State 2013 Capstone Team A 
tagline: AKA the A-Team 
---
{% include JB/setup %}

In 2013, the Mozilla corporation sponsored one Portland State capstone team in their efforts to build a Firefox OS messaging application. Documented here within is their efforts. 

Posts
=====
<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>

