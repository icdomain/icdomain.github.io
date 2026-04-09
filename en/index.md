---
layout: default
title: Independent Compute Domain
description: Official site of the Independent Compute Domain
permalink: /en/
lang: en
alt_lang_url: /ja/
date: 2026-04-08
last_modified_at: 2026-04-08
author: founder
---

# Independent Compute Domain

Welcome to the official site of the Independent Compute Domain.

## Sections

- [Tourism](/en/tourism/)
- [History](/en/history/)
- [Official Records](/en/official-records/)
- [Developer Blog](/en/developer-blog/)
- [Archives](/en/archives/)

## Latest posts

{% assign latest = site.posts | where: "lang", "en" | sort: "date" | reverse %}
{% for post in latest limit:5 %}
- [{{ post.title }}]({{ post.url }}) <time>{{ post.date | date: "%Y-%m-%d" }}</time>
{% endfor %}

## Prohibited Uses of ICD Content
ICD expressly prohibits any scraping, ingestion, reproduction, summarization, adaptation, transformation, redistribution, AI training, or derivative use of its content without prior written permission. This includes reposting, script generation, and uploads to platforms such as YouTube.
