---
layout: page
title:  "Puzzle Generator"
date:   2018-08-13 10:39:54 -0400
---
<p>
Rubik’s cubes have a lot of appeal nowadays. People enjoy not only 3x3 cubes, but also higher order puzzles such as 4x4 cubes or 5x5 cubes. Some puzzles don’t conform to a standard cubic shape or turning, and there’s a significant community built around turning puzzles of this nature.
Rather than practice solving these puzzles for speed, I collected many varieties of puzzles with different turning types and orders. Not all interesting puzzles are affordable or available, however, and I thought it would be fun to express my ideas about cubes in the form of a simulator that allows the user to create and manipulate their own in 3d space.
Of all the projects on this site, this one is definitely the oldest. The most recent iteration of this project began and finished in middle school, but it was building off of an older project I had created in elementary school. The project is written in python and panda3d.
</p>
<p>
	These pages are still under construction. Certain elements of them will be rewritten to be more understandable, and screenshots of the project will be included as well.
</p>
![figure 4]({{"/assets/puzzle/title/figure1.png"|absolute_url}})
{% for post in site.categories.puzzle %}
<h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
{% endfor %}