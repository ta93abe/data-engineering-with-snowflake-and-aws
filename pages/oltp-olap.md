---
transition: slide-up
layout: section
---

# OLTP と OLAP

<style>
h1 {
    color: #ffffff;
}
</style>

---

## 世の中には2つのデータベースがある(+α)

- **OLTP (Online Transaction Processing)**
  - 日常的な取引処理
  - 高い同時実行性が求められる
  - 正規化されたスキーマ

- **OLAP (Online Analytical Processing)**
  - 分析・集計処理
  - 大量データの読み取りに最適化
  - 非正規化・スタースキーマ

- **HTAP (Hybrid Transactional/Analytical Processing)**
  - OLTP と OLAP の両方を1つのシステムで実現
