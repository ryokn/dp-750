# DP-750 学習ドキュメント

**Exam DP-750: Implementing Data Engineering Solutions Using Azure Databricks**
**認定資格: Microsoft Certified: Azure Databricks Data Engineer Associate (beta)**

---

## このリポジトリについて

DP-750 試験の合格を目的とした、日本語の学習ドキュメント集です。Microsoft Learn の公式ラーニングパス（英語）をベースに、試験視点でのポイント整理・選択肢比較を重視してまとめています。

- ラーニングパスを一通り学習済みの方が、試験前の見直しや全体像の把握に使うことを想定しています
- 「なぜそれを選ぶのか」「他の選択肢との違いは何か」という比較・判断軸を重点的に記載しています

---

## ドキュメント一覧

| # | ファイル | 対応ラーニングパス | 試験ウェイト |
|---|---------|-----------------|------------|
| 1 | [LP2: 環境のセットアップと構成](./DP-750_LP2_環境のセットアップと構成.md) | Set up and Configure an Azure Databricks Environment（5モジュール） | 15〜20% |
| 2 | [LP3: データの準備と処理](./DP-750_LP3_データの準備と処理.md) | Prepare and Process Data with Azure Databricks（4モジュール） | 30〜35% |
| 3 | [LP4: パイプラインのデプロイと保守](./DP-750_LP4_パイプラインのデプロイと保守.md) | Deploy and Maintain Data Pipelines and Workloads With Azure Databricks（4モジュール） | 30〜35% |
| 4 | [LP1: データエンジニアリングソリューションの実装](./DP-750_LP1_データエンジニアリングソリューションの実装.md) | Implement a data engineering solution using Azure Databricks（8モジュール） | 全領域 |

## 推奨学習順序

```
LP2（基礎固め）→ LP3（データ処理）→ LP4（パイプライン）→ LP1（総合・応用）
```

LP2 で Azure Databricks の環境・Unity Catalog の基礎を押さえた上で、試験ウェイトの高い LP3・LP4 を学習し、最後に LP1 で全体を統合するのが効果的です。

---

## 試験概要

| 項目 | 内容 |
|------|------|
| 試験コード | DP-750 |
| 試験時間 | 100分 |
| 合格スコア | 700点以上（1000点満点） |
| ステータス | ベータ試験（2026年4月現在） |

### スキル領域

| スキル領域 | ウェイト |
|----------|---------|
| Set up and configure an Azure Databricks environment | 15〜20% |
| Secure and govern Unity Catalog objects | 15〜20% |
| Prepare and process data | 30〜35% |
| Deploy and maintain data pipelines and workloads | 30〜35% |

---

## 参考リソース

| リソース | URL |
|---------|-----|
| 試験スタディガイド | https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/dp-750 |
| 認定資格ページ | https://learn.microsoft.com/en-us/credentials/certifications/implementing-data-engineering-solutions-using-azure-databricks/ |
| 公式トレーニングコース（DP-750T00-A） | https://learn.microsoft.com/en-us/training/courses/dp-750t00 |
