---
layout: post
title:  "Understanding Rubik's Puzzles"
date:   2018-02-05 10:39:54 -0400
categories: puzzle
---
<p>
In order to build an expressive and powerful simulator, the components that differentiate twisting puzzles must be understood.
First of all, puzzles are usually regular polyhedra. Puzzles that are spherical or especially irregular are outside the scope of this simulator. 
</p>
![figure 1]({{"/assets/puzzle/chapter1/figure1.png"|absolute_url}})
![screencap 1]({{"/assets/puzzle/chapter1/screenshot1.png"|absolute_url}})
<p>
Secondly, puzzles are typically either face-turning, edge-turning, or vertex-turning. The simulator will support each of these (and a few more for technical reasons). 
</p>
![figure 2]({{"/assets/puzzle/chapter1/figure2.png"|absolute_url}})
<div style="display:flex; margin:1em;">
    <div style="flex:33%;">
        <img src="{{"/assets/puzzle/chapter1/screenshot3a.png"|absolute_url}}"/>
    </div>
    <div style="flex:33%;">
        <img src="{{"/assets/puzzle/chapter1/screenshot3c.png"|absolute_url}}"/>
    </div>
    <div style="flex:33%;">
        <img src="{{"/assets/puzzle/chapter1/screenshot3b.png"|absolute_url}}"/>
    </div>
</div>
<p>
Third, some puzzles are ‘deep cut’ and some are ‘shallow cut’. Each face, edge, or vertex that can be twisted has a ‘cutting plane’, or a plane that divides the puzzle into a turning and not-turning region. Increasing the depth of the cutting plane on the puzzle often increases the challenge because deeper cuts produce pieces that can be moved by many different turns. Also, puzzles can be ‘high order’, which means they have multiple parallel cutting planes, such as a 4x4 or 5x5 rubik’s cube as opposed to a 3x3 rubik’s cube.
</p>
![figure 3]({{"/assets/puzzle/chapter1/figure3.png"|absolute_url}})
<div style="display:flex; margin:1em;">
    <div style="flex:45%;">
        <img src="{{"/assets/puzzle/chapter1/screenshot2a.png"|absolute_url}}"/>
    </div>
    <div style="flex:45%;">
        <img src="{{"/assets/puzzle/chapter1/screenshot2b.png"|absolute_url}}"/>
    </div>
</div>
<p>
Simple puzzles can be defined by their cutting planes and planes that define their shape. A valid set of planes can be uniquely identified by a given set of normal vectors and a scalar depth. The set of normal vectors comes from a solid such as a dodecahedron, octahedron, etc. Sets of planes serve one of two distinct purposes. The volume of the puzzle is bounded by the shape planes, and cut into movable pieces by the cutting planes. Because pieces need to fit into their ending locations after a turn, they can only be rotated around symmetry groups of the solid they belong to. Therefore, cutting planes are always distributed along a symmetry group of the starting solid, with a given depth. Planes that define shape must also have the same symmetry group so that the puzzle does not change shape after it is turned.
If a puzzle defined with some polyhedron’s shape planes is face turning, the cutting planes will be parallel to that shape’s faces. If the puzzle is vertex turning, the cutting planes will be parallel to that shape’s dual solid’s faces. 
</p>
![figure 4]({{"/assets/puzzle/chapter1/figure4.png"|absolute_url}})
<img src="{{"/assets/puzzle/chapter1/picture1.jpg"|absolute_url}}" height="270px" style="display:block; margin-left:auto; margin-right:auto;"/>
<p>
For a puzzle with edge turning, though, calculating the cutting planes can become more difficult. Knowing that a solid and its dual have the same edge-turning cutting planes, aligning the two solids allows a third to be generated. The third solid is the convex hull of the first two solid’s vertices, and its faces are perpendicular to the cutting planes of either edge turning puzzle. 
</p>
![figure 5]({{"/assets/puzzle/chapter1/figure5.png"|absolute_url}})
<p>
<div style="display:flex; margin:1em;">
    <div style="flex:33%;">
        <img src="{{"/assets/puzzle/chapter1/screenshot4a.png"|absolute_url}}"/>
    </div>
    <div style="flex:33%;">
        <img src="{{"/assets/puzzle/chapter1/screenshot4b.png"|absolute_url}}"/>
    </div>
    <div style="flex:33%;">
        <img src="{{"/assets/puzzle/chapter1/screenshot4c.png"|absolute_url}}"/>
    </div>
</div>
For tetrahedrons, this is very simple; a regular tetrahedron is its own dual solid, and aligning them this way produces a cube. The cutting planes perpendicular to the faces of a tetrahedron (turning 120 degrees) and the cutting planes perpendicular to the faces of a cube (turning 180 degrees) represent the first set of symmetry groups that may be used together to produce puzzles.
</p>
<div style="display:flex; margin:1em;">
    <div style="flex:66%;">
        <img src="{{"/assets/puzzle/chapter1/screenshot5.png"|absolute_url}}"/>
    </div>
    <div style="flex:33%;">
        <img src="{{"/assets/puzzle/chapter1/picture2.jpg"|absolute_url}}"/>
    </div>
</div>
<p>
For cubes and octahedrons, the same process produces a different shape, the rhombic dodecahedron. The second set of symmetry groups consists of the cutting planes perpendicular to the faces of a cube (90 degree rotations), the faces of an octahedron (120 degree rotations), and the faces of a rhombic dodecahedron (180 degree rotations).
</p>
<div style="display:flex; margin:1em;">
    <div style="flex:66%;">
        <img src="{{"/assets/puzzle/chapter1/screenshot6.png"|absolute_url}}"/>
    </div>
    <div style="flex:33%;">
        <img src="{{"/assets/puzzle/chapter1/picture3.jpg"|absolute_url}}"/>
    </div>
</div>
<p>
The final set of symmetry groups comes from the icosahedron (120 degree), dodecahedron (72 degree), and rhombic triacontahedron (180 degree) via the same process.
</p>
<div style="display:flex; margin:1em;">
    <div style="flex:66%;">
        <img src="{{"/assets/puzzle/chapter1/screenshot7.png"|absolute_url}}"/>
    </div>
    <div style="flex:33%;">
        <img src="{{"/assets/puzzle/chapter1/picture4.jpg"|absolute_url}}"/>
    </div>
</div>


<div>
{% if page.previous_in_category != nil %}
<a href="{{page.previous_in_category.url}}" style="float:right;">{{page.previous_in_category.title}} &#8250;</a>
{% endif %}
{% if page.next_in_category != nil %}
<a href="{{page.next_in_category.url}}" class="float:left;">&#8249; {{page.next_in_category.title}}</a>
{% endif %}
</div>





