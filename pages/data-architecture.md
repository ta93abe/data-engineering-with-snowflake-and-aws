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

- Snowflake リソースの管理
- Terraform と使い分けるはず

---

## Apache Iceberg

オープンテーブル形式でデータレイクの課題を解決

- **ACID トランザクション**: データレイクでも確実なトランザクション処理を実現
- **スキーマ進化**: カラムの追加・削除・変更を柔軟にサポート
- **タイムトラベル**: 過去の任意の時点のデータにアクセス可能
- **パーティション進化**: データを再書き込みせずにパーティション変更が可能
- **Hidden Partitioning**: ユーザーはパーティションを意識せずにクエリ可能
- **マルチエンジン対応**: Snowflake、Spark、Trino、Flink など複数のエンジンで利用可能

---

## S3 がやっぱり大切だと思う

- 事実上の標準ストレージ
- コスト効率
- 耐久性・可用性
- S3 Tables も期待大

---

## Data Sharing

- Snowflakeのキラー機能
- データのコピー不要
- リアルタイム共有
