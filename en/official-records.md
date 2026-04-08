---
layout: default
title: Official Records
description: Official records and decrees of the Independent Compute Domain
permalink: /en/official-records/
lang: en
alt_lang_url: /ja/official-records/
date: 2026-04-08
last_modified_at: 2026-04-08
author: founder
---

# Official Records

Official decrees, decisions, and documents of the ICD.

## Latest official records

{% assign official_posts = site.posts | where: "lang", "en" | sort: "date" | reverse %}
{% assign count = 0 %}
{% for post in official_posts %}
  {% if post.categories contains "official-records" and count < 3 %}
- [{{ post.title }}]({{ post.url }}) <time>{{ post.date | date: "%Y-%m-%d" }}</time>
  {{ post.description }}
    {% assign count = count | plus: 1 %}
  {% endif %}
{% endfor %}

[See all official records → Archives](/en/archives/)
