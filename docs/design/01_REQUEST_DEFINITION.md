<!--
Program Name: DDT Request Definition
Language: Markdown
Function: 配布Repositoryの目的、対象、成功条件を定義する
Created: 2026-10-09
Last Updated: 2026-10-09
Author: Takashi Oikawa
AI: Cursor
Memo: Document ID DDT-REQ-001。Version 0.3 / Draft。正式承認ではない
-->

# Request Definition（要求定義）

<!-- Document Info（文書情報） -->
| Item（項目） | Value（値） |
|---|---|
| Document ID（文書ID） | DDT-REQ-001 |
| Version（バージョン） | 0.3 |
| Status（ステータス） | Draft |
| Created Date（作成日） | 2026-10-09 |
| Last Updated（最終更新日） | 2026-10-09 |
| Owner（管理者） | Takashi Oikawa |
| Related Documents（関連文書） | README.md / 02_REQUIREMENTS_DEFINITION.md / [../STUDENT_USAGE_GUIDE.md](../STUDENT_USAGE_GUIDE.md) |

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

このリポジトリの目的は、生徒が自身のプロジェクトの設計書を作成するためのテンプレートの配布及び使用方法のガイドラインである。本文書は、文書の役割を定義する。専用の非公開 Repository は公開しない。生徒が、各文書の役割、取得ファイル、保存先、AIへ渡す最新資料、再開方法を理解できることを求める。

---

## 2. Scope（対象範囲）

対象は、この配布 Repository、設計書 README および 01〜06 の7テンプレート、および生徒向け使用説明書 [../STUDENT_USAGE_GUIDE.md](../STUDENT_USAGE_GUIDE.md) である。

---

## 3. Out of Scope（対象外範囲）

- 個別案件の設計実績
- AI ペルソナ
- アプリ開発
- 中央標準の再設計

---

## 4. Assumptions（前提条件）

- 利用者は 2026-10-09 に正式 Purpose を DISTRIBUTION と確定した。
- この準備工程では、公開範囲は Private を維持する。元の専用 Repository を非公開のまま保つ。
- 配布テンプレートの中央正本は `solacom_main` の `docs/standards/templates/design/` である。確認済みコミットは `16c44976638b48c53ef16399b1d51217c540be0a` である。

---

## 5. Definition Details（定義内容）

### 5.1 Background and Purpose（背景・課題・目的）

このリポジトリの目的は、生徒が自身のプロジェクトの設計書を作成するためのテンプレートの配布及び使用方法のガイドラインである。専用の非公開 Repository は公開しない。使用方法の案内は [../STUDENT_USAGE_GUIDE.md](../STUDENT_USAGE_GUIDE.md) で提供する。生徒は、各文書の役割、取得するファイル、保存先、AIへ渡す最新資料、再開方法を理解できる必要がある。

### 5.2 Stakeholders（ステークホルダー一覧と関心事）

| Stakeholder（ステークホルダー） | Interests and Requests（関心事・要求） |
|---|---|
| 管理者・講師 Takashi Oikawa | 専用の非公開 Repository を公開せず、生徒へ設計書のテンプレートを渡す。 |
| 生徒 | テンプレートを取得し、自分のプロジェクトの設計書を記入する。 |
| Cursor | 指示範囲で作業する。 |

### 5.3 User Stories and Use Cases（ユーザーストーリー・ユースケース概要）

仕様 ID は採番しない。既存の F/O/R 台帳はなく、本指示の範囲で新規採番しない。

| ID | User Story / Use Case（ユーザーストーリー / ユースケース） |
|---|---|
| — | 生徒が、自身のプロジェクトの設計書を作成するために、配布されたテンプレートを取得し、自分の `docs/design/` に置いて記入する。 |
| — | 生徒が、各文書の役割、取得ファイル、保存先、AIへ渡す最新資料、再開方法を理解する。 |

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
| — | 配布元と自分のプロジェクトを区別し、読み込み対象、順序、指示文、構成図を使用説明書から確認できる。 |
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
