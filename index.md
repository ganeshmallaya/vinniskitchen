---
layout: default
title: Home
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

# Vinni’s Kitchen

Homestyle Indian food, made fresh. We cater events and weekly meals.

- 🧑‍🍳 **Lady‑owned, community‑loved**
- 🥗 **Catering** for parties & events
- 📦 **Weekly Meal Boxes** (pre‑order)

<div align="center" style="margin:1.25rem 0;">
  <a href="{{ '/menu/' | relative_url }}" style="padding:10px 16px;border:1px solid #0366d6;border-radius:6px;text-decoration:none;">See Menu</a>
  &nbsp;
  <a href="https://g.page/r/" target="_blank" rel="noopener" style="padding:10px 16px;border:1px solid #0366d6;border-radius:6px;text-decoration:none;">Read Google Reviews</a>
</div>

## Featured Recipes
{% assign recipes = site.posts | where_exp: "post", "post.categories contains 'recipe'" %}
<ul>
{% for post in recipes limit:5 %}
  <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a> — {{ post.date | date: "%b %d, %Y" }}</li>
{% endfor %}
</ul>
