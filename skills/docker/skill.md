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
# macOS (Docker Desktop)
brew install --cask docker

# Ubuntu/Debian
sudo apt-get update
sudo apt-get install docker.io docker-compose

# インストール確認
docker --version
docker-compose --version
```

## 使用例

```bash
# Dockerfileからイメージビルド
docker build -t myapp:latest .

# コンテナ起動
docker run -d -p 3000:3000 --name myapp myapp:latest

# 起動中のコンテナ一覧
docker ps

# 全てのコンテナ一覧（停止中含む）
docker ps -a

# イメージ一覧
docker images

# コンテナのログ確認
docker logs myapp

# コンテナに入る
docker exec -it myapp /bin/bash

# コンテナ停止
docker stop myapp

# コンテナ削除
docker rm myapp

# Docker Compose起動
docker-compose up -d

# Docker Compose停止
docker-compose down
```
