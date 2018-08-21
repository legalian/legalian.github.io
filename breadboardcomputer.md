---
layout: page
title:  "Breadboard Computer"
date:   2018-08-13 10:39:54 -0400
---
<p>
	When people say they built a computer, they typically mean they ordered parts and put those parts together. Rarely do people build computers from scratch, but it does happen. Several notable examples come to mind. Some of these circuits are even able to boot with Linux. Those typically use cpu chips that come in an ic, but other circuits construct their cpu out of more basic chips. I set out to build the latter kind myself, because I believed I had an understanding of how a computer works on a basic hardware level, and a physical, functioning model of a basic Turing machine built across several breadboards sounded like a very cool thing to have.
</p>
<p>
	This project was a slower undertaking for me than some of my other projects, because I found myself alternating between building the computer and waiting on more parts to arrive in the mail. If you are thinking of taking on this project yourself, I highly recommend jameco.com. The IC chips I ordered were very cheap. Breadboards and wires eventually got expensive, however. The only cost-effective method was to cut and strip ?gague wire myself and find cheap breadboards to order off of amazon. I also ended up 3D-printing housing to keep the breadboards well organized.
</p>
<p>
	Having control over the opset of the computer can greatly simplify the circuit. For breadboard computers whose cpu is built from logic gates, it makes the most sense to invent your own opset, since it likely won’t be able to run a real OS anyway. This means that, to run code on the machine, you’ll need to write a compiler to compile some language into that opset. I just came up with my own language to parse, so I could make it as barebones as I wanted. This part of the project was an interesting segway into compilers and it gave me something to work on while I waited on parts that I ordered. 
</p>

{% for post in site.categories.breadboard %}
<h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
{% endfor %}