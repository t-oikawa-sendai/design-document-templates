<!--
Program Name: DDT Requirements Definition
Language: Markdown
Function: 配布物、取得と利用の案内、検証要件を定義する
Created: 2026-10-09
Last Updated: 2026-10-10
Author: Takashi Oikawa
AI: Cursor
Memo: Document ID DDT-REQS-001。Version 0.6 / Draft。正式承認ではない
-->

# Requirements Definition（要件定義）

<!-- Document Info（文書情報） -->
| Item（項目） | Value（値） |
|---|---|
| Document ID（文書ID） | DDT-REQS-001 |
| Version（バージョン） | 0.6 |
| Status（ステータス） | Draft |
| Created Date（作成日） | 2026-10-09 |
| Last Updated（最終更新日） | 2026-10-10 |
| Owner（管理者） | Takashi Oikawa |
| Related Documents（関連文書） | README.md / 01_REQUEST_DEFINITION.md / 03_DATA_AND_SECURITY_DESIGN.md / 04_UI_AND_FLOW_DESIGN.md / 05_ARCHITECTURE_DESIGN.md / [../STUDENT_USAGE_GUIDE.md](../STUDENT_USAGE_GUIDE.md) / [../GOVERNED_DEVELOPMENT_GUIDE.md](../GOVERNED_DEVELOPMENT_GUIDE.md) |

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

本文書は、配布物、取得と利用の案内、検証要件を定義する。配布の目的文は [01_REQUEST_DEFINITION.md](./01_REQUEST_DEFINITION.md) と同一である。

> SDD（仕様駆動開発）で、AIが作成する設計文書を決まった7文書・決まった節へ収め、重複と冗長化を防ぐためのテンプレートを配布する。生徒は自分のリポジトリに配置して使う。

SDDは、仕様書を先に書き、AIはその仕様に従って実装する進め方である。同じ仕様は正本を一つにし、他からは参照する（SSOT）。設定ファイルは利用先で任意であり、不在を導入違反にしない。参考資料 [../GOVERNED_DEVELOPMENT_GUIDE.md](../GOVERNED_DEVELOPMENT_GUIDE.md) に使用方法を記載し、root README と使用説明書から参照する。指示例の全文は使用説明書を正本とし、参考資料へ再掲しない。

---

## 2. Scope（対象範囲）

- root README から使用説明書、7テンプレート、参考資料へ到達できること
- 文書の説明、設定なしで完結する記入・仕様変更・実装の指示、フォルダ図、確認の方法を提供すること
- 利用先 `docs/design/` への配置を案内すること
- 管理用文書と配布物を分けること
- 元 Repository の具体的な業務情報を配布しないこと
- コピー照合、validator、差分レビューを行うこと

---

## 3. Out of Scope（対象外範囲）

- 独自 GUI
- 独自 API
- DB
- 生徒向け配布ZIP生成、ダウンロード自動化、GitHub Template 設定。これらは本指示の範囲に含めない。Repository 外へレビュー資料を出力する作業とは区別する

---

## 4. Assumptions（前提条件）

配布形式は、この工程では Markdown ファイルである。

---

## 5. Definition Details（定義内容）

### 5.1 Functional Requirements（機能要件一覧）

仕様 ID は採番しない。優先度の固定値は作らない。

| ID | Feature Name（機能名） | Priority（優先度） | Details（詳細） |
|---|---|---|---|
| — | root README から使用説明書と7テンプレートへ到達できる | 指定なし | 掲載内容と重複の扱いは、本節の Root README Content と Duplication Handling に定義する。以前の、役割一覧を置かずリンクだけにする制約、および3手順の早見に限定する制約は、この定義で置き換える。 |
| — | 文書の説明、指示文、フォルダ図、確認 | 指定なし | 使用説明書に、同一の目的文、用語ミニ辞典、設計7文書の役割、取得と配置、初期値表、リンクと画像、設定なしで使える3場面の指示例を各1つ記載する。設定ファイルの不在を停止理由にしない。手順A・手順B・LEARNINGの利用区分、授業・課題・演習・今期を前提にした本文、修正済み未公開版の不具合FAQは置かない。任意の設定導入は参考資料へリンクする。 |
| — | 利用先への配置を案内する | 指定なし | 自分のプロジェクトの `docs/design/` に README と 01〜06 を同じ階層で置く案内をする。 |
| — | 管理用文書と配布物を分ける | 指定なし | 管理用設計書は `docs/design/`、生徒向け配布物は `templates/design/` とする。 |
| — | 元 Repository の業務情報を配布しない | 指定なし | 元 Repository の具体的な業務情報を配布しない。 |
| — | コピー照合、validator、差分レビュー | 指定なし | 配布コピーの内容照合、validator、差分レビューを行う。 |

