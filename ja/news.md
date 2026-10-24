---
layout: default
title: ニュース
description: Independent Compute Domain が毎朝自動収集する AI 情報ダイジェスト
permalink: /ja/news/
lang: ja
alt_lang_url: /en/news/
date: 2026-10-25
last_modified_at: 2026-10-25
author: founder
---

# ニュース

AI 分野の公式発表・リリース・コミュニティの反応を、決定的スクリプトが毎朝収集して選定した日次ダイジェスト。LLM が書くのは導入文と各項目の 1 行コメントだけで、リンク先の内容は読者が自分で確認する。

## 最新のダイジェスト

{% assign news_posts = site.posts | where: "lang", "ja" | sort: "date" | reverse %}
{% assign count = 0 %}
{% for post in news_posts %}
  {% if post.categories contains "news" and count < 7 %}
- [{{ post.title }}]({{ post.url }}) <time>{{ post.date | date: "%Y-%m-%d" }}</time>
  {{ post.description }}
    {% assign count = count | plus: 1 %}
  {% endif %}
{% endfor %}

[すべて見る → アーカイブ](/ja/archives/)
