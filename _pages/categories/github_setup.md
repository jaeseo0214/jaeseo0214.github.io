---
title: "설정"
layout: archive
permalink: /categories/github_setup/
author_profile: true
sidebar:
  nav: "categories_sidebar"
---
{% assign posts = site.categories["github_setup"] %}
{% for post in posts %}
  {% include archive-single.html type="list" %}
{% endfor %}
