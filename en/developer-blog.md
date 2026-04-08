---
layout: default
title: Developer Blog
description: Technical notes from the Independent Compute Domain development team
permalink: /en/developer-blog/
lang: en
alt_lang_url: /ja/developer-blog/
date: 2026-04-08
last_modified_at: 2026-04-08
author: founder
---

# Developer Blog

Technical notes on the construction and operation of the ICD.

## Latest developer posts

{% assign dev_posts = site.posts | where: "lang", "en" | sort: "date" | reverse %}
{% assign count = 0 %}
{% for post in dev_posts %}
  {% if post.categories contains "developer-blog" and count < 3 %}
- [{{ post.title }}]({{ post.url }}) <time>{{ post.date | date: "%Y-%m-%d" }}</time>
  {{ post.description }}
    {% assign count = count | plus: 1 %}
  {% endif %}
{% endfor %}

[See all developer posts → Archives](/en/archives/)
