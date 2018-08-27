---
layout: post
title:  "Rubik's Puzzle Nuances"
date:   2018-02-19 10:39:54 -0400
categories: puzzle
---
![figure 5]({{"/assets/puzzle/chapter3/screenshot1.png"|absolute_url}})
<p>
The generator is able to make truncated shapes very easily. Multiple sets of shape planes can be added, and the puzzle's volume will be bounded by all of them, so adding both a shape and that shape's dual will allow truncated shapes to be added. Both vertex and edge truncations can be done for any of the natural solids.
</p>
![figure 5]({{"/assets/puzzle/chapter3/screenshot2.png"|absolute_url}})
<p>
The generator is not restricted to creating just edge turning, vertex turning, or face turning puzzles. Hybrids can be made, which twist about multiple types of features. Adding multiple sets of cutting planes allows any combination to be made.
</p>
![figure 5]({{"/assets/puzzle/chapter3/screenshot3.png"|absolute_url}})
<p>
Higher order puzzles are easy, too. Multiple of the same set of planes can be added with different depths. Stacking cube planes like that creates the '5x5' cube, but the same principle applies to any puzzle.
</p>
<div style="display:flex; margin:1em;">
    <div style="flex:45%;">
        <img src="{{"/assets/puzzle/chapter3/screenshot4a.png"|absolute_url}}"/>
    </div>
    <div style="flex:45%;">
        <img src="{{"/assets/puzzle/chapter3/screenshot4b.png"|absolute_url}}"/>
    </div>
</div>
<p>
While all cutting planes must come from compatable symmetry groups, shape planes do not have this restriction. In this example, the dodecahedron can be scrambled with tetrahedron cutting planes and still stay the same shape, because tetrahedron cutting planes line up with icosahedron cutting planes.
</p>
<div style="display:flex; margin:1em;">
    <div style="flex:45%;">
        <img src="{{"/assets/puzzle/chapter3/screenshot5a.png"|absolute_url}}"/>
    </div>
    <div style="flex:45%;">
        <img src="{{"/assets/puzzle/chapter3/screenshot5b.png"|absolute_url}}"/>
    </div>
</div>
<p>
Not all combinations of shape and cutting planes have that property. Some change shape when scrambled, but there's nothing wrong with that- there are puzzles for sale in real life that behave this way.
</p>


<div>
{% if page.previous_in_category != nil %}
<a href="{{page.previous_in_category.url}}" style="float:right;">{{page.previous_in_category.title}} &#8250;</a>
{% endif %}
{% if page.next_in_category != nil %}
<a href="{{page.next_in_category.url}}" class="float:left;">&#8249; {{page.next_in_category.title}}</a>
{% endif %}
</div>