#### Root README Content（ルートREADMEの掲載内容）

ルート README のタイトルは `design-document-templates（SDD設計文書テンプレート集）` とする。紹介文は「及川Styleの設計文書管理方式に基づく、7文書構成のテンプレート集です。」とする。業界標準を意味する「標準」、および「及川式」へは変更しない。

文書情報表は維持する。Document ID、Created Date、Owner、Status Draft は維持する。Version と Last Updated は、文書を更新したときの既存の版規則に従って更新する。ヘッダ構造の変更と一括削除は行わない。

本文は次の節とする。

1. Project Overview（概要）。対象は、自分の開発で AI に設計文書を作成・更新させる人である。7文書のテンプレートと使用方法を提供し、既存の設計書を整理する場合と、これから設計を始める場合の両方を対象とする。目的文は [01_REQUEST_DEFINITION.md](./01_REQUEST_DEFINITION.md) §5.1 の原文引用とする。SDD は、先に仕様を定め、その仕様に従って AI に実装させる進め方であると説明する。
2. Problem / Solution / Benefit Summary（問題・解決・効果の概要）。現在の問題、解決方針、期待効果を表で示す。SSOT を守ることを述べ、文書作成・仕様変更・実装時の管理方法と指示例は使用説明書 §6 を参照する。
3. Distribution Contents（配布内容）。設計テンプレートは設計書 README と 01〜06 の7文書である。所有者の確定判断として、7文書の名称と役割を掲載する。01 は要求定義、02 は要件定義とする。テンプレート、使用説明書、参考資料への入口を置く。
4. Getting Started（利用開始）。手順は2つまでとする。7文書を取得して自分のリポジトリの `docs/design/` に配置すること、文書情報を自分のプロジェクトに合わせて初期化することである。具体的な方法は使用説明書 §4 と §5 を参照する。配置後の進め方は、使用説明書のよくある質問 Q1 を参照する。
5. Optional Configuration Files（任意の設定ファイル）。AGENTS.md と CONSTITUTION.md の導入は任意であり、設定ファイルがなくても7文書で運用できる。7文書だけと、7文書に設定ファイルを加えた場合の利点と注意点を表で示す。役割、使用方法、製品別の対応、公式情報は参考資料を参照する。
6. Review and Approval（確認・承認）。設計内容の判断と承認は、利用先リポジトリの持ち主が行う。承認前の確認項目と文書情報の扱いは使用説明書 §5 を参照する。
7. Repository Contents（ファイル区分）。利用者向け案内、利用先へ配置する文書、配布元の管理資料、配布元の管理ルール、配布元の既存作成ガイド、履歴・検証資産を区分する。7文書を利用するために、配布元の管理用ファイルを自分のリポジトリへコピーする必要はない。
8. Change History and Owner（変更履歴・管理者）。変更履歴は CHANGELOG.md、管理者は Takashi Oikawa とする。

案内本文は「です・ます」とする。表は簡潔な表現とする。目的文は原文引用を維持する。使用説明書の各節へのリンクは、確定した見出しのアンカーを付ける。ファイル単位のリンクを、節への直接リンクとして完成扱いにしない。

#### Duplication Handling（重複の扱い）

README には、所有者の確定判断として7文書の名称と役割を掲載する。使用説明書 §3 の文書 ID、記載例、説明全文は転載しない。以前の「README には役割一覧を置かずリンクだけにする」は、名称と役割の表で置き換える。

次の詳細は、それぞれの記載先を参照し、README へ再掲しない。

| Content（内容） | Location（記載先） |
|---|---|
| 配置・初期化の詳細 | 使用説明書 §4・§5 |
| 既存設計書の移行・設計開始 | よくある質問の Q1 |
| 管理方法・AIへの指示例 | 使用説明書 §6 |
| 承認前の確認項目 | 使用説明書 §5 |
| 設定方法・製品別対応・公式情報 | 参考資料 |
| 用語辞典 | 使用説明書 §2 |

