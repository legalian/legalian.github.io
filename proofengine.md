---
layout: page
title:  "Proof Engine"
date:   2018-08-13 10:39:54 -0400
---
<p>
	This is an old project I worked on in highschool in sophomore and junior year. I'm very interested in formal methods and type theory, but when I started working on the project I didn't know that there were a lot of systems out there already built what I was planning to do. The project was basically a HOL SMT solver. The project as a whole went through many versions, but it actually started as a first order logic solver that searched for set theory proofs.
	The following posts document the later portion of the project, where I switched to designing a type theory solver instead.
</p>

{% for post in site.categories.proof reversed %}
<h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
{% endfor %}
