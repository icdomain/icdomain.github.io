---
layout: default
title: 公文書館
description: Independent Compute Domain の公文書館 (公式記録および布告)
permalink: /ja/official-records/
lang: ja
alt_lang_url: /en/official-records/
date: 2026-04-08
last_modified_at: 2026-04-08
author: founder
---

# 公文書館

ICDの公式布告、決定、記録文書。

## 最新の公文書

{% assign official_posts = site.posts | where: "lang", "ja" | sort: "date" | reverse %}
{% assign count = 0 %}
{% for post in official_posts %}
  {% if post.categories contains "official-records" and count < 3 %}
- [{{ post.title }}]({{ post.url }}) <time>{{ post.date | date: "%Y-%m-%d" }}</time>
  {{ post.description }}
    {% assign count = count | plus: 1 %}
  {% endif %}
{% endfor %}

[公文書をすべて見る → アーカイブ](/ja/archives/)
