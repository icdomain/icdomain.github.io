---
layout: post
title: "開発者ブログスタート & Jekyll ダークモード実装"
date: 2025-01-23 15:00:00 +0900
categories: [dev-blog]
excerpt: "開発者ブログを開設しました。最初の記事として、サイトにダークモードを実装した過程を記録します。"
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
