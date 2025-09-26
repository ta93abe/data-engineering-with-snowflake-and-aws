---
transition: slide-up
layout: section
---

# Workflow Orchestration

---

## 概論

<v-clicks>

- データパイプラインのスケジューリング
- 依存関係の管理
- エラーハンドリング・リトライ

</v-clicks>

---

## Step Functions

<v-clicks>

- AWSのサーバーレスワークフロー
- 視覚的なワークフロー定義
- 他のAWSサービスとの連携

</v-clicks>

---

## Amazon Managed Workflows for Apache Airflow

<v-clicks>

- フルマネージドAirflow
- dbtとの連携サンプル有り

</v-clicks>

<div v-click class="mt-4">
参考：<a href="https://docs.aws.amazon.com/ja_jp/mwaa/latest/userguide/samples-dbt.html" target="_blank">AWS dbt サンプル</a>
</div>

---

## Snowflake Task

<v-clicks>

- Snowflake ネイティブのスケジューラー
- SQL でワークフロー定義
- 他ツール不要のシンプルさ

</v-clicks>

---

## Managed Services

<v-clicks>

- **Airflow** - 最も有名なワークフローエンジン
- **Prefect** - モダンなPythonワークフロー
- **TROCCO** - データ統合プラットフォーム
- **Dagster** - データアセット中心の設計
- **Kestra** - 宣言的ワークフロー

</v-clicks>