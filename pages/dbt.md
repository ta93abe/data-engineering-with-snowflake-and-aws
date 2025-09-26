---
transition: slide-up
layout: section
---

# dbt については語りたい

---

## データエンジニアリングの世界に<br>ソフトウェアエンジニアリングがやってきた

---

### Version Control

<v-clicks>

- Git で dbt のプロジェクトを管理
- Snowflake のワークシートは散らかりがち
- データ変換のロジック、ドキュメントの一元管理

</v-clicks>

---

### Testing

#### Generic Test

<v-clicks>

- YAML にサクッと書ける
- 一意性、NULL チェック、参照整合性

</v-clicks>

#### Singular Test

<v-clicks>

- カスタムSQLテスト
- ビジネスロジックの検証

</v-clicks>

#### Unit Test

<v-clicks>

- モデルの単体テスト
- データ変換ロジックの検証

</v-clicks>

---

### CI/CD

```bash
dbt build --target prod
```

<v-clicks>

- Git push → 自動テスト・デプロイ
- 本番環境への安全なリリース

</v-clicks>

---

### Documentation

<v-clicks>

- YAML でカラムに説明が書ける
- 自動生成されるドキュメント
- **リネージュ** - データの血統管理

</v-clicks>