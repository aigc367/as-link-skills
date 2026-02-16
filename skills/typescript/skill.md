---
name: TypeScript
description: JavaScriptに型システムを追加したプログラミング言語。型安全性とIDEサポートを向上
category: 
tags: []
---

# TypeScript

JavaScriptに型システムを追加したプログラミング言語。型安全性とIDEサポートを向上

## インストール

```bash
npm install -D typescript @types/node
```

## 使用例

```bash
# tsconfig.json生成
npx tsc --init

# TypeScriptコンパイル（全ファイル）
npx tsc

# 特定ファイルをコンパイル
npx tsc src/index.ts

# Watch モード
npx tsc --watch

# TypeScriptファイルを直接実行（tsx使用）
npx tsx src/script.ts
```
