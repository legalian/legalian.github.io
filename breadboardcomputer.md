---
layout: page
title:  "Breadboard Computer"
date:   2018-08-13 10:39:54 -0400
---
<p>
	This project was a slower undertaking for me than some of my other projects, because I found myself alternating between building the computer and waiting on more parts to arrive in the mail. If you are thinking of taking on this project yourself, I highly recommend jameco.com. The IC chips I ordered were very cheap. Breadboards and wires eventually got expensive, however. The only cost-effective method was to cut and strip wire myself and find cheap breadboards to order off of amazon. I also ended up 3D-printing housing to keep the breadboards well organized.
</p>
<p>
	Having control over the opset of the computer can greatly simplify the circuit. For breadboard computers whose cpu is built from logic gates, it makes the most sense to invent your own opset, since it likely won’t be able to run a real OS anyway. This means that, to run code on the machine, you’ll need to write a compiler to compile some language into that opset. I just came up with my own language to parse, so I could make it as barebones as I wanted. This part of the project was an interesting segway into compilers and it gave me something to work on while I waited on parts that I ordered. 
</p>
<p>
	These pages are still under construction. Certain elements of them will be rewritten to be more understandable, and screenshots of the project will be included as well.
</p>

{% for post in site.categories.breadboard reversed %}
<h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
{% endfor %}