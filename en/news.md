---
layout: default
title: News
description: Daily AI intelligence digest collected automatically every morning by the Independent Compute Domain
permalink: /en/news/
lang: en
alt_lang_url: /ja/news/
date: 2026-10-25
last_modified_at: 2026-10-25
author: founder
---

# News

A daily digest of official AI announcements, releases and community reaction, collected and selected every morning by deterministic scripts. The LLM writes only the introduction and a one-line note per item; readers verify linked content themselves.

## Latest Digests

{% assign news_posts = site.posts | where: "lang", "en" | sort: "date" | reverse %}
{% assign count = 0 %}
{% for post in news_posts %}
  {% if post.categories contains "news" and count < 7 %}
- [{{ post.title }}]({{ post.url }}) <time>{{ post.date | date: "%Y-%m-%d" }}</time>
  {{ post.description }}
    {% assign count = count | plus: 1 %}
  {% endif %}
{% endfor %}

[See all → Archives](/en/archives/)
