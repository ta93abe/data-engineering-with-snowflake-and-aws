---
transition: slide-up
layout: section
---

# なぜ Snowflake を<br>使いたくなるのか

<style>
h1 {
    color: #ffffff;
}
</style>

---
layout: two-cols
---

<template v-slot:default>

## Snowflake と AWS の関係

- Snowflake は AWS, Azure, Google Cloud のマルチクラウド対応
    - アカウントを作るときにどこに作るか選べる
- AWS は Snowflake のカンファレンスにスポンサーとして参加
- Snowflake は AWS のサービスと連携可能

</template>
<template v-slot:right>

<img src="/swtt-overview.png" alt="Snowflake World Tour Tokyo 2024" class="w-96 ml-4">
<img src="/swtt-double-black-diamond.png" alt="Snowflake World Tour Tokyo 2024 Sponsors" class="w-96 ml-4">

</template>

<style>
h2 {
    margin-bottom: 1rem;
}
</style>

---
layout: two-cols
---

<template v-slot:default>
<img src="/db-ranking.png" alt="DB Engine Ranking" class="w-84" />
</template>
<template v-slot:right>
<img src="/db-ranking-chart.png" alt="DB Engine Ranking Chart" class="w-84" />
</template>


---
layout: two-cols
---

<template v-slot:default>

## 単一プラットフォーム

- プラットフォーム
- アナリティクス
- AI
- データエンジニアリング
- アプリケーションとコラボレーション

すべてが一つのプラットフォームで完結

</template>

<template v-slot:right>

<img src="/data-ai-platform.png" alt="Data & AI Platform" class="w-128">

</template>

<style>
h2 {
    margin-bottom: 1rem;
}
</style>

---

## Snow CLI

- コマンドラインでの操作
- CI/CDパイプラインとの統合
- さまざまなオブジェクトが管理できる
    - Snowflake Native Apps
    - Snowflake Cortex
    - Snowflake Git Integration
    - Snowflake Notebook
    - Snowflake Warehouse
    - Snowflake Stage
    - Snowpark
    - Snowflake Container Services
    - Streamlit in Snowflake

<a href="Snowflake CLI" target="_blank">Snowflake CLI | Snowflake Documentation</a>

<style>
h2 {
    margin-bottom: 1rem;
}
</style>

---

## Snowflake Marketplace

- サードパーティデータを簡単に利用できる
    - 企業情報
    - 地理空間データ
    - 気象データ
- データ共有の仕組み
- Internal Marketplace
    - 限定的なアカウント同士でデータやアプリケーションを共有できる

<style>
h2 {
    margin-bottom: 1rem;
}
</style>


---

## Streamlit in Snowflake

- Python で Web アプリが書ける
- Snowflake 内でデプロイできる
- 認証どうしよう問題がない
- もちろん Snow CLI 越しにもデプロイ可能、Git でも管理できる

<img src="/streamlit.png" class="mx-auto mt-12" />

<style>
h2 {
    margin-bottom: 1rem;
}
</style>

---

## Snowflake Notebook

- Jupyter的な環境
- Snowflake内で実行
- データ分析・探索に最適
- スケジュール実行も可能
- Python, SQL, Markdown が使える
- Streamlit も動く

<style>
h2 {
    margin-bottom: 1rem;
}
</style>

---

## Snowpark Container Services

- コンテナベースのワークロード
- 機械学習モデルのデプロイ
- カスタムアプリケーションの実行

<style>
h2 {
    margin-bottom: 1rem;
}
</style>
