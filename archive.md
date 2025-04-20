---
layout: page
title: archive
permalink: /archive/
---

# 🗂️ Post Archive

A chronological list of all posts on mnote.

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
      <small>({{ post.date | date: "%Y-%m-%d" }})</small>
    </li>
  {% endfor %}
</ul>