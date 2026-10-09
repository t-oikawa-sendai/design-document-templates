<!--
Program Name: DDT Operation and Handoff
Language: Markdown
Function: 更新、検証、レビュー、公開前確認の順と文書の受け入れ確認を定義する
Created: 2026-10-09
Last Updated: 2026-10-09
Author: Takashi Oikawa
AI: Cursor
Memo: Document ID DDT-OPS-001。Version 0.3 / Draft。正式承認ではない
-->

# Operation and Handoff Design（運用・詳細設計引き継ぎ）

<!-- Document Info（文書情報） -->
| Item（項目） | Value（値） |
|---|---|
| Document ID（文書ID） | DDT-OPS-001 |
| Version（バージョン） | 0.3 |
| Status（ステータス） | Draft |
| Created Date（作成日） | 2026-10-09 |
| Last Updated（最終更新日） | 2026-10-09 |
| Owner（管理者） | Takashi Oikawa |
| Related Documents（関連文書） | README.md / 01_REQUEST_DEFINITION.md / 05_ARCHITECTURE_DESIGN.md / [../STUDENT_USAGE_GUIDE.md](../STUDENT_USAGE_GUIDE.md) |

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

本文書は、更新、検証、レビュー、公開前確認の順と、文書の受け入れ確認を定義する。

---

## 2. Scope（対象範囲）

この配布 Repository の文書について、配布元確認から公開前確認までの順を対象とする。

---

## 3. Out of Scope（対象外範囲）

本文書では対象外。理由: アプリの単体テスト、結合テスト、運用監視は対象外である。

---

## 4. Assumptions（前提条件）

- 配布コピーは、管理文書の固有化より前に配置し、内容を照合する。
- 原本とコピーが異なれば停止する。
- 現段階は Private の準備中である。生徒が取得できる公開状態ではない。

---

## 5. Definition Details（定義内容）

### 5.1 Handoff Items to Detail Design（詳細設計への引き継ぎ事項）

仕様 ID は採番しない。次の事項は確定した引き継ぎであり、未決の業務仕様ではない。

| ID | Handoff Item（引き継ぎ事項） | Details / Background（詳細・背景） |
|---|---|---|
| — | 原本の Version 相違 | 配布元 README の一覧は 01〜06 を Version 0.1 と表示し、各文書の Document Info は Version 0.2 である。公開前に解消する。中央正本の修正と再配布は、この工程では行わない。配布コピーだけを修正しない。使用説明書の追加は、この相違の解消ではない。 |
| — | 使用説明書の追加と指摘修正 | 生徒向け使用説明書を追加し、レビューで確認した指摘を管理文書へ反映する。B の管理ルール導入経路と承認権限は、説明書の B を実際に提供するときに講師が確定する。この確定は B 利用の準備条件であり、A の設計テンプレート利用の説明を止める条件ではない。LEARNING は、先生が Purpose を LEARNING と確定した場合の手順として説明する。生徒用の管理ルール一式や installer は新設しない。 |
| — | 公開状態 | この準備工程では Private を維持する。生徒が取得できる公開状態になったとは記録しない。 |
| — | commit / push | この工程の完了に含めない。明示指示の後に行う。 |
| — | 後続工程 | 原本不一致の修正と再配布、正式承認、明示指示後の commit / push、Actions、公開内容確認、Public 変更、生徒側での取得確認は後続工程である。 |

### 5.2 Implementation Constraints and Notes（実装時の注意点・制約）

- 配布7文書の本文、日付、Owner、Status、Version、改行、相対リンクを変換しない。
- 原本とコピーが異なれば停止する。
- 原本の Version 相違を、配布コピーだけを修正して解消しない。
- `CONSTITUTION.md`、`AGENTS.md`、`docs/standards/DOCUMENT_GOVERNANCE_STANDARD.md`、validator、workflow を独自編集しない。

### 5.3 Test Policy and Acceptance Criteria（テスト方針・受け入れ基準）

