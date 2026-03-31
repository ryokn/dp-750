# DP-750 学習ドキュメント作成 仕様書

> **作成日**: 2026-04-01
> **対象試験**: Exam DP-750: Implementing Data Engineering Solutions Using Azure Databricks
> **対応認定資格**: Microsoft Certified: Azure Databricks Data Engineer Associate (beta)

---

## 1. 試験概要

| 項目 | 内容 |
|------|------|
| 試験コード | DP-750 |
| 正式名称 | Implementing Data Engineering Solutions Using Azure Databricks |
| 認定資格 | Microsoft Certified: Azure Databricks Data Engineer Associate (beta) |
| レベル | 中級（Associate） |
| 試験時間 | 100分 |
| 合格スコア | 700以上（1000点満点） |
| ステータス | ベータ試験（2026年4月現在） |

### 対象者

Azure Databricks を使用したデータエンジニアリングソリューションの設計・実装に従事するデータエンジニア。以下のスキルを有することが前提となる。

- Azure Databricks でのデータ統合とモデリング
- 最適化されたパイプラインの構築と展開
- ワークロードのトラブルシューティングと保守
- Unity Catalog を使用したデータ品質とガバナンスのベストプラクティス

### 前提スキル

- SQL（中級以上）
- Python プログラミング（ノートブック環境での実装経験）
- Git バージョン管理の実践知識
- SDLC プラクティスの経験
- Microsoft Entra / Azure Data Factory / Azure Monitor の基礎知識

---

## 2. スキル領域と試験ウェイト

| # | スキル領域 | ウェイト |
|---|----------|---------|
| 1 | Set up and configure an Azure Databricks environment | 15〜20% |
| 2 | Secure and govern Unity Catalog objects | 15〜20% |
| 3 | Prepare and process data | 30〜35% |
| 4 | Deploy and maintain data pipelines and workloads | 30〜35% |

### スキル領域の詳細

#### 領域 1: Set up and configure an Azure Databricks environment（15〜20%）
- コンピュートタイプの選択と設定（job compute, serverless, warehouse, classic/shared compute）
- パフォーマンス設定（CPU、ノード数、自動スケーリング、ノードタイプ、クラスターサイズ、プーリング）
- コンピュート機能設定（Photon acceleration、Databricks runtime、ML機能）
- ライブラリのインストール
- コンピュートリソースへのアクセス権限設定
- Unity Catalog オブジェクトの作成・整理（命名規則、カタログ、スキーマ、ボリューム）
- テーブル、ビュー、マテリアライズドビューの作成
- フォーリーンカタログの実装・DDL操作

#### 領域 2: Secure and govern Unity Catalog objects（15〜20%）
- Unity Catalog セキュアオブジェクトへの権限付与
- テーブル・カラムレベルのアクセス制御、行レベルセキュリティ実装
- Azure Key Vault シークレットアクセス
- サービスプリンシパル・マネージドアイデンティティによる認証
- ABAC 実装（タグとポリシー）
- 行フィルターとカラムマスク設定
- データリネージ追跡（Catalog Explorer、オーナー、履歴、依存関係）
- 監査ログ設定
- Delta Sharing のセキュア戦略

#### 領域 3: Prepare and process data（30〜35%）
- データ取り込みロジックの設計・データソース構成
- 適切なデータ取り込みツール選択（Lakeflow Connect、ノートブック、Azure Data Factory）
- データローディング方法選択（バッチ、ストリーミング）
- テーブルフォーマット選択（Parquet, Delta, CSV, JSON, Iceberg）
- データパーティショニング戦略の設計・実装
- SCD（Slowly Changing Dimension）タイプ選択
- テンポラルテーブルの実装
- クラスタリング戦略（液体クラスタリング、Z-ordering、削除ベクトル）
- マネージド/アンマネージドテーブルの選択
- データクレンジング、変換、ロード操作
- データ品質制約の実装
- スキーマ実装とスキーマドリフト管理

#### 領域 4: Deploy and maintain data pipelines and workloads（30〜35%）
- パイプライン設計と実装（ノートブック、Lakeflow Spark Declarative Pipelines）
- Lakeflow Jobs の実装（作成、トリガー設定、スケジューリング、アラート、自動再開）
- 開発ライフサイクルプロセス（Git、ブランチ、プルリクエスト、コンフリクト解消）
- Databricks Asset Bundles の設定とパッケージ化
- Azure Databricks CLI および REST API を使用したバンドルデプロイ
- ワークロード監視・トラブルシューティング・最適化
- Spark UI、DAG 分析、クエリプロファイルを使用した診断
- Delta テーブル最適化（OPTIMIZE、VACUUM）
- Azure Monitor でのログストリーミング・アラート設定

---

## 3. 学習リソース構成

### 公式ラーニングパス（Microsoft Learn）

| # | ラーニングパス | モジュール数 | 対応スキル領域 | URL |
|---|--------------|-----------|-------------|-----|
| 1 | Implement a data engineering solution using Azure Databricks | 8 | 全領域の基礎 | https://learn.microsoft.com/en-us/training/paths/azure-databricks-data-engineer/ |
| 2 | Set up and Configure an Azure Databricks Environment | 5 | 領域1 | https://learn.microsoft.com/en-us/training/paths/azure-databricks-data-engineer-set-up-configure-environment/ |
| 3 | Prepare and Process Data with Azure Databricks | 4 | 領域3 | https://learn.microsoft.com/en-us/training/paths/azure-databricks-data-engineer-prepare-process-data/ |
| 4 | Deploy and Maintain Data Pipelines and Workloads With Azure Databricks | 4 | 領域4 | https://learn.microsoft.com/en-us/training/paths/azure-databricks-data-engineer-deploy-maintain-data-pipelines-workloads/ |

