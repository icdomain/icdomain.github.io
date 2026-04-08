---
layout: post
title: 記事タイトル
description: 記事の説明（120字以内）
permalink: /en/archives/2025/01/23/jekyll-darkmode-implementation/
lang: en
date: 2025-01-23T00:00:00Z
last_modified_at: 2025-01-23T00:00:00Z
author: founder
categories: [official-records]
tags: [TAG1, TAG2, TAG3]
---

# Jekyll でダークモード実装記録

GitHub Pages + Jekyll でダークモードを実装した際の技術メモです。単純な CSS だけでなく、ユーザー体験を重視した実装を心がけました。

## 実装の要件

- ✅ ブラウザの `prefers-color-scheme` 設定を自動検出
- ✅ 手動切り替えボタンの提供
- ✅ ユーザー設定の永続化（`localStorage`）
- ✅ ページ読み込み時のちらつき防止
- ✅ 既存のインラインスタイルと共存

## 技術的な実装ポイント

### 1. CSS変数によるテーマ管理

```css
:root {
  --bg-color: #ffffff;
  --text-color: #333333;
  --link-color: #0066cc;
  --border-color: #cccccc;
  --nav-hover: #f0f0f0;
}

[data-theme="dark"] {
  --bg-color: #1a1a1a;
  --text-color: #e0e0e0;
  --link-color: #66b3ff;
  --border-color: #444444;
  --nav-hover: #2a2a2a;
}

@media (prefers-color-scheme: dark) {
  :root:not([data-theme]) {
    --bg-color: #1a1a1a;
    --text-color: #e0e0e0;
    --link-color: #66b3ff;
    --border-color: #444444;
    --nav-hover: #2a2a2a;
  }
}
