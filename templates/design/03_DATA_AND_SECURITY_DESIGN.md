# Data and Security Design（データ・セキュリティ設計）

<!-- Document Info（文書情報） -->
| Item（項目） | Value（値） |
|---|---|
| Document ID（文書ID） | DATA-001 |
| Version（バージョン） | 0.3 |
| Status（ステータス） | Draft |
| Created Date（作成日） | 2026-06-21 |
| Last Updated（最終更新日） | 2026-10-10 |
| Owner（管理者） | Takashi Oikawa |
| Related Documents（関連文書） | README.md / 02_REQUIREMENTS_DEFINITION.md / 05_ARCHITECTURE_DESIGN.md |

---

## Table of Contents（目次）

1. [Purpose（目的）](#1-purpose目的)
2. [Scope（対象範囲）](#2-scope対象範囲)
3. [Out of Scope（対象外範囲）](#3-out-of-scope対象外範囲)
4. [Assumptions（前提条件）](#4-assumptions前提条件)
5. [Definition Details（定義内容）](#5-definition-details定義内容)
6. [Open Issues（未決事項）](#6-open-issues未決事項)
7. [Handoff to Detail Design（詳細設計への引き継ぎ）](#7-handoff-to-detail-design詳細設計への引き継ぎ)

---

## 1. Purpose（目的）

<!-- この文書が何を定義し、誰に向けて書かれているかを記述する -->
<!-- 例: 本文書は、○○機能におけるデータモデル・セキュリティ設計仕様を定義し、
        実装フェーズの基準とすることを目的とする -->

（記入欄）

---

## 2. Scope（対象範囲）

（記入欄）

---

## 3. Out of Scope（対象外範囲）

<!-- 該当内容がない場合: 「本文書では対象外。理由: ○○」と記載する -->

（記入欄）

---

## 4. Assumptions（前提条件）

（記入欄）

---

## 5. Definition Details（定義内容）

### 5.1 Entity Definition and ER Diagram（エンティティ定義・ER図）

<!-- 主要エンティティとその関係を記述する -->
<!-- ER図は Mermaid / 画像 / リンクのいずれかで添付する -->

#### Entity List（エンティティ一覧）

| Entity Name（エンティティ名） | Description（説明） |
|---|---|
| （記入欄） | （記入欄） |

#### ER Diagram（ER図）

```
（ER図を記述、または画像リンクを貼る）
```

### 5.2 Table Definitions（テーブル定義）

<!-- 原則として全テーブルを記載する -->
<!-- 一部のみ記載する場合は、対象範囲と除外理由を明記する -->

#### [Table Name（テーブル名）]

| Column（カラム名） | Type（型） | NOT NULL | PK / FK | Description（説明） |
|---|---|---|---|---|
| （記入欄） | （記入欄） | （記入欄） | （記入欄） | （記入欄） |

### 5.3 Data Access and Role Design（データアクセス権限・ロール設計）

<!-- 誰がどのデータに対してどの操作を許可されるかを記述する -->
<!-- ロールとデータ操作権限の正本は本節である -->

| Role Name（ロール名） | Accessible Data / Permitted Operations（アクセス可能なデータ / 操作範囲） |
|---|---|
| （記入欄） | （記入欄） |

### 5.4 Personal and Confidential Data Policy（個人情報・機密データの取り扱い方針）

<!-- 個人情報・機密データの定義、分類、保護上の注意と、その保存・保持・廃棄方針を記述する。個人・機密データの保存・保持・廃棄方針の正本は本節である。一般データの方針は本節へ書かない -->
<!-- ログの取得・保持・廃棄方針は、個人・機密情報を含む場合も §5.5 を参照し、再掲しない。ログに含まれる個人・機密情報の分類と保護上の注意は本節に書く -->
<!-- アクセス制限は §5.3 のロールとデータ操作権限を参照し、方針上必要な補足だけを書く。方式と実装は §5.6 に書く -->
<!-- 該当データがない場合: 「本文書では対象外。理由: 個人情報・機密データを扱わないため」と記載する -->

（記入欄）

### 5.5 Encryption, Masking, and Logging Policy（暗号化・マスキング・ログ取得方針）

<!-- 暗号化対象・方式、マスキング対象・方式を記述する。ログの取得対象、保持期間、廃棄条件は、個人・機密情報を含む場合も本節が正本である。個人・機密情報としての保護方針は §5.4 を参照し、再掲しない -->
<!-- 06_OPERATION_AND_HANDOFF.md §5.6 は本節のログ方針を参照し、保守の実行方法を書く -->
<!-- 該当内容がない場合: 「本文書では対象外。理由: ○○」と記載する -->

| Type（種別） | Target（対象） | Policy / Method（方式・方針） |
|---|---|---|
| Encryption（暗号化） | （記入欄） | （記入欄） |
| Masking（マスキング） | （記入欄） | （記入欄） |
| Logging（ログ取得） | （記入欄） | （記入欄） |

### 5.6 Security Design Specifications（セキュリティ設計仕様）

<!-- 認証・認可・権限・通信・保存・廃棄・個人情報保護の実装方式を記述する -->
<!-- ロールとデータ操作権限は §5.3 を参照し、認可と権限は方式・実装上の補足だけを書く -->
<!-- 個人・機密データの保存・保持・廃棄方針は §5.4 を参照し、ここでは実装方式を書く。方針の期限を本節で決め直さない -->
<!-- ログの取得・保持方針は §5.5 を参照し、方式の補足だけを書く -->
<!-- 個人・機密データとログを除く一般データの保存・保持・廃棄方針は 06_OPERATION_AND_HANDOFF.md §5.6 を参照し、方式の補足だけを書く -->
<!-- セキュリティ上の要求レベルは 02_REQUIREMENTS_DEFINITION.md に記載する -->

| Type（種別） | Design Specification（設計仕様） |
|---|---|
| Authentication（認証） | （記入欄） |
| Authorization（認可） | （記入欄） |
| Access Control（権限管理） | （記入欄） |
| Communication（通信） | （記入欄） |
| Data Storage（データ保存） | （記入欄） |
| Data Disposal（データ廃棄） | （記入欄） |
| Personal Data Protection（個人情報保護） | （記入欄） |

---

## 6. Open Issues（未決事項）

<!-- 未決事項は、この文書の Document ID とローカル ID の組で識別する。例: DATA-001:TBD-001 -->
<!-- 課題管理の台帳を別に使っている場合は、同じ課題の既存 ID を参照し、新しく採番しない。台帳の導入は 7文書運用の必須条件にしない -->

| ID | Open Issue（未決事項） | Owner（担当者） | Due Date（期限） | Status（ステータス） |
|---|---|---|---|---|
| TBD-001 | （記入欄） | （記入欄） | （記入欄） | Open |

---

## 7. Handoff to Detail Design（詳細設計への引き継ぎ）

<!-- 実装フェーズに伝えるべき設計意図・判断経緯・注意事項を記述する -->
<!-- 該当内容がない場合: 「本文書では対象外。理由: ○○」と記載する -->

（記入欄）
