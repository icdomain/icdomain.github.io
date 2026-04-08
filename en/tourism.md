---
layout: default
title: ICD Tourism
description: Tourism information for the Independent Compute Domain
permalink: /en/tourism/
lang: en
alt_lang_url: /ja/tourism/
date: 2026-04-08
last_modified_at: 2026-04-08
author: founder
---

# ICD Tourism

Sights and visitor information for the Independent Compute Domain.

## Latest tourism posts

{% assign tourism_posts = site.posts | where: "lang", "en" | sort: "date" | reverse %}
{% assign count = 0 %}
{% for post in tourism_posts %}
  {% if post.categories contains "tourism" and count < 3 %}
- [{{ post.title }}]({{ post.url }}) <time>{{ post.date | date: "%Y-%m-%d" }}</time>
  {{ post.description }}
    {% assign count = count | plus: 1 %}
  {% endif %}
{% endfor %}

[See all tourism posts → Archives](/en/archives/)
