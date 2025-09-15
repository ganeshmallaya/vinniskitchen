---
layout: default
title: Recipes
permalink: /recipes/
---

<p align="center">
  <a href="{{ '/' | relative_url }}">Home</a> •
  <a href="{{ '/recipes/' | relative_url }}">Recipes</a> •
  <a href="{{ '/menu/' | relative_url }}">Menu</a> •
  <a href="{{ '/about/' | relative_url }}">About</a> •
  <a href="{{ '/contact/' | relative_url }}">Contact</a> •
  <a href="https://g.page/r/" target="_blank" rel="noopener">Reviews</a>
</p>

<hr/>

# Recipes

Browse our home‑style recipes.

{% assign recipes = site.posts | where_exp: "post", "post.categories contains 'recipe'" %}
<ul>
{% for post in recipes %}
  <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a> — {{ post.date | date: "%b %d, %Y" }}</li>
{% endfor %}
</ul>
