---
layout: page
title: About
permalink: /about/
---


This is my website. I write about projects that I've done and this website is still under heavy construction and review.

<h1>Voxel engine posts</h1>
<ul>
	{% for post in site.categories.voxel reversed %}
<li><h3><a href="{{ post.url }}">{{ post.title }}</a></h3></li>
	{% endfor %}
</ul>

<h1>Breadboard computer posts</h1>
	{% for post in site.categories.breadboard reversed %}
<li><h3><a href="{{ post.url }}">{{ post.title }}</a></h3></li>
	{% endfor %}

<h1>Proof engine posts</h1>
<ul>
	{% for post in site.categories.proof reversed %}
<li><h3><a href="{{ post.url }}">{{ post.title }}</a></h3></li>
	{% endfor %}
</ul>
