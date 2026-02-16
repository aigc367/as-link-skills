---
name: Supabase
description: オープンソースのFirebase代替。PostgreSQLデータベース、認証、ストレージ、リアルタイム機能を提供
category: 
tags: []
---

# Supabase

オープンソースのFirebase代替。PostgreSQLデータベース、認証、ストレージ、リアルタイム機能を提供

## インストール

```bash
npm install @supabase/supabase-js
```

## 使用例

```bash
# Supabaseクライアント初期化
import { createClient } from '@supabase/supabase-js'
const supabase = createClient(SUPABASE_URL, SUPABASE_ANON_KEY)

# データ取得
const { data, error } = await supabase.from('table').select('*')

# データ挿入
const { data, error } = await supabase.from('table').insert({ column: 'value' })
```
