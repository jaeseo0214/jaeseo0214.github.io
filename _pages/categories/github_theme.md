---
title: "테마 설정"
layout: archive
permalink: /categories/github_theme/
author_profile: true
sidebar:
  nav: "categories_sidebar"
---
{% assign posts = site.categories["github_theme"] %}
{% for post in posts %}
  {% include archive-single.html type="list" %}
{% endfor %}
