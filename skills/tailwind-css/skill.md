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
# Tailwind設定ファイル生成
npx tailwindcss init

# CSSビルド（開発時）
npx tailwindcss -i ./src/input.css -o ./dist/output.css --watch

# CSSビルド（本番）
npx tailwindcss -i ./src/input.css -o ./dist/output.css --minify
```
