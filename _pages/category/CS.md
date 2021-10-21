---
title: "Computer Science"
layout: category
permalink: /categories/cs/
author_profile: true
taxonomy: CS
---

{% assign posts = site.categories.CS %}
{% for post in posts %} {% include archive-single.html type=page.entries_layout %} {% endfor %}
