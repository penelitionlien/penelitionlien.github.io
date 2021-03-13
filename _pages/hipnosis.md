---
layout: page
title: Hipnosis
permalink: /hipnosis
comments: false
image: 
imageshadow: true
---

{% for post in site.categories.Hipnosis %}
 <li><span>{{ post.date | date_to_string }}</span> &nbsp; <a href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}
