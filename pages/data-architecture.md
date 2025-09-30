---
transition: slide-up
layout: section
---

# 中央集権データ基盤と分散データ基盤

<style>
h1 {
    color: #ffffff;
}
</style>

---

## とりあえず Terraform

- Infrastructure as Code
- 再現可能な環境構築
- チームでの管理
- Snowflake Provider もあるし、他のツールに関してもだいたい揃ってる

---

## Snowflake Data Project なんてのもある

- Snowflakeリソースの管理
- Terraform と使い分けるはず

---

## Apache Iceberg

- オープンテーブル形式
- データレイクの課題を解決
- ACID トランザクション対応

---

## S3 がやっぱり大切

- 事実上の標準ストレージ
- コスト効率
- 耐久性・可用性
- S3 Tables も期待大

---

## Data Sharing

- Snowflakeのキラー機能
- データのコピー不要
- リアルタイム共有
