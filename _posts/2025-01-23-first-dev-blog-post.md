---
layout: post
title: Article Title
description: Article description (max 120 chars)
permalink: /en/archives/2025/01/23/first-dev-blog-post/
lang: en
date: 2025-01-23T00:00:00Z
last_modified_at: 2025-01-23T00:00:00Z
author: founder
categories: [official-records]
tags: [TAG1, TAG2, TAG3]
---

# 開発者ブログスタート！

Luminarch独立国の公式サイトに開発者ブログを開設しました 🎉

## 今回実装したもの

### 1. ダークモード機能
- ブラウザの `prefers-color-scheme` 設定を自動検出
- 手動切り替えボタン（☀️/🌙）
- `localStorage` で設定保存
- ちらつき防止の仕組み

### 2. ナビゲーション強化
- ホーム、開発者ブログ、歴史の3つのセクション
- アクティブページのハイライト
- レスポンシブデザイン

### 3. ブログシステム
- Jekyll標準のブログ機能
- カテゴリー別表示（`dev-blog` / `general`）
- タグ機能
- 記事の概要（excerpt）表示

## 技術的なポイント

### CSS変数でテーマ管理

```css
:root {
  --bg-color: #ffffff;
  --text-color: #333333;
  --link-color: #0066cc;
}

[data-theme="dark"] {
  --bg-color: #1a1a1a;
  --text-color: #e0e0e0;
  --link-color: #66b3ff;
}
