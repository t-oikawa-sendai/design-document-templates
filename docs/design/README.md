<!--
Program Name: DDT Design Index
Language: Markdown
Function: design-document-templates 自体の管理用設計書一覧
Created: 2026-10-09
Last Updated: 2026-10-09
Author: Takashi Oikawa
AI: Cursor
Memo: Document ID DDT-DESIGN-INDEX-001。Version 0.4 / Draft。正式承認ではない
-->

# Design Documents Index（設計書一覧）

<!-- Document Info（文書情報） -->
| Item（項目） | Value（値） |
|---|---|
| Document ID（文書ID） | DDT-DESIGN-INDEX-001 |
| Version（バージョン） | 0.4 |
| Status（ステータス） | Draft |
| Created Date（作成日） | 2026-10-09 |
| Last Updated（最終更新日） | 2026-10-09 |
| Owner（管理者） | Takashi Oikawa |
| Related Documents（関連文書） | [CHANGELOG.md](../../CHANGELOG.md) / [README.md](../../README.md) / [../STUDENT_USAGE_GUIDE.md](../STUDENT_USAGE_GUIDE.md) / [01_REQUEST_DEFINITION.md](./01_REQUEST_DEFINITION.md) / [02_REQUIREMENTS_DEFINITION.md](./02_REQUIREMENTS_DEFINITION.md) / [03_DATA_AND_SECURITY_DESIGN.md](./03_DATA_AND_SECURITY_DESIGN.md) / [04_UI_AND_FLOW_DESIGN.md](./04_UI_AND_FLOW_DESIGN.md) / [05_ARCHITECTURE_DESIGN.md](./05_ARCHITECTURE_DESIGN.md) / [06_OPERATION_AND_HANDOFF.md](./06_OPERATION_AND_HANDOFF.md) |

> 詳細な変更履歴はリポジトリルートの [CHANGELOG.md](../../CHANGELOG.md) を参照。

この文書は、配布 Repository 自体の管理用設計書の入口である。生徒向け配布テンプレートの一覧は、root の [README.md](../../README.md) にあり、配置先は `templates/design/` である。

---

## Table of Contents（目次）