| Type（種別） | Policy / Criteria（方針・基準） |
|---|---|
| Unit Test（単体テスト） | 対象外。理由: アプリの単体テストは対象外である。 |
| Integration Test（結合テスト） | 対象外。理由: アプリの結合テストは対象外である。 |
| System Test（システムテスト） | 対象外。理由: アプリのシステムテストは追加しない。 |
| Acceptance Test（受け入れテスト） | 文書の受け入れ確認を行う。配布7文書の Git Blob SHA が照合値と一致すること。原本とコピーが異なる場合は停止すること。管理用文書に未記入のテンプレート本文が残っていないこと。配布テンプレートの記入欄が保持されていること。validator を実行すること。使用説明書に、5管理文書と設計7文書の役割、AI読込みのパスと順序、初回と再開の指示文、配布元と自分のプロジェクトの区別、コピー対応表、2つのフォルダ図があること。ルート README から説明書へ、管理設計から説明書へ、設計書一覧から各文書へのリンクが利用先で成立すること。原本 README 一覧の Version 0.1 と各設計書 Version 0.2 の相違が残っている間は、整合確認完了および正式公開完了としないこと。使用説明書の追加を、この相違の解消としないこと。この準備工程を、生徒が取得できる公開状態としないこと。 |

### 5.4 Deployment and Release Overview（デプロイ・リリース手順概要）

今回の工程の作業は、使用説明書の追加、レビュー指摘の修正、検証、実差分の再提出である。原本不一致の修正と再配布、正式承認、明示指示後の commit / push、Actions、公開内容確認、Public 変更、生徒側での取得確認は後続工程である。この表は手順の定義であり、後続工程を完了した記録ではない。

| Step（ステップ） | Task（作業内容） | Owner（担当） |
|---|---|---|
| 1 | 配布元確認 | 指示範囲の作業 |
| 2 | 指定パスへ無変更コピー | 指示範囲の作業 |
| 3 | 全件内容照合 | 指示範囲の作業 |
| 4 | 使用説明書の追加と、指摘に基づく管理文書の更新 | 指示範囲の作業 |
| 5 | validator と差分検査 | 指示範囲の作業 |
| 6 | 実差分の再提出 | 指示範囲の作業。再提出はレビュー合格ではない |
| 7 | 修正後の差分レビュー | 設計担当 |
| 8 | 原本不一致の修正と再配布 | 後続工程 |
| 9 | 正式承認 | 後続工程 |
| 10 | 明示指示後の commit / push | 利用者または設計担当の明示指示がある場合のみ |
| 11 | GitHub Actions の確認 | commit / push の後 |
| 12 | 公開内容の確認と Public への変更 | Public へ変更する前 |
| 13 | 生徒側での取得確認 | 後続工程 |

### 5.5 Monitoring, Alerts, and Incident Response（監視・アラート・障害対応方針）

| Aspect（観点） | Policy / Procedure（方針・手順） |
|---|---|
| Monitoring Targets and Methods（監視対象・監視方法） | 対象外。理由: アプリの運用監視は対象外である。 |
| Alert Recipients and Conditions（アラート通知先・条件） | 対象外。理由: アプリの運用監視は対象外である。 |
| Incident Confirmation Procedure（障害確認手順） | 対象外。理由: アプリの運用監視は対象外である。 |
| Recovery Procedure（復旧手順） | 対象外。理由: アプリの運用監視は対象外である。 |
| Escalation（エスカレーション先） | 対象外。理由: アプリの運用監視は対象外である。 |

### 5.6 Operational Constraints and Maintenance（運用上の制約・定期メンテナンス）

本文書では、アプリの定期メンテナンス、バッチ、データ保持期間は対象外。理由: アプリの運用は扱わない。文書を更新するときは 5.4 の順に従う。原本とコピーが異なれば停止する。原本の Version 相違は公開前課題である。

---

## 6. Open Issues（未決事項）

本文書の範囲に未決仕様はない。理由: 5.1 の事項は確定した引き継ぎである。原本の Version 相違は公開前の修正課題であり、未決の業務仕様ではない。使用説明書の追加では解消しない。同じ課題は [CURRENT.md](../../project-notes/CURRENT.md) に記録する。テンプレートの空の TBD 行は、本 Repository の未決事項ではない。

| ID | Open Issue（未決事項） | Owner（担当者） | Due Date（期限） | Status（ステータス） |
|---|---|---|---|---|
| — | 未決仕様はない。原本の Version 相違は公開前の修正課題であり、未決の業務仕様ではない。 | — | — | — |

---

## 7. Handoff to Detail Design（詳細設計への引き継ぎ）

- 原本 README 一覧の Version 0.1 と各設計書 Version 0.2 の相違は、公開前に解消する。この工程では中央正本を修正せず、配布コピーだけも修正しない。使用説明書の追加は、この相違の解消ではない。
- この準備工程では Private を維持する。公開完了とは扱わない。
- commit / push は、明示指示の後に行う。
