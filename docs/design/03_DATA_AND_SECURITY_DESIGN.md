<!--
Program Name: DDT Data and Security Design
Language: Markdown
Function: 配布文書の情報構成と、公開情報の扱いを定義する
Created: 2026-10-09
Last Updated: 2026-10-09
Author: Takashi Oikawa
AI: Cursor
Memo: Document ID DDT-DATA-001。Version 0.3 / Draft。正式承認ではない
-->

# Data and Security Design（データ・セキュリティ設計）

<!-- Document Info（文書情報） -->
| Item（項目） | Value（値） |
|---|---|
| Document ID（文書ID） | DDT-DATA-001 |
| Version（バージョン） | 0.3 |
| Status（ステータス） | Draft |
| Created Date（作成日） | 2026-10-09 |
| Last Updated（最終更新日） | 2026-10-09 |
| Owner（管理者） | Takashi Oikawa |
| Related Documents（関連文書） | README.md / 02_REQUIREMENTS_DEFINITION.md / 05_ARCHITECTURE_DESIGN.md / [../STUDENT_USAGE_GUIDE.md](../STUDENT_USAGE_GUIDE.md) |

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

本文書は、配布文書の情報構成と、公開してよい情報の扱いを定義する。

---

## 2. Scope（対象範囲）

Repository 固有の管理・案内11文書と配布テンプレート7文書の情報構成、Document Info、配布元コミットと内容照合を対象とする。11文書の内訳は、root README、`project-notes/CURRENT.md`、`CHANGELOG.md`、`docs/design/` の7文書、および `docs/STUDENT_USAGE_GUIDE.md` である。この内訳は [02_REQUIREMENTS_DEFINITION.md](./02_REQUIREMENTS_DEFINITION.md) と一致する。

---

## 3. Out of Scope（対象外範囲）

本文書では対象外。理由: アプリのエンティティ、DB、業務データ、ログは扱わない。

---

## 4. Assumptions（前提条件）

- 各対象文書は Document Info の7項目を持つ。
- 配布元コミットは `solacom_main` の `16c44976638b48c53ef16399b1d51217c540be0a` である。
- 資格情報と内部案件情報は載せない。

---

## 5. Definition Details（定義内容）

### 5.1 Entity Definition and ER Diagram（エンティティ定義・ER図）

アプリのエンティティは扱わない。情報の単位は文書である。

#### Entity List（エンティティ一覧）

| Entity Name（エンティティ名） | Description（説明） |
|---|---|
| Repository固有の管理・案内11文書 | root README、`project-notes/CURRENT.md`、`CHANGELOG.md`、`docs/design/` の7文書、および使用説明書 `docs/STUDENT_USAGE_GUIDE.md`。既存10件と使用説明書1件である。使用説明書は Repository 固有の案内文書であり、中央管理コピーでも無変更の配布テンプレートでもない。中央管理コピーや既存作成ガイドはこの件数に含めない。各文書は Document Info を持つ。 |
| 配布テンプレート7文書 | `templates/design/` の README と 01〜06。中央正本 `solacom_main` の `docs/standards/templates/design/`（コミット `16c44976638b48c53ef16399b1d51217c540be0a`）から無変更で配置し、Git Blob SHA で内容を照合する。 |

#### ER Diagram（ER図）

```
本文書では対象外。理由: アプリのエンティティ関係図は作成しない。DBは提供しない。
```

### 5.2 Table Definitions（テーブル定義）

対象範囲は文書のみである。DB のテーブルは除外する。理由: DB は提供しない。

#### Out of Scope（対象外）

| Column（カラム名） | Type（型） | NOT NULL | PK / FK | Description（説明） |
|---|---|---|---|---|
| — | — | — | — | 対象外。理由: DB のカラム定義は行わない。 |

### 5.3 Data Access and Role Design（データアクセス権限・ロール設計）

この Repository で独自認証は実装しない。GitHub の認証を利用する。

| Role Name（ロール名） | Accessible Data / Permitted Operations（アクセス可能なデータ / 操作範囲） |
|---|---|
| 管理者（Takashi Oikawa） | Repository を管理する。GitHub の認証を利用する。 |
| 生徒 | テンプレートを取得する。この準備工程では Private であり、取得できる公開状態ではない。 |
| Cursor | 指示範囲で作業する。独自の認証主体は追加しない。 |

### 5.4 Personal and Confidential Data Policy（個人情報・機密データの取り扱い方針）

資格情報、認証情報、個別案件の管理実績、内部案件情報は載せない。元 Repository の具体的な業務情報は配布しない。

生徒が AI へ渡すのは、自分の最新の課題、設計、作業状態である。配布元の履歴、`project-notes/CURRENT.md`、記入済みの管理用設計を、自分の実績として使わない。この案内は [../STUDENT_USAGE_GUIDE.md](../STUDENT_USAGE_GUIDE.md) に記載する。

### 5.5 Encryption, Masking, and Logging Policy（暗号化・マスキング・ログ取得方針）

| Type（種別） | Target（対象） | Policy / Method（方式・方針） |
|---|---|---|
| Encryption（暗号化） | アプリデータ | 対象外。理由: アプリの暗号化対象は扱わない。 |
| Masking（マスキング） | アプリデータ | 対象外。理由: アプリのマスキング対象は扱わない。 |
| Logging（ログ取得） | アプリログ | 対象外。理由: アプリのログは対象外である。 |

### 5.6 Security Design Specifications（セキュリティ設計仕様）

| Type（種別） | Design Specification（設計仕様） |
|---|---|
| Authentication（認証） | GitHub の認証を利用する。この Repository で独自認証は実装しない。 |
| Authorization（認可） | 独自認可は実装しない。GitHub の公開範囲に従う。この準備工程では Private である。 |
| Access Control（権限管理） | この準備工程では Private を維持する。元の専用 Repository を非公開のまま保つ。Private から Public へ変更する前に、内容と履歴を確認する。 |
| Communication（通信） | 独自の通信実装はない。GitHub を利用する。 |
| Data Storage（データ保存） | Markdown ファイルを Git で管理する。 |
| Data Disposal（データ廃棄） | 未指定。独自の廃棄手順は作らない。 |
| Personal Data Protection（個人情報保護） | 資格情報、内部案件情報、個別案件の業務情報は載せない。 |

---

## 6. Open Issues（未決事項）

本文書の範囲に未決仕様はない。理由: 本指示で指定した事項は確定事項として本文に記載した。データ廃棄手順が未指定であることは、独自手順を作らない確定事項であり、未決仕様ではない。テンプレートの空の TBD 行は、本 Repository の未決事項ではない。

| ID | Open Issue（未決事項） | Owner（担当者） | Due Date（期限） | Status（ステータス） |
|---|---|---|---|---|
| — | 未決仕様はない。理由は本節本文のとおり。 | — | — | — |

---

## 7. Handoff to Detail Design（詳細設計への引き継ぎ）

アプリ実装への引き継ぎは対象外。理由: DB と独自認証は実装しない。Private から Public へ変更する前に、内容と履歴を確認する。配置は [05_ARCHITECTURE_DESIGN.md](./05_ARCHITECTURE_DESIGN.md) に記載する。
