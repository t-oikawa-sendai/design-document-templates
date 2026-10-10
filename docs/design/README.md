<!--
Program Name: DDT Design Index
Language: Markdown
Function: design-document-templates 自体の管理用設計書一覧
Created: 2026-10-09
Last Updated: 2026-10-10
Author: Takashi Oikawa
AI: Cursor
Memo: Document ID DDT-DESIGN-INDEX-001。Version 0.12 / Draft。正式承認ではない
-->

# Design Documents Index（設計書一覧）

<!-- Document Info（文書情報） -->
| Item（項目） | Value（値） |
|---|---|
| Document ID（文書ID） | DDT-DESIGN-INDEX-001 |
| Version（バージョン） | 0.12 |
| Status（ステータス） | Draft |
| Created Date（作成日） | 2026-10-09 |
| Last Updated（最終更新日） | 2026-10-10 |
| Owner（管理者） | Takashi Oikawa |
| Related Documents（関連文書） | [CHANGELOG.md](../../CHANGELOG.md) / [README.md](../../README.md) / [../STUDENT_USAGE_GUIDE.md](../STUDENT_USAGE_GUIDE.md) / [../GOVERNED_DEVELOPMENT_GUIDE.md](../GOVERNED_DEVELOPMENT_GUIDE.md) / [01_REQUEST_DEFINITION.md](./01_REQUEST_DEFINITION.md) / [02_REQUIREMENTS_DEFINITION.md](./02_REQUIREMENTS_DEFINITION.md) / [03_DATA_AND_SECURITY_DESIGN.md](./03_DATA_AND_SECURITY_DESIGN.md) / [04_UI_AND_FLOW_DESIGN.md](./04_UI_AND_FLOW_DESIGN.md) / [05_ARCHITECTURE_DESIGN.md](./05_ARCHITECTURE_DESIGN.md) / [06_OPERATION_AND_HANDOFF.md](./06_OPERATION_AND_HANDOFF.md) |

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

正式 Purpose は DISTRIBUTION である。開発目的の正本は [01_REQUEST_DEFINITION.md](./01_REQUEST_DEFINITION.md) §5.1 である。

