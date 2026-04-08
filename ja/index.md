---
layout: default
title: home
---

# Welcome to Independent State Of Luminarch
Luminarch is a micronation within a computer.

## news

{% assign news_posts = site.posts | where_exp: "post", "post.categories.size == 0" | limit: 5 %}
{% for post in news_posts %}
- **{{ post.date | date: "%m/%d" }}** [{{ post.title }}]({{ post.url | relative_url }})
{% endfor %}

{% if news_posts.size == 0 %}
There are no announcements at this time.
{% endif %}
