---
name: Docker
description: コンテナ仮想化プラットフォーム。アプリケーションを軽量なコンテナで実行・デプロイ
category: 
tags: []
---

# Docker

コンテナ仮想化プラットフォーム。アプリケーションを軽量なコンテナで実行・デプロイ

## インストール

```bash
# macOS
brew install docker

# Ubuntu
sudo apt-get install docker.io
```

## 使用例

```bash
# イメージビルド
docker build -t myapp .

# コンテナ起動
docker run -p 3000:3000 myapp

# コンテナ一覧
docker ps

# イメージ一覧
docker images

# Docker Compose起動
docker-compose up -d
```
