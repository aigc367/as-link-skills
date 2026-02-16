---
name: Tailwind CSS
description: ユーティリティファーストのCSSフレームワーク。クラス名でスタイリングを素早く実装
category: 
tags: []
---

# Tailwind CSS

ユーティリティファーストのCSSフレームワーク。クラス名でスタイリングを素早く実装

## インストール

```bash
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p
```

## 使用例

```bash
# tailwind.config.jsとpostcss.config.js生成
npx tailwindcss init -p

# CSSファイルに追加
# @tailwind base;
# @tailwind components;
# @tailwind utilities;

# ビルド（開発モード・Watch）
npx tailwindcss -i ./src/input.css -o ./dist/output.css --watch

# ビルド（本番・圧縮）
npx tailwindcss -i ./src/input.css -o ./dist/output.css --minify
```
