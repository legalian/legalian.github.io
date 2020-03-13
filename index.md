---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: page
---




This is my website. I write about projects that I've done and this website is still under heavy construction and review.

<h1>Voxel engine posts</h1>
{% for post in site.categories.voxel reversed %}
<h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
{% endfor %}

<h1>Breadboard computer posts</h1>
{% for post in site.categories.breadboard reversed %}
<h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
{% endfor %}

<h1>Proof engine posts</h1>
{% for post in site.categories.proof reversed %}
<h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
{% endfor %}


