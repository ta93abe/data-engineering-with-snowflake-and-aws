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


## AWS

### Step Functions

- サーバーレスワークフロー
- Workflow Studio による視覚的な設計
- リトライ・エラーハンドリング機能
- dbt とかも動かせる

### Amazon Managed Workflows for Apache Airflow (MWAA)

- フルマネージド Apache Airflow
- Python で DAG を柔軟に記述
- 自動スケーリング対応
- Airflow エコシステムをそのまま活用

<style>
h2 {
  margin-bottom: 1rem;
}
h3 {
    margin-block: 1rem;
}
</style>

---

## Snowflake

### Task

- Snowflake ネイティブのスケジューラー
- SQL でワークフロー定義
- 他ツール不要のシンプルさ
- 結構大変だと思う。

<style>
h2 {
  margin-bottom: 1rem;
}
h3 {
    margin-block: 1rem;
}
</style>

---

## Managed Services

- **TROCCO** - データ統合プラットフォーム
- **Apache Airflow** - 最も有名なワークフローエンジン
- **Dagster** - データアセット中心の設計
- **Prefect** - モダンなPythonワークフロー
- **Kestra** - 宣言的ワークフロー

<style>
h2 {
  margin-bottom: 1rem;
}
</style>
