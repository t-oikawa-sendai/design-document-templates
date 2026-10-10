<!--
Program Name: DDT Request Definition
Language: Markdown
Function: 配布Repositoryの目的、対象、成功条件を定義する
Created: 2026-10-09
Last Updated: 2026-10-10
Author: Takashi Oikawa
AI: Cursor
Memo: Document ID DDT-REQ-001。Version 0.6 / Draft。正式承認ではない
-->

# Request Definition（要求定義）

<!-- Document Info（文書情報） -->
| Item（項目） | Value（値） |
|---|---|
| Document ID（文書ID） | DDT-REQ-001 |
| Version（バージョン） | 0.6 |
| Status（ステータス） | Draft |
| Created Date（作成日） | 2026-10-09 |
| Last Updated（最終更新日） | 2026-10-10 |
| Owner（管理者） | Takashi Oikawa |
| Related Documents（関連文書） | README.md / 02_REQUIREMENTS_DEFINITION.md / [../STUDENT_USAGE_GUIDE.md](../STUDENT_USAGE_GUIDE.md) / [../GOVERNED_DEVELOPMENT_GUIDE.md](../GOVERNED_DEVELOPMENT_GUIDE.md) |

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

本文書は、配布の目的、対象、成功条件を定義する。正式 Purpose は DISTRIBUTION であり、開発目的の全文はこの Purpose の変更ではない。開発目的の正本は §5.1 である。

SDDは、仕様書を先に書き、AIはその仕様に従って実装する進め方である。専用の非公開 Repository は公開しない。同じ仕様の正本は一つにし、他の文書からは参照する（SSOT）。利用先の AGENTS.md と CONSTITUTION.md は任意である。両方がなくても記入、仕様変更、実装、確認を進められる。使い方は [../STUDENT_USAGE_GUIDE.md](../STUDENT_USAGE_GUIDE.md)、設定ファイルの使用方法は [../GOVERNED_DEVELOPMENT_GUIDE.md](../GOVERNED_DEVELOPMENT_GUIDE.md) で配布し、root README と使用説明書から参照する。

---

## 2. Scope（対象範囲）

対象は、この配布 Repository、設計書 README および 01〜06 の7テンプレート、生徒向け使用説明書 [../STUDENT_USAGE_GUIDE.md](../STUDENT_USAGE_GUIDE.md)、および参考資料 [../GOVERNED_DEVELOPMENT_GUIDE.md](../GOVERNED_DEVELOPMENT_GUIDE.md) である。

---

## 3. Out of Scope（対象外範囲）

- 個別案件の設計実績
- AI ペルソナ
- アプリ開発
- 中央標準の再設計
- 手順A・手順B・LEARNINGという利用区分の提供。正式 Purpose の変更は対象外である
- 利用先に既にある設定ファイルの削除
- 中央管理コピーの修正と再配布

---

## 4. Assumptions（前提条件）

- 利用者は 2026-10-09 に正式 Purpose を DISTRIBUTION と確定した。2026-10-10 の目的文の訂正は、この Purpose を変えない。
- 手順Aのみを今期の提供区分とする方針は、2026-10-10 の指示で撤回済みである。初期値は、既存文書ID、自分のOwner、初期化日のCreated Date / Last Updated、Version 0.1、Status Draftとする。配布テンプレートの Version とは区別する。
- 設計内容と承認は、利用先リポジトリの持ち主が判断する。AIは未決事項や承認実績を推測しない。
- 設定ファイルが既にある利用先では、その現行ルールを読む。削除や無視は案内しない。配布元自身は既存管理ルールで運用を続ける。
- この準備工程では、公開範囲は Private を維持する。元の専用 Repository を非公開のまま保つ。
- 配布テンプレートの中央正本は `solacom_main` の `docs/standards/templates/design/` である。確認済みコミットは `16c44976638b48c53ef16399b1d51217c540be0a` である。

---

## 5. Definition Details（定義内容）

### 5.1 Background and Purpose（背景・課題・目的）

