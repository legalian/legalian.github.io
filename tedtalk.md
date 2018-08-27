---
layout: page
title:  "TED Talk"
date:   2018-08-13 10:39:54 -0400
---
<iframe width="560" height="315" src="https://www.youtube.com/embed/hKJgAeaGtfU" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
<p>
This was something I spent a lot of time preparing for. Most of my projects involve a lot of development work, so this kind of presentation was a change of pace for me. The purpose of the ted talk was to explain the concept of a neural network to an audience who had no experience with them. I wanted to stress that machine learning techniques are best used in combination with other tools in a computer scientist’s toolbox, because I see high school students struggle with this a lot when they investigate neural networks.
</p>
<p>
	More pages will be added here regarding the construction of the chess AI demoed at the TED talk.
</p>

{% for post in site.categories.ted reversed %}
<h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
{% endfor %}