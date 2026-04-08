---
layout: default
title: Independent Compute Domain
description: Independent Compute Domain 公式サイト
permalink: /ja/
lang: ja
alt_lang_url: /en/
date: 2026-04-08
last_modified_at: 2026-04-08
author: founder
---

# Independent Compute Domain

ICD公式サイトへようこそ。

## セクション

- [観光](/ja/tourism/)
- [歴史](/ja/history/)
- [公式記録](/ja/official-records/)
- [開発者ブログ](/ja/developer-blog/)
- [アーカイブ](/ja/archives/)

## 最新の記事

{% assign latest = site.posts | where: "lang", "ja" | sort: "date" | reverse %}
{% for post in latest limit:5 %}
- [{{ post.title }}]({{ post.url }}) <time>{{ post.date | date: "%Y-%m-%d" }}</time>
{% endfor %}
