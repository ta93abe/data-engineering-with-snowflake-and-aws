---
transition: slide-up
layout: section
---

# dbt については語りたい

---

## データエンジニアリングの世界に<br>ソフトウェアエンジニアリングがやってきた

---

### Version Control



- Git で dbt のプロジェクトを管理
- Snowflake のワークシートは散らかりがち
- データ変換のロジック、ドキュメントの一元管理



---

### Testing

---

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

---

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

---

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

---

### CI/CD

```bash
dbt build --target prod
```

- Git push → 自動テスト・デプロイ
- 本番環境への安全なリリース

---

### Documentation

- YAML でカラムに説明が書ける
- 自動生成されるドキュメント
- **リネージュ** - データの血統管理

<img src="/dbt-docs.png" class="mx-auto" />