全体の管理方針を README の独立した節として再掲しない。

### 5.2 Non-Functional Requirements（非機能要件）

| Type（種別） | Requirement（要件内容） |
|---|---|
| Performance（性能） | 未指定。固定値は作らない。 |
| Availability（可用性） | 未指定。固定値は作らない。 |
| Security Requirement Level（セキュリティ要求レベル） | 元 Repository の具体的な業務情報を配布しない。資格情報を載せない。 |
| Maintainability（保守性） | コピー照合、validator、差分レビューを行う。 |
| Other（その他） | 配布形式は Markdown ファイルである。生徒向け配布ZIP生成、ダウンロード自動化、GitHub Template 設定は本指示の範囲に含めない。Repository 外へレビュー資料を出力する作業とは区別する。 |

### 5.3 Screen List（画面一覧）

| Screen ID（画面ID） | Screen Name（画面名） | Purpose / Overview（利用目的・概要） |
|---|---|---|
| — | 独自画面は提供しない | 対象外。理由: 独自 GUI は提供しない。閲覧は GitHub の README とファイル閲覧を使う。詳細は [04_UI_AND_FLOW_DESIGN.md](./04_UI_AND_FLOW_DESIGN.md)。 |

### 5.4 API Overview（API一覧の概要）

| API ID | API Name / Endpoint Overview（API名 / エンドポイント概要） | Purpose（用途） |
|---|---|---|
| — | 独自 API は提供しない | 対象外。理由: 独自 API は提供しない。 |

### 5.5 Data Overview（データ種別・件数規模の概要）

| Data Type（データ種別） | Estimated Volume（想定件数・規模） | Notes（備考） |
|---|---|---|
| Repository固有の管理・案内文書 | 12文書 | root README、CURRENT、CHANGELOG、管理設計7文書の既存10件と、使用説明書1件と参考資料1件。中央管理コピーや既存作成ガイドはこの件数に含めない |
| 配布する設計テンプレート | 7文書 | `templates/design/` のREADMEと01〜06。無変更で保持 |
| 生徒向け使用説明書 | 上記12件に含む1文書 | `docs/STUDENT_USAGE_GUIDE.md`。テンプレート7件とは別の利用資料。同じ文書をRepository全体の件数へ重複加算しない |

この12文書と、必須 Governance 文書10件は別の分類である。必須 Governance 文書10件と検証資産2件の分類・件数は変えない。未指定の人数と業務データ件数は作らない。

### 5.6 Mapping to Request Definition（要求定義との対応マッピング）

仕様 ID は採番しない。

| User Story ID（ユーザーストーリー ID） | Functional Requirement ID（対応する機能要件 ID） |
|---|---|
| — 。生徒がテンプレートを取得して記入する。 | ID は採番しない。対応する内容は、root README から7テンプレートへ到達できること、および利用先 `docs/design/` への配置を案内すること。 |
| — 。生徒が使用説明書により記入、仕様変更、実装を行う。 | ID は採番しない。対応する内容は、使用説明書への入口、3場面の指示例、参考資料へのリンクである。設定の不在は停止理由にしない。 |

---

## 6. Open Issues（未決事項）

本文書の範囲に未決仕様はない。理由: 本指示で指定した事項は確定事項として本文に記載した。性能、可用性、優先度が未指定であることは、固定値を作らない確定事項であり、未決仕様ではない。テンプレートの空の TBD 行は、本 Repository の未決事項ではない。

| ID | Open Issue（未決事項） | Owner（担当者） | Due Date（期限） | Status（ステータス） |
|---|---|---|---|---|
| — | 未決仕様はない。理由は本節本文のとおり。 | — | — | — |

---

## 7. Handoff to Detail Design（詳細設計への引き継ぎ）

アプリ実装への引き継ぎは対象外。理由: 独自 GUI、独自 API、DB は提供しない。情報の扱いの続きは [03_DATA_AND_SECURITY_DESIGN.md](./03_DATA_AND_SECURITY_DESIGN.md)、閲覧と記入の流れは [04_UI_AND_FLOW_DESIGN.md](./04_UI_AND_FLOW_DESIGN.md)、配置は [05_ARCHITECTURE_DESIGN.md](./05_ARCHITECTURE_DESIGN.md) に記載する。
