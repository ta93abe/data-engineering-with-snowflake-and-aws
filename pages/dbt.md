---
transition: slide-up
layout: section
---

# dbt について語りたい

---
layout: center
---

## データエンジニアリングの世界に<br>ソフトウェアエンジニアリングがやってきた

---

### Version Control

- Git で dbt のプロジェクトを管理
- Snowflake のワークシートは散らかりがち
- データ変換のロジック、ドキュメントの一元管理

<style>
h3 {
    margin-bottom: 1rem;
}
</style>

---

### Testing

#### Generic Test

- YAML にサクッと書ける
- 一意性、NULL チェック、参照整合性

```yaml
models:
  - name: customers
    columns:
      - name: customer_id
        tests:
          - unique
          - not_null
      - name: status
        tests:
          - accepted_values:
              values: ['active', 'inactive']
```

<style>
h4 {
    margin-bottom: 1rem;
}
</style>

---

### Testing

#### Singular Test

- カスタムSQLテスト

```sql
-- tests/assert_order_total_matches_line_items.sql
select
    order_id,
    order_total,
    calculated_total
from (
    select
        o.order_id,
        o.order_total,
        sum(oi.quantity * oi.unit_price) as calculated_total
    from {{ ref('orders') }} o
    left join {{ ref('order_items') }} oi
        on o.order_id = oi.order_id
    group by o.order_id, o.order_total
)
where abs(order_total - calculated_total) > 0.01
```

<style>
h4 {
    margin-bottom: 1rem;
}
</style>

<!-- このテストは 注文の合計金額の整合性 をチェックしています。 具体的には：
orders テーブルに保存されている order_total（注文合計額）
order_items テーブルから計算した calculated_total（各商品の数量×単価の合計）
この2つの金額が一致しているかを検証します。 where abs(order_total - calculated_total) > 0.01 で、差が0.01以上ある不整合なレコードを抽出します。テストが成功する（= 不整合なデータが0件）ことで、データの信頼性が保証されます。 -->

---

### Testing

#### Unit Test

- モデルの単体テスト
- データ変換ロジックの検証

```yaml
unit_tests:
  - name: test_customer_metrics_calculation
    model: customer_metrics
    given:
      - input: ref('customers')
        rows:
          - {customer_id: 1, email: "test@example.com"}
      - input: ref('orders')
        rows:
          - {order_id: 1, customer_id: 1, order_total: 100.00}
    expect:
      rows:
        - {customer_id: 1, total_orders: 1, total_spent: 100.00}
```

<style>
h4 {
    margin-bottom: 1rem;
}
</style>

---

### CI/CD

- Git push → 自動テスト・デプロイ
- 本番環境への安全なリリース
- dbt profile で環境切り替え
- dbt Cloud という SaaS を使うとサクッと作れる

```bash
dbt build --target prod
dbt build --target dev
dbt build --target ci
```

<style>
h3 {
    margin-bottom: 1rem;
}
</style>

---

### Documentation

- YAML でカラムに説明が書ける
- 自動生成されるドキュメント
- **リネージュ** - データの血統管理

<img src="/dbt-docs.png" class="mx-auto" />

<style>
h3 {
    margin-bottom: 1rem;
}
</style>