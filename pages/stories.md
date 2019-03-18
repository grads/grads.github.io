---
layout: page
title: Stories
permalink: /stories-roll/
weight: 4
---


{% for post in site.posts %}

<div style="margin-bottom:50px; margin-top:50px">
<h1><b>{{ post.title }}</b></h1>

<p class="article-metadata text-muted">
{{ post.date | date_to_long_string }} -  
<b>
{% assign words = post.content | number_of_words %}
{% if words < 360 %}
less than 1 min read time
{% else %}
{{ post.words | divided_by:180 }} mins read time
{% endif %}
</b>

<br>

{% if post.tags != empty %}
Tags: 
{% for tag in post.tags %}
<span class="badge badge-pill text-primary border border-primary">{{ tag }}</span>
{% endfor %}
{% endif %}
</p>

{{ post.content }}
</div>

<br>

<hr>

{% endfor %}

<footer>
  Everything is going to be okay.</br>
</footer>