開発目的は §1 の目的文と同一である。

> SDD（仕様駆動開発）で、AIが作成する設計文書を決まった7文書・決まった節へ収め、重複と冗長化を防ぐためのテンプレートを配布する。生徒は自分のリポジトリに配置して使う。

専用の非公開 Repository は公開しない。生徒は、各文書の役割、取得するファイル、保存先、設定がなくても使える指示、仕様変更から実装までの接続を理解できる必要がある。7文書の効果は、記載先の指定、参照関係の維持、人による確認を運用して得る。参考資料は、設定の有無に応じた使用方法を説明し、使用説明書の指示例を全文では再掲しない。

### 5.2 Stakeholders（ステークホルダー一覧と関心事）

| Stakeholder（ステークホルダー） | Interests and Requests（関心事・要求） |
|---|---|
| 配布元の管理者 Takashi Oikawa | 専用の非公開 Repository を公開せず、テンプレート、使用説明書、参考資料を渡す。配布元の管理ルールは維持する。 |
| 利用先の持ち主（生徒） | テンプレートを取得し、自分のプロジェクトの設計書を記入する。設計内容と承認を判断する。設定ファイルの導入有無を決める。 |
| Cursor | 指示範囲で作業する。 |

### 5.3 User Stories and Use Cases（ユーザーストーリー・ユースケース概要）

仕様 ID は採番しない。既存の F/O/R 台帳はなく、本指示の範囲で新規採番しない。

| ID | User Story / Use Case（ユーザーストーリー / ユースケース） |
|---|---|
| — | 生徒が、自身のプロジェクトの設計書を作成するために、配布されたテンプレートを取得し、自分の `docs/design/` に置いて記入する。 |
| — | 生徒が、各文書の役割、取得ファイル、保存先、設定なしの指示、仕様変更後の実装を理解する。設計内容は持ち主が承認する。 |

### 5.4 Constraints（制約条件）

予算、公開日、人数は未指定である。未指定であることを確定事項とし、固定値は作らない。未決仕様にはしない。

| Type（種別） | Constraint（制約内容） |
|---|---|
| Budget（予算） | 未指定。固定値は作らない。 |
| Deadline（期限） | 公開日は未指定。人数も未指定。固定値は作らない。 |
| Technical（技術） | 未指定。固定値は作らない。 |
| Regulatory（法規） | 未指定。固定値は作らない。 |

### 5.5 Success Criteria and Acceptance Conditions（成功基準・受け入れ条件）

仕様 ID は採番しない。

| ID | Success Criteria / Acceptance Condition（成功基準・受け入れ条件） |
|---|---|
| — | 7文書を取得し、記入できる。 |
| — | 配布元の管理用設計と自分のプロジェクトを区別し、設定がなくても記入、仕様変更、実装の指示を使用説明書から確認できる。 |
| — | 参考資料へのリンクから、記載先、設定の有無、任意導入、デメリットを確認できる。 |
| — | 元の専用 Repository が非公開を維持する。 |
| — | 配布元との内容照合と公開前確認が完了している。 |

公開前確認は、現段階では未完了である。完了した事実としては記録しない。

---

## 6. Open Issues（未決事項）

本文書の範囲に未決仕様はない。理由: 本指示で指定した事項は確定事項として本文に記載した。予算、公開日、人数が未指定であることは、固定値を作らない確定事項であり、未決仕様ではない。テンプレートの空の TBD 行は、本 Repository の未決事項ではない。

| ID | Open Issue（未決事項） | Owner（担当者） | Due Date（期限） | Status（ステータス） |
|---|---|---|---|---|
| — | 未決仕様はない。理由は本節本文のとおり。 | — | — | — |

---

## 7. Handoff to Detail Design（詳細設計への引き継ぎ）

本文書では、アプリの詳細設計への引き継ぎは対象外。理由: アプリ開発は対象外である。この配布 Repository の続きは [02_REQUIREMENTS_DEFINITION.md](./02_REQUIREMENTS_DEFINITION.md) 以降に記載する。
