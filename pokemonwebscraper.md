---
layout: page
title:  "Pokemon Webscraper"
date:   2018-08-13 10:39:54 -0400
---
<p>
	Smaller-scale projects can be rewarding too, especially if you’re looking for something to work on with friends. I was teaching a friend of mine python, and I had to make sure the project was interesting, so I went with a mockup Pokémon game written in pygame. Although the game didn’t ultimately turn out, I thought the method I took to handle the large amount of content was rewarding on its own. Neither me nor the person I was teaching had the time to implement over 700 Pokémon and a substantial world map, which means data for the game must be mined or generated.
</p>

{% for post in site.categories.pokemon reversed %}
<h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
{% endfor %}