---
transition: slide-up
layout: section
---

# Workflow Orchestration

---

## 概論

- データパイプラインのスケジューリング
- 依存関係の管理
- エラーハンドリング・リトライ

---

## Step Functions

- AWSのサーバーレスワークフロー
- 視覚的なワークフロー定義
- 他のAWSサービスとの連携

---

## Amazon Managed Workflows for Apache Airflow

- フルマネージドAirflow
- dbtとの連携サンプル有り

<div v-click class="mt-4">
参考：<a href="https://docs.aws.amazon.com/ja_jp/mwaa/latest/userguide/samples-dbt.html" target="_blank">AWS dbt サンプル</a>
</div>

---

## Snowflake Task

- Snowflake ネイティブのスケジューラー
- SQL でワークフロー定義
- 他ツール不要のシンプルさ

---

## Managed Services

- **TROCCO** - データ統合プラットフォーム
- **Airflow** - 最も有名なワークフローエンジン
- **Dagster** - データアセット中心の設計
- **Prefect** - モダンなPythonワークフロー
- **Kestra** - 宣言的ワークフロー
