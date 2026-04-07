---
layout: default
title: Official Records
permalink: /official-records/
---

# Official Records
This section publishes formal decisions, declarations, and administrative records.

{% assign official_records_posts = site.posts | where_exp: "post", "post.categories contains 'official-records'" %}

{% if official_records_posts.size > 0 %}
## Posts

{% for post in official_records_posts %}
- [{{ post.title }}]({{ post.url | relative_url }}) - {{ post.date | date: "%Y-%m-%d" }}
{% endfor %}
{% else %}
There are no official records at this time.
{% endif %}
