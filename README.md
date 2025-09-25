# Snowflake と AWS で始めるデータエンジニアリング

## OLTP と OLAP

## データエンジニアというお仕事

https://komi.theletter.jp/posts/e4790bf0-fb84-11ee-9b01-3da9ec89ce20

## データエンジニアの道具

### SQL

### Python

## なぜ Snowflake を使いたくなるのか

### 単一プラットフォーム

### Snowflake Marketplace

### Streamlit in Snowflake

### Snowpark Container Services

### Snow CLI

### DB Engine

## Data Ingestion

### 概論

### AWS Glue

### Snowpipe

### Managed Services

#### Fivetran

#### TROCCO

#### Airbyte

#### dlt

#### CData

## dbt については語りたい

### データエンジニアリングの世界にソフトウェアエンジニアリングがやってきた。

#### Version Management

Git で dbt のプロジェクトを管理する。
例えば Snowflake にワークシートという SQL ファイルを扱えるが、どうしても散らかってしまう(Git統合も最近できるようになった)
データ変換のロジック、ドキュメント

#### Testing

##### Generic Test

YAML にサクッと書ける。

##### Singular Test

##### Unit Test

#### CI/CD

```bash
dbt build --target prod
```

#### Documentation

YAML でカラムに説明が書ける。

リネージュ

## Workflow Orchestration

### 概論

### Step Functions

### Amazon Managed Workflows for Apache Airflow

https://docs.aws.amazon.com/ja_jp/mwaa/latest/userguide/samples-dbt.html

### Snowflake Task

### Managed Services

#### Airflow

#### TROCCO

#### Dagster

#### Kestra

## 中央集権データ基盤と分散データ基盤

### Iceberg

### S3 がやっぱり大切

### Data Sharing

### データメッシュ

## 機械学習のプラットフォームを選ぶ

### AWS でやる。

### Snowflake でやる。

## 一応 AI 関連の機能

### AISQL

### Snowflake Intelligence

#### Semantic View

https://www.snowflake.com/ja/blog/open-semantic-interchange-ai-standard/
