---
transition: slide-up
layout: section
---

# AI と機械学習

<style>
h1 {
    color: #ffffff;
}
</style>

---
layout: image-right
image: /snowflake-cortex.png
backgroundSize: contain
---

## Snowflake Cortex

AI/ML機能を統合したプラットフォーム

- LLM関数群の提供
- ベクトル検索・RAG対応
- SQLベースのAI機能

---

## AISQL

Snowflake 標準 SQL で使える関数群

- ai_complete
- ai_extract
- ai_agg
- join on ai_filter
- ai_filter
- ai_classify

例えばこんな感じ

````md magic-move
```sql
select *
from my_table
```
```sql
select *
from my_table
where ai_filter(prompt('Find rows where the description indicates a positive sentiment'))
```
````

<v-click>
もはや黒魔術🪄
</v-click>

---

## Snowflake Intelligence

### Semantic View

- これからのデータエンジニアリングで非常に重要な概念
- ビジネス定義の標準化
- 人間が SQL を介さずに必要なデータを取得できるようにする
- AI もこれを読むイメージ

<div v-click class="mt-4">
参考: <a href="https://www.snowflake.com/ja/blog/open-semantic-interchange-ai-standard/" target="_blank">Open Semantic Interchange</a>
</div>

<style>
h2 {
    margin-bottom: 1rem;
}
h3 {
    margin-bottom: 1rem;
}
</style>


---

## Snowpark ML

- **ANOMALY_DETECTION**: 異常検知（不正検知、システム監視）
- **CLASSIFICATION**: 分類モデル（顧客セグメント、チャーン予測）
- **FORECAST**: 時系列予測（需要予測、売上予測）

データの移動なしでモデル構築が可能

```sql
CREATE OR REPLACE SNOWFLAKE.ML.FORECAST sales_forecast(
  INPUT_DATA => SYSTEM$REFERENCE('TABLE', 'sales_data'),
  TIMESTAMP_COLNAME => 'date',
  TARGET_COLNAME => 'amount'
);
```

<style>
h2 {
    margin-bottom: 1rem;
}
h3 {
    margin-bottom: 1rem;
}
</style>

---

## AWS での ML/AI ワークロード

### SageMaker

- **モデル開発**: Jupyter Notebook 環境での実験・開発
- **AutoML**: SageMaker Autopilot による自動モデル選択・チューニング
- **モデルトレーニング**: 分散学習、スポットインスタンス活用
- **モデルデプロイ**: リアルタイム推論エンドポイント、バッチ変換

<style>
h2 {
    margin-bottom: 1rem;
}
h3 {
    margin-bottom: 1rem;
}
</style>

---

## AWS の AI サービス

- **Amazon Bedrock**: 基盤モデル(Claude, Llama等)の利用
- **Amazon Comprehend**: 自然言語処理（感情分析、エンティティ抽出）
- **Amazon Rekognition**: 画像・動画分析
- **Amazon Textract**: ドキュメントからのテキスト抽出

<style>
h2 {
    margin-bottom: 1rem;
}
h3 {
    margin-bottom: 1rem;
}
</style>

---

## ユースケース別の選択

| ワークロード | AWS | Snowflake |
|------------|-----|-----------|
| 構造化データの予測 | SageMaker | Snowpark ML ⭐ |
| カスタムディープラーニング | SageMaker ⭐ | - |
| LLM アプリケーション | Bedrock ⭐ | Cortex ⭐ |
| 画像・動画分析 | Rekognition ⭐ | - |
| SQL ベースの AI | - | Cortex ⭐ |
| データ統合型 ML | - | Snowpark ML ⭐ |

<style>
h2 {
    margin-bottom: 1rem;
}
h3 {
    margin-bottom: 1rem;
}
</style>