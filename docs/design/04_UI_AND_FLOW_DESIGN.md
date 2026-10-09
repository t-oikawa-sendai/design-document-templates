<!--
Program Name: DDT UI and Flow Design
Language: Markdown
Function: GitHub上の閲覧、コピー、記入の流れを定義する
Created: 2026-10-09
Last Updated: 2026-10-09
Author: Takashi Oikawa
AI: Cursor
Memo: Document ID DDT-UI-001。Version 0.4 / Draft。正式承認ではない
-->

# UI and Flow Design（UI・フロー設計）

<!-- Document Info（文書情報） -->
| Item（項目） | Value（値） |
|---|---|
| Document ID（文書ID） | DDT-UI-001 |
| Version（バージョン） | 0.4 |
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

本文書は、GitHub 上での閲覧、テンプレートの取得、記入の流れを定義する。独自 GUI は提供しない。

---

## 2. Scope（対象範囲）

生徒の流れは、ルート README から使用説明書を読むこと、今期の手順Aと初期値の確認、7テンプレートの取得と自分の `docs/design/` への配置、課題文と自分の最新文書を AI へ渡すこと、読めた資料と未読資料の確認、設計書の記入、一覧・参照・図の確認、決定済み・未決・次回の相談事項の記録である。フォルダ構成図と指示文の詳細は [../STUDENT_USAGE_GUIDE.md](../STUDENT_USAGE_GUIDE.md) を参照する。閲覧は GitHub の README とファイル閲覧を使う。独自 GUI は提供しない。

---

## 3. Out of Scope（対象外範囲）

- 独自の画面項目
- ワイヤーフレーム
- アプリの入力検証
- アプリのエラー画面
- 画像の新規作成

---

## 4. Assumptions（前提条件）

閲覧は GitHub の README とファイル閲覧を使う。この Repository の独自 GUI はない。

---

## 5. Definition Details（定義内容）

### 5.1 Screen List — Detail Definition（画面一覧・詳細定義）

画面 ID は採番しない。独自の画面項目は定義しない。

| Screen ID（画面ID） | Screen Name（画面名） | Input Items（入力項目） | Output Items（出力項目） | Main Operations（主要操作） | Notes（備考） |
|---|---|---|---|---|---|
| — | 独自画面は定義しない | 対象外。理由: 独自の画面項目は定義しない。 | 対象外。理由: 独自の画面項目は定義しない。 | GitHub の README とファイル閲覧を利用する。 | 独自 GUI は提供しない。 |

### 5.2 Screen Transition and Business Flow（画面遷移図・業務フロー）

画面遷移図は作成しない。理由: 独自 GUI は提供しない。生徒の流れは次のとおりである。フォルダ構成図と指示文の詳細は [../STUDENT_USAGE_GUIDE.md](../STUDENT_USAGE_GUIDE.md) を参照する。

1. ルートREADMEから使用説明書を読む。
2. 今期の手順Aと初期値を確認する。
3. 7テンプレートを取得し、自分の `docs/design/` へ配置する。
4. 課題文と自分の最新文書を、該当する一覧・順序でAIへ渡す。
5. 読めた資料・未読資料を確認して設計書を記入する。
6. 一覧・参照・図と今回の設計内容を確認する。
7. 決定済み・未決・次回の相談事項を記録して、次のAIへ渡す。

### 5.3 Wireframes and Layout Policy（主要画面のワイヤーフレーム・レイアウト方針）

#### Out of Scope（対象外）

本文書では対象外。理由: 独自のワイヤーフレームは提供しない。画像は新規作成しない。

### 5.4 Operation Flow and User Scenarios（操作フロー・ユーザーシナリオ）

シナリオ ID は採番しない。

| Scenario ID（シナリオID） | Operation Name（操作名） | Steps（操作手順） |
|---|---|---|
| — | 説明書を使ってテンプレートを記入する | 1. ルートREADMEから使用説明書を読む。2. 今期の手順Aと初期値を確認する。3. 7テンプレートを取得し、自分の `docs/design/` へ配置する。4. 課題文と自分の最新文書を、該当する一覧・順序でAIへ渡す。5. 読めた資料・未読資料を確認して設計書を記入する。6. 一覧・参照・図と今回の設計内容を確認する。7. 決定済み・未決・次回の相談事項を記録して、次のAIへ渡す。 |

### 5.5 Validation and Error Handling Policy（バリデーション・エラーハンドリング方針 / UI層）

| Target（対象） | Validation Rules（バリデーションルール） | Error Message / Display Policy（エラーメッセージ・表示方針） |
|---|---|---|
| アプリの入力 | 対象外。理由: アプリの入力検証は提供しない。 | 対象外。理由: アプリのエラー画面は提供しない。 |

### 5.6 Accessibility and Responsive Design Policy（アクセシビリティ・レスポンシブ対応方針）

本文書では対象外。理由: 独自 GUI を提供しない。

---

## 6. Open Issues（未決事項）

本文書の範囲に未決仕様はない。理由: 本指示で指定した流れは確定事項として本文に記載した。独自画面を提供しないことは未決ではない。テンプレートの空の TBD 行は、本 Repository の未決事項ではない。

| ID | Open Issue（未決事項） | Owner（担当者） | Due Date（期限） | Status（ステータス） |
|---|---|---|---|---|
| — | 未決仕様はない。理由は本節本文のとおり。 | — | — | — |

---

## 7. Handoff to Detail Design（詳細設計への引き継ぎ）

アプリ実装への引き継ぎは対象外。理由: 独自 GUI は実装しない。生徒の操作は GitHub の README とファイル閲覧で行う。
