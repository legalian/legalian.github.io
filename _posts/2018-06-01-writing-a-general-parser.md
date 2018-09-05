---
layout: post
title:  "Breadboard computer operations"
date:   2018-06-01 10:39:54 -0400
categories: proof
---
<p>
OOPS! This page is still being worked on.
</p>


<div>
{% if page.previous_in_category != nil %}
<a href="{{page.previous_in_category.url}}" style="float:right;">{{page.previous_in_category.title}} &#8250;</a>
{% endif %}
{% if page.next_in_category != nil %}
<a href="{{page.next_in_category.url}}" class="float:left;">&#8249; {{page.next_in_category.title}}</a>
{% endif %}
</div>
