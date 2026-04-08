---
layout: default
title: 開発者ブログ
description: Independent Compute Domain 開発チームによる技術記録
permalink: /ja/developer-blog/
lang: ja
alt_lang_url: /en/developer-blog/
date: 2026-04-08
last_modified_at: 2026-04-08
author: founder
---

# 開発者ブログ

ICDの構築・運営に関する技術記録。

## 最新の開発記事

{% assign dev_posts = site.posts | where: "lang", "ja" | sort: "date" | reverse %}
{% assign count = 0 %}
{% for post in dev_posts %}
  {% if post.categories contains "developer-blog" and count < 3 %}
- [{{ post.title }}]({{ post.url }}) <time>{{ post.date | date: "%Y-%m-%d" }}</time>
  {{ post.description }}
    {% assign count = count | plus: 1 %}
  {% endif %}
{% endfor %}

[開発記事をすべて見る → アーカイブ](/ja/archives/)
