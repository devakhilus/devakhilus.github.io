---
# layout: home
icon: fab fa-php  # Change icon as needed
order: 1  # Position of the tab
title: PHP
permalink: /php/
entries_layout: list
pagination:
  enabled: true
  category: php
  per_page: 10
---


{% assign php_posts = site.posts | where: "categories", "php" %}

<ul>
  {% for post in php_posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a> <small>({{ post.date | date: "%b %d, %Y" }})</small>
    </li>
  {% endfor %}
</ul>
