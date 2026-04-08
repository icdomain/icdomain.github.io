---
layout: default
title: ICD観光
description: Independent Compute Domain の観光案内ページ
permalink: /ja/tourism/
lang: ja
alt_lang_url: /en/tourism/
date: 2026-04-08
last_modified_at: 2026-04-08
author: founder
---

# ICD観光

ICDの観光名所と訪問情報。

## 最新の観光記事

{% assign tourism_posts = site.posts | where: "lang", "ja" | sort: "date" | reverse %}
{% assign count = 0 %}
{% for post in tourism_posts %}
  {% if post.categories contains "tourism" and count < 3 %}
- [{{ post.title }}]({{ post.url }}) <time>{{ post.date | date: "%Y-%m-%d" }}</time>
  {{ post.description }}
    {% assign count = count | plus: 1 %}
  {% endif %}
{% endfor %}

[観光記事をすべて見る → アーカイブ](/ja/archives/)
