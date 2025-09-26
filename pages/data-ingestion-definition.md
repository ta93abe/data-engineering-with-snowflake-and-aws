---
layout: two-cols
layoutClass: gap-8
---

# Data Ingestion とは？

<div class="space-y-4">

<div v-click="1" class="p-4 bg-blue-50 rounded-lg border-l-4 border-blue-500">
<h3 class="font-semibold text-blue-800">定義</h3>
<p class="text-blue-700">様々なデータソースから分析用データベースやデータウェアハウスにデータを取り込むプロセス</p>
</div>

<div v-click="2" class="p-4 bg-green-50 rounded-lg border-l-4 border-green-500">
<h3 class="font-semibold text-green-800">目的</h3>
<p class="text-green-700">分析、レポーティング、機械学習のためにデータを利用可能な形で集約</p>
</div>

</div>

::right::

<div v-click="3" class="mt-8">

```mermaid {scale: 0.8}
graph LR
    subgraph "データソース"
        DB[(データベース)]
        API[API]
        File[ファイル]
        Stream[ストリーム]
    end

    subgraph "Data Ingestion"
        ETL[Extract<br>Transform<br>Load]
        ELT[Extract<br>Load<br>Transform]
    end

    subgraph "分析基盤"
        DW[(Data Warehouse)]
        DL[(Data Lake)]
    end

    DB --> ETL
    API --> ETL
    File --> ELT
    Stream --> ELT

    ETL --> DW
    ELT --> DL
```

</div>