---
layout: single 
title: "LARS"
author_profile: true 
---
Excerpt

{% assign lars_projects = site.posts | where_exp:"post","post.tags contains 'LARS'" %}
{% for project in lars_projects %}
### [{{ project.title }}]({{ project.url }})
{{ project.excerpt }}
{% endfor %}

