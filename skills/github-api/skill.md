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
# 1. GitHub Settings → Developer settings → Personal access tokens → Generate new token
# 2. 必要な権限を選択（repo, workflow, admin:org など）
# 3. トークンを生成してコピー

# 環境変数に設定
export GITHUB_TOKEN="your_personal_access_token"
```

## 使用例

```bash
# リポジトリ情報取得
curl -H "Authorization: Bearer $GITHUB_TOKEN" \
  https://api.github.com/repos/OWNER/REPO

# ファイル内容取得
curl -H "Authorization: Bearer $GITHUB_TOKEN" \
  https://api.github.com/repos/OWNER/REPO/contents/PATH

# ファイル作成・更新
curl -X PUT \
  -H "Authorization: Bearer $GITHUB_TOKEN" \
  -H "Accept: application/vnd.github.v3+json" \
  https://api.github.com/repos/OWNER/REPO/contents/PATH \
  -d '{
    "message": "Add/Update file",
    "content": "'$(echo -n "file content" | base64)'",
    "sha": "existing_file_sha_if_updating"
  }'

# Issue作成
curl -X POST \
  -H "Authorization: Bearer $GITHUB_TOKEN" \
  -H "Accept: application/vnd.github.v3+json" \
  https://api.github.com/repos/OWNER/REPO/issues \
  -d '{"title":"Issue title","body":"Issue description"}'

# JavaScriptで使用（Octokit）
npm install @octokit/rest

# Octokitの使用例
import { Octokit } from '@octokit/rest'
const octokit = new Octokit({ auth: process.env.GITHUB_TOKEN })
const { data } = await octokit.repos.get({ owner: 'OWNER', repo: 'REPO' })
```
