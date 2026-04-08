---
layout: default
title: ICDの歴史
description: Independent Compute Domain の沿革と歴史的記録
permalink: /ja/history/
lang: ja
alt_lang_url: /en/history/
date: 2026-04-08
last_modified_at: 2026-04-08
author: founder
---

# ICDの歴史

ICDの建国から現在に至るまでの歩み。

## 最新の歴史記事

{% assign history_posts = site.posts | where: "lang", "ja" | sort: "date" | reverse %}
{% assign count = 0 %}
{% for post in history_posts %}
  {% if post.categories contains "history" and count < 3 %}
- [{{ post.title }}]({{ post.url }}) <time>{{ post.date | date: "%Y-%m-%d" }}</time>
  {{ post.description }}
    {% assign count = count | plus: 1 %}
  {% endif %}
{% endfor %}

[歴史記事をすべて見る → アーカイブ](/ja/archives/)
