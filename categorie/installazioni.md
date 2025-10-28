---
layout: default
title: Installazioni
permalink: /categorie/installazioni/
---

# Installazioni

{% assign posts_cat = site.categories.installazioni | sort: "date" | reverse %}
{% if posts_cat and posts_cat.size > 0 %}
<ul>
  {% for post in posts_cat %}
  <li>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    <small> — {{ post.date | date: "%d %B %Y" }}</small>
    {% if post.excerpt %}<br>{{ post.excerpt }}{% endif %}
  </li>
  {% endfor %}
</ul>
{% else %}
<p>Nessun articolo ancora.</p>
{% endif %}
