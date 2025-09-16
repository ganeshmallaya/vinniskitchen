{% include nav.html %}
<link rel="stylesheet" href="/assets/css/custom.css">
<img class="header-logo" src="/assets/images/vinniskitchen-logo.png" alt="Vinni's Kitchen logo">

# Recipes
{% assign recipes = site.posts | where_exp: "post", "post.categories contains 'recipe'" %}
<ul>
{% for post in recipes %}
  <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a> — {{ post.date | date: "%b %d, %Y" }}</li>
{% endfor %}
</ul>