### 各ラーニングパスのモジュール一覧

#### LP1: Implement a data engineering solution using Azure Databricks（8モジュール）
1. Perform incremental processing with Spark Structured Streaming
2. Implement streaming architecture patterns with Delta Live Tables
3. Optimize performance with Spark and Delta Live Tables
4. Implement CI/CD workflows in Azure Databricks
5. Automate workloads with Azure Databricks Jobs
6. Manage data privacy and governance with Azure Databricks
7. Use SQL Warehouses in Azure Databricks
8. Run Azure Databricks Notebooks with Azure Data Factory

#### LP2: Set up and Configure an Azure Databricks Environment（5モジュール）
1. Explore Azure Databricks
2. Understand Azure Databricks architecture
3. Understand Azure Databricks Integrations
4. Select and Configure Compute in Azure Databricks
5. Create and organize objects in Unity Catalog

#### LP3: Prepare and Process Data with Azure Databricks（4モジュール）
1. Design and implement data modeling with Azure Databricks
2. Ingest data into Unity Catalog
3. Cleanse, transform, and load data into Unity Catalog
4. Implement and manage data quality constraints with Azure Databricks

#### LP4: Deploy and Maintain Data Pipelines and Workloads With Azure Databricks（4モジュール）
1. Design and implement data pipelines with Azure Databricks
2. Implement Lakeflow Jobs with Azure Databricks
3. Implement development lifecycle processes in Azure Databricks
4. Monitor, troubleshoot and optimize workloads in Azure Databricks

---

## 4. 作成する学習ドキュメントの計画

### 出力ファイル一覧

| # | ファイル名 | 対応ラーニングパス | 優先度 |
|---|----------|-----------------|-------|
| 1 | `DP-750_LP2_環境のセットアップと構成.md` | LP2（5モジュール） | 高（基礎） |
| 2 | `DP-750_LP3_データの準備と処理.md` | LP3（4モジュール） | 高（試験ウェイト高） |
| 3 | `DP-750_LP4_パイプラインのデプロイと保守.md` | LP4（4モジュール） | 高（試験ウェイト高） |
| 4 | `DP-750_LP1_データエンジニアリングソリューションの実装.md` | LP1（8モジュール） | 中（応用・統合） |

### 推奨作成順序

```
LP2（基礎固め）→ LP3（データ処理）→ LP4（パイプライン）→ LP1（総合・応用）
```

理由:
- LP2 で環境・Unity Catalog の基礎を押さえることで LP3・LP4 の理解が深まる
- LP3・LP4 は試験ウェイトが高く（各 30〜35%）優先的に習得すべき
- LP1 は応用・統合的な内容のため最後に学習すると体系的に理解しやすい

---

## 5. ドキュメント作成のポイント

1. **自然な日本語にする**
   - 英語の語順に引きずられた直訳表現を避け、日本語として読みやすい文章にする
   - 主語・目的語が明確で、文意が一読で伝わる構成にする

2. **要点を抑えつつ情報はなるべく落とさない**
   - 冗長な説明は圧縮してよいが、概念・機能・選択肢の情報は省略しない
   - 表・箇条書きを活用して、コンパクトに多くの情報を収める

3. **試験前の見直し・全体像の把握を目的とする**
   - ラーニングパスそのものは別途学習済みである前提で書く
   - 手を動かして学ぶ内容（ハンズオン手順など）は省略し、概念・設計判断・選択肢の比較に重点を置く
   - 「なぜそれを選ぶのか」「他の選択肢との違いは何か」という試験視点の解説を意識する
   - 各セクションは短時間で読み返せる密度を意識する

---

## 6. ドキュメント品質基準

### 日本語表記の規則
- 機械翻訳の直訳表現を避け、自然な日本語で記述する
- Microsoft 公式の日本語技術用語を優先使用する

| 英語 | 日本語表記 |
|------|-----------|
| Unity Catalog | Unity Catalog（そのまま） |
| Lakeflow | Lakeflow（そのまま） |
| Delta Live Tables | Delta Live Tables（そのまま） |
| Slowly Changing Dimension | SCD（緩やかに変化するディメンション） |
| Liquid Clustering | 液体クラスタリング |
| Managed Identity | マネージド ID |
| Service Principal | サービスプリンシパル |
| Data Lineage | データリネージ |
| Audit Log | 監査ログ |

### 構造の要件
- 各モジュールに「学習目標」セクションを必ず含める
- 表を積極的に使い、選択肢の比較・一覧を整理する
- 試験で問われる比較ポイントを明示する（例: マネージドテーブル vs アンマネージドテーブル）
- ドキュメント末尾に「まとめ」と「参考リソース」を含める

---

## 7. 参考リソース

| リソース | URL |
|---------|-----|
| 試験スタディガイド | https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/dp-750 |
| 認定資格ページ | https://learn.microsoft.com/en-us/credentials/certifications/implementing-data-engineering-solutions-using-azure-databricks/ |
| 公式トレーニングコース（DP-750T00-A） | https://learn.microsoft.com/en-us/training/courses/dp-750t00 |
| Exam Readiness Zone | https://learn.microsoft.com/en-us/shows/exam-readiness-zone/ |
