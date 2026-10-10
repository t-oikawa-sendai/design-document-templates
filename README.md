<!--
Program Name: DDT Root README
Language: Markdown
Function: 配布入口、利用早見、7文書管理の概要を示す
Created: 2026-10-09
Last Updated: 2026-10-10
Author: Takashi Oikawa
AI: Cursor
Memo: Document ID DDT-README-001。Version 0.11 / Draft。正式承認ではない
-->

# design-document-templates（SDD設計文書テンプレート集）

> 及川Styleの設計文書管理方式に基づく、7文書構成のテンプレート集です。

<details>
<summary>Document Info（文書情報）</summary>

<!-- Document Info（文書情報） -->
| Item（項目） | Value（値） |
|---|---|
| Document ID（文書ID） | DDT-README-001 |
| Version（バージョン） | 0.11 |
| Status（ステータス） | Draft |
| Created Date（作成日） | 2026-10-09 |
| Last Updated（最終更新日） | 2026-10-10 |
| Owner（管理者） | Takashi Oikawa |
| Related Documents（関連文書） | [CHANGELOG.md](./CHANGELOG.md) / [使用説明書](./docs/STUDENT_USAGE_GUIDE.md) / [設計テンプレート](./templates/design/README.md) / [7文書管理と設定ファイルの参考資料](./docs/GOVERNED_DEVELOPMENT_GUIDE.md) |

</details>

## 1. Project Overview（概要）

自分の開発でAIに設計文書を作成・更新させる方に向けて、7文書のテンプレートと使用方法を提供します。既存の設計書を整理する場合と、これから設計を始める場合の両方で使えます。