SDDの定義は [使用説明書§2](../STUDENT_USAGE_GUIDE.md#2-用語ミニ辞典) を参照する。専用の非公開 Repository は公開しない。基本構成は、利用先の `docs/design/README.md` と 01〜06 の7文書である。同じ仕様の正本は一つにし、他の文書からは参照する（SSOT）。7文書の存在だけでは効果を保証しない。記載先の指定、参照関係の維持、人による確認を運用とする。

利用先の `AGENTS.md` と `CONSTITUTION.md` の導入は任意である。両方がなくても、記入、仕様変更、実装、確認を進められる。設定ファイルが既にある利用先では、その現行ルールを読む。設定の削除や無視を案内しない。配布元自身は既存の管理ルールで運用を続ける。この任意性と、配布元の必須管理資産は別である。

使い方は [../STUDENT_USAGE_GUIDE.md](../STUDENT_USAGE_GUIDE.md) で配布する。管理方式の共通前提、設定の有無による構成、AIへの適用方法は [参考資料§1](../GOVERNED_DEVELOPMENT_GUIDE.md#1-管理方式の共通前提) で配布し、root README と使用説明書から参照する。本文は参考資料に置き、この一覧へ再掲しない。

---

## 2. Problem / Solution / Benefit Summary（問題・解決・効果の概要）

| Item（項目） | Summary（概要） | Detail Document（詳細文書） |
|---|---|---|
| Current Problems（現在の問題点） | AI任せにすると、似た設計文書が乱立し、どれが正しい仕様か分からなくなる。専用の非公開 Repository は公開しない。 | [01_REQUEST_DEFINITION.md](./01_REQUEST_DEFINITION.md) |
| Development Purpose（開発目的） | 正本は 01 §5.1。全文はそこを参照する。 | [01_REQUEST_DEFINITION.md](./01_REQUEST_DEFINITION.md) |
| Solution Approach（解決方針） | 7テンプレートを `templates/design/` に置く。使用説明書で取得、初期化、記入、仕様変更、実装への接続を説明する。同じ仕様は再掲せず参照する。設定ファイルは利用先で任意とし、詳細は参考資料へ置く。root README から説明書、テンプレート、参考資料へ案内する。管理用文書と配布物を分ける。 | [01_REQUEST_DEFINITION.md](./01_REQUEST_DEFINITION.md) |
| System Functions（システム機能） | 設計書 README と 01〜06、計7文書を Markdown で配布する。使用説明書と参考資料を配布する。利用先の設定ファイル導入は任意である。独自アプリ機能は提供しない。 | [02_REQUIREMENTS_DEFINITION.md](./02_REQUIREMENTS_DEFINITION.md) |
| Expected Benefits（期待効果） | 生徒がテンプレートを取得し、自分のプロジェクトの `docs/design/` に置いて記入できる。仕様の記載先が決まり、重複を参照に置き換えられる。設定がなくても指示例で開始できる。 | [01_REQUEST_DEFINITION.md](./01_REQUEST_DEFINITION.md) |
| Completion Criteria（完成判定基準） | 7文書の取得と記入ができること。設定がなくても記入、仕様変更、実装の指示が説明書で完結すること。参考資料へのリンクを確認できること。元の専用 Repository が非公開を維持すること。配布元との内容照合と公開前確認が完了していること。公開前確認は未完了である。 | [01_REQUEST_DEFINITION.md](./01_REQUEST_DEFINITION.md) |

---

## 3. Screen Overview（画面概要）

本文書では対象外。理由: 独自アプリの画面は提供しない。画像は新規作成しない。配布テンプレートにある画像パスは記入例であり、この Repository の完成済み画像ではない。

詳細の対象外理由: [04_UI_AND_FLOW_DESIGN.md](./04_UI_AND_FLOW_DESIGN.md)

---

## 4. Design Documents Index（設計書一覧）

この表は管理用設計書の索引である。配布テンプレートの版数とは別である。01〜06 の Version / Status は、各文書の Document Info と一致させる。

| File（ファイル名） | Document Name（文書名） | Status（ステータス） | Version（バージョン） | Owner（担当者） |
|---|---|---|---|---|
| [README.md](./README.md) | Design Documents Index（設計書一覧） | Draft | 0.12 | Takashi Oikawa |
| [01_REQUEST_DEFINITION.md](./01_REQUEST_DEFINITION.md) | Request Definition（要求定義） | Draft | 0.8 | Takashi Oikawa |
| [02_REQUIREMENTS_DEFINITION.md](./02_REQUIREMENTS_DEFINITION.md) | Requirements Definition（要件定義） | Draft | 0.11 | Takashi Oikawa |
| [03_DATA_AND_SECURITY_DESIGN.md](./03_DATA_AND_SECURITY_DESIGN.md) | Data and Security Design（データ・セキュリティ設計） | Draft | 0.7 | Takashi Oikawa |
| [04_UI_AND_FLOW_DESIGN.md](./04_UI_AND_FLOW_DESIGN.md) | UI and Flow Design（UI・フロー設計） | Draft | 0.7 | Takashi Oikawa |
| [05_ARCHITECTURE_DESIGN.md](./05_ARCHITECTURE_DESIGN.md) | Architecture Design（アーキテクチャ設計） | Draft | 0.6 | Takashi Oikawa |
| [06_OPERATION_AND_HANDOFF.md](./06_OPERATION_AND_HANDOFF.md) | Operation and Handoff Design（運用・詳細設計引き継ぎ） | Draft | 0.10 | Takashi Oikawa |

---

## 5. Overall Design Policy（設計上の全体方針・前提）

- 正式 Purpose は DISTRIBUTION である。開発目的の正本は 01 §5.1 である。Purpose の値は変えない。
- 管理用設計書は `docs/design/`、生徒向け配布物は `templates/design/` とする。
- 配布時に本文、日付、Owner、Status、Version、改行、相対リンクを変換しない。
- 中央管理コピーは独自に編集しない。中央管理コピーの修正は中央原本側の手順であり、今回の配布物の修正範囲に含めない。
- 使用説明書は `docs/STUDENT_USAGE_GUIDE.md` とする。設定ファイルの参考資料は `docs/GOVERNED_DEVELOPMENT_GUIDE.md` とし、root README と使用説明書から参照する。
- 手順A・手順B・LEARNINGという利用区分は、この配布物に置かない。これは正式 Purpose の変更ではない。
- 利用先に設定ファイルが既にある場合は、その現行ルールを読む。削除や無視により任意運用へ移す案内はしない。管理方式は設定の有無で変えない。共通前提、構成、AIへの適用の本文は参考資料 §1 に置く。
- 配布元自身は既存管理ルールで運用を続ける。利用先で任意であることと、配布元の必須管理資産は別である。
- この準備工程では、公開範囲は Private を維持する。この工程では Public にしない。元の専用 Repository を非公開のまま保つ。

---

## 6. Glossary（用語集・略語定義）

| Term / Abbreviation（用語・略語） | Definition（定義） |
|---|---|
| DISTRIBUTION | この Repository の正式 Purpose。テンプレートの配布と使用方法の案内。 |
| SDD（仕様駆動開発） | [使用説明書§2](../STUDENT_USAGE_GUIDE.md#2-用語ミニ辞典) を参照する。 |
| SSOT | 正しい情報の管理元を一つに定める原則。同じ仕様は正本を一つにし、他からは参照する。 |
| 管理用設計書 | `docs/design/` の文書。この配布 Repository 自体の設計。 |
| 配布テンプレート | `templates/design/` の7文書。生徒が取得するテンプレート。 |
| 中央テンプレ正本 | `solacom_main` の `docs/standards/templates/design/`。 |
| 参考資料 | `docs/GOVERNED_DEVELOPMENT_GUIDE.md`。§1 に、7文書の記載先、管理方式の共通前提、設定の有無による構成、AIへの適用方法を置く。 |

---

## 7. Document Owners and Reviewers（文書管理者・レビュアー一覧）

| Role（役割） | Name（氏名） | Assigned Documents（担当文書） |
|---|---|---|
| Document Owner（文書管理者） | Takashi Oikawa | All Documents（全文書） |
| Reviewer（レビュアー） | 未指定 | 差分レビューは設計担当が行う。氏名の追加指定はない。 |
