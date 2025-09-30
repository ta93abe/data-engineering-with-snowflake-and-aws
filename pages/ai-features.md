---
transition: slide-up
layout: section
---

# AI 関連の機能

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


---

## AISQL

Snowflake 標準 SQL で使える関数群

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
