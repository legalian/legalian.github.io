---
layout: page
title:  "Voxel Engine"
date:   2018-08-13 10:39:54 -0400
---
<p>
	Voxel games have seen a rise in popularity as people begin to understand them more. The development of these games is interesting; they often require creative solutions to fulfill voxel game’s demand for resources. Volumetric information can require a lot of memory to store, and a lot of processing power to update. Some of these solutions share commonality with algorithms originally developed for medical imaging, and for good reason- they both need to turn volumetric information into mesh that can be rendered.
</p>
<p>
	I think many CS students are reluctant to work on video games because it doesn’t sound very serious, but they don’t appreciate the technical challenges to overcome with 3D games that force you to learn. I worked on a voxel engine from 8th grade through sophomore year and ended up with a very workable result that I plan to develop games with in the future. Back in 8th grade I worked in python with the graphics library panda3D, but performance issues and global interpreter lock drove me to become proficient in C++ and OpenGL. I started out just trying to make a simple Minecraft clone, where the simplest volumetric data storage and isosurface extraction algorithms suffice. After finishing the bare-bones essentials of that voxel engine, though, I decided that I wanted to take it further.
</p>
<p>
	I consider procedualworld’s voxel farm to be a major inspiration moving forward from my 8th grade Minecraft mock-up. I’ve read every blog post more than once, first for inspiration and then for guidance.
</p>
<p>
	These pages are still under construction. Certain elements of them will be rewritten to be more understandable, and screenshots of the project will be included as well.
</p>
![figure 1]({{"/assets/vox/title/figure1.png"|absolute_url}})
{% for post in site.categories.voxel %}
<h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
{% endfor %}