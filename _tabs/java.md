---
# layout: home
icon: fas fa-mug-hot  # Change icon as needed
order: 2  # Position of the tab (adjust as needed)
title: Java
permalink: /java/
entries_layout: list
pagination:
  enabled: true
  category: java
  per_page: 10
---

{% assign java_posts = site.posts | where: "categories", "java" %}

<ul>
  {% for post in java_posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a> <small>({{ post.date | date: "%b %d, %Y" }})</small>
    </li>
  {% endfor %}
</ul>
