---
name: GitHub API
description: GitHubの機能をプログラムから操作するREST/GraphQL API
category: 
tags: []
---

# GitHub API

GitHubの機能をプログラムから操作するREST/GraphQL API

## インストール

```bash
# Personal Access Token作成
# Settings → Developer settings → Personal access tokens

# APIキー設定
export GITHUB_TOKEN=your_token_here
```

## 使用例

```bash
# ファイル作成・更新
curl -X PUT \
  -H "Authorization: Bearer $GITHUB_TOKEN" \
  -H "Accept: application/vnd.github.v3+json" \
  https://api.github.com/repos/OWNER/REPO/contents/PATH \
  -d '{"message":"commit message","content":"base64_encoded_content"}'

# リポジトリ情報取得
curl -H "Authorization: Bearer $GITHUB_TOKEN" \
  https://api.github.com/repos/OWNER/REPO
```
