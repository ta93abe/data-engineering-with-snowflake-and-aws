---
transition: slide-up
layout: section
---

# Workflow Orchestration

<style>
h1 {
    color: #ffffff;
}
</style>

---

## 概論

- データパイプラインのスケジューリング
- 依存関係の管理 (DAG)
- エラーハンドリング・リトライ

<!-- DAG とはノードが循環をせずに一方向の接続によってリンクされているグラフ -->

---

## Step Functions

- AWSのサーバーレスワークフロー
- 視覚的なワークフロー定義
- 他のAWSサービスとの連携

---

## Amazon Managed Workflows for Apache Airflow

- フルマネージドAirflow

---

## Snowflake Task

- Snowflake ネイティブのスケジューラー
- SQL でワークフロー定義
- 他ツール不要のシンプルさ
- 結構大変だと思う。

---

## Managed Services

- **TROCCO** - データ統合プラットフォーム
- **Apache Airflow** - 最も有名なワークフローエンジン
- **Dagster** - データアセット中心の設計
- **Prefect** - モダンなPythonワークフロー
- **Kestra** - 宣言的ワークフロー
