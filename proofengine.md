---
layout: page
title:  "Proof Engine"
date:   2018-08-13 10:39:54 -0400
---
<p>
I’d argue that the most powerful tools in programming are those that interpret code. Compilers, interpreters, transpilers, and static code analyzers are all able to perform large amounts of intellectual work, enabling tasks which were previously impossible.
The obvious examples are compilers; the world would be a much smaller place if all software had to be written by hand in assembly. Less obvious are optimizations provided by the compiler. There are hundreds of little details that programmers do not need to be aware of because compilers take care of them.
Last summer, for my internship, I worked with webGL and OpenCV.js to create an augmented reality application for mobile in the browser. As computers became more powerful, there came a time when it became feasible to do feature detection in a mobile browser. Rather than create an entirely new implementation of the computer vision algorithms in OpenCV, developers used enscripten, a powerful C to JavaScript transpiler to generate OpenCV's web counterpart. It’s not the only codebase to do this, either. Apples2Oranges is a powerful transpiler capable of converting an entire IOS native application into a PWA.
Beyond compiling or translating code, static analyzers can use logical proofs to find or rule out bugs or violated assertions in code segments. Mathematicians also commonly use proof assistants to ensure that their proofs make sense, and in some cases, generate proofs for smaller conjectures to speed up the mathematician’s work.
Proof generators that accept conjectures that are partially specified are especially powerful, because then extra information can be extracted from a proof. The conjecture “a number equal to five exists”, once proven, may become fully specified, which allows the program to extract that the number in question is five. If a proof generator can operate over an arbitrary set of axioms, then it can reason over conjectures such as, “a JavaScript program equivalent to this C++ application exists.” This allows a proof generator to function as a transpiler, as well.
The problem of reasoning over logical proofs is difficult to do in a way that is both powerful and efficient, but the applications are endless for a proof generator that works well. A very powerful proof generator could be used to optimize code for speed, memory usage, length, translate code into another language, and detect if code has bugs, all without executing any of the given code. The ability to automatically perform large amounts of any logical work on a large scale opens up a world of opportunity that I’d like to explore.
Sophomore and junior year, I worked on this project from a variety of different angles. My earlier attempts include a first order logic system, and type theory system without dependently typed functions, but neither of those were flexible enough to represent useful logical work. The posts below document, on a very shallow level, my most successful proof generator. The proof generator is currently too slow to be given creative axioms and perform useful programming functions, but it was able to prove the fundamental theorem of calculus given the definitions of continuity, limits, integrals, and derivatives, which I consider a success. There is still more that can be done to improve the speed of the algorithm, but that milestone is a good place to rest at.
</p>

{% for post in site.categories.proof reversed %}
<h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
{% endfor %}
