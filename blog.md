---
layout: default
title: Blog
permalink: /blog/
---

# Blog

Thoughts on statistics, machine learning, and other things.

[← Home]({{ '/' | relative_url }})

{% for post in site.posts %}
## [{{ post.title }}]({{ post.url | relative_url }})

{{ post.date | date: "%-d %B %Y" }}

{{ post.excerpt }}

[Read more →]({{ post.url | relative_url }})

{% endfor %}