目的文は、[管理用要求定義書](./docs/design/01_REQUEST_DEFINITION.md#51-background-and-purpose背景課題目的) §5.1からの引用です。

> SDD（仕様駆動開発）で、AIが作成する設計文書を決まった7文書・決まった節へ収め、重複と冗長化を防ぐためのテンプレートを配布する。生徒は自分のリポジトリに配置して使う。

SDD（Spec-Driven Development／仕様駆動開発）は、先に仕様を定め、その仕様に従ってAIに実装させる進め方です。

## 2. Problem / Solution / Benefit Summary（問題・解決・効果の概要）

| Item（項目） | Summary（概要） |
|---|---|
| Current Problems（現在の問題） | 設計書をAI任せにすると、似た内容の「設計文書もどき」が大量に生成され、どれが正しい仕様か分からなくなることがあります。 |
| Solution Approach（解決方針） | 記載先を7文書の決まった節に収め、同じ仕様は一つの箇所を正本として管理し、他の箇所から参照します。 |
| Expected Benefits（期待効果） | 文書の乱立・重複・矛盾を抑え、仕様の所在、変更箇所、実装との対応を確認しやすくします。 |

この管理方法により、SSOT（正しい情報の管理元を一つに定める原則）を守ります。

文書作成・仕様変更・実装時の管理方法と指示例は、[使用説明書§6](./docs/STUDENT_USAGE_GUIDE.md#6-aiへの指示)を参照してください。

## 3. Distribution Contents（配布内容）

設計テンプレートは、設計書READMEと01〜06の7文書です。

| Document（文書） | File（ファイル） | Role（役割） |
|---|---|---|
| 設計書README | [`README.md`](templates/design/README.md) | 設計全体の概要と各文書への入口 |
| 01 要求定義 | [`01_REQUEST_DEFINITION.md`](templates/design/01_REQUEST_DEFINITION.md) | 背景、解決したい問題、開発目的、成功基準 |
| 02 要件定義 | [`02_REQUIREMENTS_DEFINITION.md`](templates/design/02_REQUIREMENTS_DEFINITION.md) | 実現する機能、品質条件、制約 |
| 03 データ・セキュリティ設計 | [`03_DATA_AND_SECURITY_DESIGN.md`](templates/design/03_DATA_AND_SECURITY_DESIGN.md) | データ構造、操作権限、情報の保護 |
| 04 UI・フロー設計 | [`04_UI_AND_FLOW_DESIGN.md`](templates/design/04_UI_AND_FLOW_DESIGN.md) | 画面、操作、処理の流れ |
| 05 アーキテクチャ設計 | [`05_ARCHITECTURE_DESIGN.md`](templates/design/05_ARCHITECTURE_DESIGN.md) | システム構成と各部分の責務 |
| 06 運用・詳細設計引き継ぎ | [`06_OPERATION_AND_HANDOFF.md`](templates/design/06_OPERATION_AND_HANDOFF.md) | 実装への引き継ぎ、テスト、運用 |

- テンプレート：[templates/design/](./templates/design/README.md)
- 記入・使用方法：[使用説明書](./docs/STUDENT_USAGE_GUIDE.md)
- 任意の設定ファイルの使用方法：[参考資料](./docs/GOVERNED_DEVELOPMENT_GUIDE.md)

## 4. Getting Started（利用開始）

1. templates/design/ の7文書を取得し、自分のリポジトリの docs/design/ に配置します。
2. 文書情報を自分のプロジェクトに合わせて初期化します。

具体的な方法は、使用説明書の[§4「取得と配置」](./docs/STUDENT_USAGE_GUIDE.md#4-取得と配置)と[§5「自分の文書にする」](./docs/STUDENT_USAGE_GUIDE.md#5-自分の文書にする)を参照してください。

配置後の進め方は、[よくある質問のQ1](./docs/STUDENT_USAGE_GUIDE.md#q1-how-do-i-start既存の設計書がある場合これから設計する場合はどう始めますか)を参照してください。

## 5. Optional Configuration Files（任意の設定ファイル）

AGENTS.md はAIへの作業指示、CONSTITUTION.md はプロジェクトの管理規則を記載するファイルです。利用は任意ですが、設定ファイルの有無にかかわらず、同じ7文書管理方式を適用します。

| Configuration（構成） | Benefits（メリット） | Considerations（注意点） |
|---|---|---|
| 7文書 | 仕様の記載先が決まり、文書の乱立・重複を抑えられます。 | 作業時に管理方法をAIへ伝え、文書間の整合を確認する必要があります。 |
| 7文書＋設定ファイル | 共通ルールをまとめ、毎回の指示を短くし、引き継ぎを行いやすくします。 | 設定の理解・更新と、AIへの適用確認が必要です。 |

共通前提は、[参考資料§1 管理方式の共通前提](./docs/GOVERNED_DEVELOPMENT_GUIDE.md#1-管理方式の共通前提)を参照してください。製品別の対応と公式情報は、[参考資料§8](./docs/GOVERNED_DEVELOPMENT_GUIDE.md#8-使用するaiごとの設定方法と公式情報)を参照してください。

## 6. Review and Approval（確認・承認）

設計内容の判断と承認は、利用先リポジトリの持ち主が行います。

承認前の確認項目と文書情報の扱いは、[使用説明書§5](./docs/STUDENT_USAGE_GUIDE.md#5-自分の文書にする)を参照してください。

## 7. Repository Contents（ファイル区分）

| Category（区分） | Files（ファイル） | Purpose（用途） |
|---|---|---|
| 利用者向け案内 | ルートREADME、使用説明書、参考資料 | この配布物の概要と使用方法 |
| 利用先へ配置する文書 | templates/design/の7文書 | 自分の開発の設計文書 |
| 配布元の管理資料 | docs/design/、project-notes/CURRENT.md | 配布リポジトリ自体の設計と現在状態 |
| 配布元の管理ルール | AGENTS.md、CONSTITUTION.md、docs/standards/ | 配布元の作業・文書管理 |
| 配布元の既存作成ガイド | docs/NEW_REPOSITORY_SETUP_GUIDE.md | 配布元が管理するリポジトリ作成手順 |
| 履歴・検証資産 | CHANGELOG.md、scripts/、.github/workflows/ | 配布物の変更履歴と検証 |

7文書を利用するために、配布元の管理用ファイルを自分のリポジトリへコピーする必要はありません。

## 8. Change History and Owner（変更履歴・管理者）

- 変更履歴：[CHANGELOG.md](./CHANGELOG.md)
- 管理者：Takashi Oikawa
