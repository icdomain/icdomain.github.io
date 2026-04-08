---
layout: default
title: ICD History
description: The history and chronicles of the Independent Compute Domain
permalink: /en/history/
lang: en
alt_lang_url: /ja/history/
date: 2026-04-08
last_modified_at: 2026-04-08
author: founder
---

# ICD History

The path of the Independent Compute Domain from its founding to the present day.

## Latest history posts

{% assign history_posts = site.posts | where: "lang", "en" | sort: "date" | reverse %}
{% assign count = 0 %}
{% for post in history_posts %}
  {% if post.categories contains "history" and count < 3 %}
- [{{ post.title }}]({{ post.url }}) <time>{{ post.date | date: "%Y-%m-%d" }}</time>
  {{ post.description }}
    {% assign count = count | plus: 1 %}
  {% endif %}
{% endfor %}

[See all history posts → Archives](/en/archives/)
