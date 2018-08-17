---
layout: page
title:  "TED Talk"
date:   2018-08-13 10:39:54 -0400
---
<iframe width="560" height="315" src="https://www.youtube.com/embed/hKJgAeaGtfU" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
<p>
	ted talk ted talk ted talk
</p>

{% for post in site.categories.ted %}
<h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
{% endfor %}