---
layout: home
title: Welcome to My Site
permalink: /
---

# Welcome to {{ site.title }}

{{ site.description }}

[Explore Blog](/blog/) | [Learn More About Me](/about/)

---

## Latest Posts

{% for post in site.posts limit:3 %}
- **[{{ post.title }}]({{ post.url }})**  
  {{ post.excerpt | strip_html | truncatewords: 30 }}
{% endfor %}
