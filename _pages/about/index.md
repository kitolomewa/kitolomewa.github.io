---
layout: content
title: Writing
permalink: /writing/
---

{% assign current_year = "" %}

{% for post in site.posts %}

{% assign post_year = post.date | date: "%Y" %}

{% if post_year != current_year %}
{% assign current_year = post_year %}

## {{ current_year }}

{% endif %}

### [{{ post.title }}]({{ post.url | relative_url }})

{{ post.description }}

{{ post.date | date: "%b %d, %Y" }}

{% endfor %}
