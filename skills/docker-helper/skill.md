---
name: Docker Helper
description: Dockerコンテナとイメージを管理するためのヘルパースキル
category: f12ba5e0-1e1d-43e5-afca-d58136cadb9c
tags: []
---

# Docker Helper

Dockerコンテナとイメージを管理するためのヘルパースキル

## インストール

```bash
curl -o ~/.claude/skills/docker-helper/SKILL.md https://raw.githubusercontent.com/aigc367/as-link-skills/main/skills/docker-helper/skill.md
```

## 使用例

```bash
# コンテナ一覧を表示
docker-helper ps

# イメージをクリーンアップ
docker-helper cleanup

# コンテナログを表示
docker-helper logs <container-name>
```
