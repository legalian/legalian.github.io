---
layout: page
title: About
permalink: /about/
---


This is my funky website. I write about projects that I've done and this website is still under heavy construction and review. Go away.

<h1>Voxel engine posts</h1>
{% for post in site.categories.voxel %}
<h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
{% endfor %}