1. [Project Overview（プロジェクト・機能の概要）](#1-project-overviewプロジェクト機能の概要)
2. [Problem / Solution / Benefit Summary（問題・解決・効果の概要）](#2-problem--solution--benefit-summary問題解決効果の概要)
3. [Screen Overview（画面概要）](#3-screen-overview画面概要)
4. [Design Documents Index（設計書一覧）](#4-design-documents-index設計書一覧)
5. [Overall Design Policy（設計上の全体方針・前提）](#5-overall-design-policy設計上の全体方針前提)
6. [Glossary（用語集・略語定義）](#6-glossary用語集略語定義)
7. [Document Owners and Reviewers（文書管理者・レビュアー一覧）](#7-document-owners-and-reviewers文書管理者レビュアー一覧)

---

## 1. Project Overview（プロジェクト・機能の概要）

このリポジトリの目的は、生徒が自身のプロジェクトの設計書を作成するためのテンプレートの配布及び使用方法のガイドラインである。専用の非公開 Repository は公開しない。配布する設計テンプレートは、設計書 README と 01〜06、計7文書である。これに加えて、文書の役割、AI読込み、フォルダ構成、初回と再開の説明を [../STUDENT_USAGE_GUIDE.md](../STUDENT_USAGE_GUIDE.md) で提供する。使用説明書は第8の設計書ではない。

---

## 2. Problem / Solution / Benefit Summary（問題・解決・効果の概要）

| Item（項目） | Summary（概要） | Detail Document（詳細文書） |
|---|---|---|
| Current Problems（現在の問題点） | 専用の非公開 Repository を公開せず、生徒へ設計書のテンプレートを渡す。 | [01_REQUEST_DEFINITION.md](./01_REQUEST_DEFINITION.md) |
| Development Purpose（開発目的） | このリポジトリの目的は、生徒が自身のプロジェクトの設計書を作成するためのテンプレートの配布及び使用方法のガイドラインである。 | [01_REQUEST_DEFINITION.md](./01_REQUEST_DEFINITION.md) |
| Solution Approach（解決方針） | 7テンプレートを `templates/design/` に置く。使用説明書で、文書の役割、AI読込み、フォルダ構成、初回と再開を説明する。root README から説明書とテンプレートへ案内する。管理用文書と配布物を分ける。 | [01_REQUEST_DEFINITION.md](./01_REQUEST_DEFINITION.md) |
| System Functions（システム機能） | 設計書 README と 01〜06、計7文書を Markdown で配布する。使用説明書1文書で利用方法を案内する。独自アプリ機能は提供しない。 | [02_REQUIREMENTS_DEFINITION.md](./02_REQUIREMENTS_DEFINITION.md) |
| Expected Benefits（期待効果） | 生徒がテンプレートを取得し、自分のプロジェクトの `docs/design/` に置いて記入できる。文書の役割、AIへ渡す資料、再開方法を説明書で確認できる。 | [01_REQUEST_DEFINITION.md](./01_REQUEST_DEFINITION.md) |
| Completion Criteria（完成判定基準） | 7文書の取得と記入ができること。説明書から読み込み対象、順序、指示文、構成図を確認できること。元の専用 Repository が非公開を維持すること。配布元との内容照合と公開前確認が完了していること。公開前確認は未完了である。 | [01_REQUEST_DEFINITION.md](./01_REQUEST_DEFINITION.md) |

---

## 3. Screen Overview（画面概要）

本文書では対象外。理由: 独自アプリの画面は提供しない。画像は新規作成しない。配布テンプレートにある画像パスは記入例であり、この Repository の完成済み画像ではない。

詳細の対象外理由: [04_UI_AND_FLOW_DESIGN.md](./04_UI_AND_FLOW_DESIGN.md)

---

## 4. Design Documents Index（設計書一覧）

この表は管理用設計書の索引である。配布テンプレートの版数とは別である。01〜06 の Version / Status は、各文書の Document Info と一致させる。

| File（ファイル名） | Document Name（文書名） | Status（ステータス） | Version（バージョン） | Owner（担当者） |
|---|---|---|---|---|
| [README.md](./README.md) | Design Documents Index（設計書一覧） | Draft | 0.4 | Takashi Oikawa |
| [01_REQUEST_DEFINITION.md](./01_REQUEST_DEFINITION.md) | Request Definition（要求定義） | Draft | 0.3 | Takashi Oikawa |
| [02_REQUIREMENTS_DEFINITION.md](./02_REQUIREMENTS_DEFINITION.md) | Requirements Definition（要件定義） | Draft | 0.3 | Takashi Oikawa |
| [03_DATA_AND_SECURITY_DESIGN.md](./03_DATA_AND_SECURITY_DESIGN.md) | Data and Security Design（データ・セキュリティ設計） | Draft | 0.3 | Takashi Oikawa |
| [04_UI_AND_FLOW_DESIGN.md](./04_UI_AND_FLOW_DESIGN.md) | UI and Flow Design（UI・フロー設計） | Draft | 0.3 | Takashi Oikawa |
| [05_ARCHITECTURE_DESIGN.md](./05_ARCHITECTURE_DESIGN.md) | Architecture Design（アーキテクチャ設計） | Draft | 0.3 | Takashi Oikawa |
| [06_OPERATION_AND_HANDOFF.md](./06_OPERATION_AND_HANDOFF.md) | Operation and Handoff Design（運用・詳細設計引き継ぎ） | Draft | 0.3 | Takashi Oikawa |

---

## 5. Overall Design Policy（設計上の全体方針・前提）

- 正式 Purpose は DISTRIBUTION である。テンプレートの配布と使用方法の案内である。
- 管理用設計書は `docs/design/`、生徒向け配布物は `templates/design/` とする。
- 配布時に本文、日付、Owner、Status、Version、改行、相対リンクを変換しない。
- 中央管理コピーは独自に編集しない。
- 使用説明書は `docs/STUDENT_USAGE_GUIDE.md` とする。設計書一覧の第8行にはしない。
- この準備工程では、公開範囲は Private を維持する。この工程では Public にしない。元の専用 Repository を非公開のまま保つ。

---

## 6. Glossary（用語集・略語定義）

| Term / Abbreviation（用語・略語） | Definition（定義） |
|---|---|
| DISTRIBUTION | この Repository の正式 Purpose。テンプレートの配布と使用方法の案内。 |
| 管理用設計書 | `docs/design/` の文書。この配布 Repository 自体の設計。 |
| 配布テンプレート | `templates/design/` の7文書。生徒が取得するテンプレート。 |
| 中央テンプレ正本 | `solacom_main` の `docs/standards/templates/design/`。 |

---

## 7. Document Owners and Reviewers（文書管理者・レビュアー一覧）

| Role（役割） | Name（氏名） | Assigned Documents（担当文書） |
|---|---|---|
| Document Owner（文書管理者） | Takashi Oikawa | All Documents（全文書） |
| Reviewer（レビュアー） | 未指定 | 差分レビューは設計担当が行う。氏名の追加指定はない。 |
