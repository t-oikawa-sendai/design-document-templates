<!--
Program Name: DDT Operation and Handoff
Language: Markdown
Function: 更新、検証、レビュー、公開前確認の順と文書の受け入れ確認を定義する
Created: 2026-10-09
Last Updated: 2026-10-10
Author: Takashi Oikawa
AI: Cursor
Memo: Document ID DDT-OPS-001。Version 0.10 / Draft。正式承認ではない
-->

# Operation and Handoff Design（運用・詳細設計引き継ぎ）

<!-- Document Info（文書情報） -->
| Item（項目） | Value（値） |
|---|---|
| Document ID（文書ID） | DDT-OPS-001 |
| Version（バージョン） | 0.10 |
| Status（ステータス） | Draft |
| Created Date（作成日） | 2026-10-09 |
| Last Updated（最終更新日） | 2026-10-10 |
| Owner（管理者） | Takashi Oikawa |
| Related Documents（関連文書） | [README.md](./README.md) / [01_REQUEST_DEFINITION.md](./01_REQUEST_DEFINITION.md) / [05_ARCHITECTURE_DESIGN.md](./05_ARCHITECTURE_DESIGN.md) / [../STUDENT_USAGE_GUIDE.md](../STUDENT_USAGE_GUIDE.md) / [../GOVERNED_DEVELOPMENT_GUIDE.md](../GOVERNED_DEVELOPMENT_GUIDE.md) |

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
- 原本とコピーが異なる場合は、[§5.2](#52-implementation-constraints-and-notes実装時の注意点制約) に従い停止する。
- 現段階は Private の準備中である。生徒が取得できる公開状態ではない。

---

## 5. Definition Details（定義内容）

### 5.1 Handoff Items to Detail Design（詳細設計への引き継ぎ事項）

仕様 ID は採番しない。次の事項は確定した引き継ぎであり、未決の業務仕様ではない。

| ID | Handoff Item（引き継ぎ事項） | Details / Background（詳細・背景） |
|---|---|---|
| — | 原本の Version 相違 | 索引と各文書の旧版数不一致は解消済みである。解消済み実績は [project-notes/CURRENT.md](../../project-notes/CURRENT.md) と [CHANGELOG.md](../../CHANGELOG.md) を参照する。現行の公開阻害条件にしない。今後の版数照合は継続する。正式承認、独立レビュー、公開前確認、Public化は未完了であり、この解消とは別である。 |
| — | 使用説明書の再構成 | 2026-10-10 の指示で、手順A・手順B・LEARNINGの利用区分は撤回済みである。使用説明書は、目的文、7文書の役割、取得と配置、初期値、設定なしの3場面の指示例を各1つ持つ。初期値は既存文書ID、自分のOwner、初期化日のCreated Date / Last Updated、Version 0.1、Status Draftとする。設定ファイルの詳細は参考資料へ置き、指示例の全文は再掲しない。正式 Purpose は DISTRIBUTION のままである。 |
| — | 公開状態 | この準備工程では Private を維持する。生徒が取得できる公開状態になったとは記録しない。 |
| — | commit / push | 明示指示がある場合に通常の方法で行う。force push は使わない。正式承認や Public 化とは別である。 |
| — | 後続工程 | 正式承認、明示指示後の commit / push、Actions、公開内容確認、Public 変更、生徒側での取得確認は後続工程である。 |

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
| Acceptance Test（受け入れテスト） | 文書の受け入れ確認を行う。掲載要件の充足は [02 §5.1](./02_REQUIREMENTS_DEFINITION.md#51-functional-requirements機能要件一覧) を参照し、本表へ再掲しない。確認項目は表の下に示す。 |

確認項目:

- 配布7文書の Git Blob SHA が照合値と一致すること。原本とコピーが異なる場合は、[§5.2](#52-implementation-constraints-and-notes実装時の注意点制約) に従い停止すること。
- 管理用文書に未記入のテンプレート本文が残っておらず、配布テンプレートの記入欄が保持されていること。
- `python3 scripts/validate-docs.py` を実行し、このコマンドと `git diff --check` の終了コードが 0 であること。
- 指定外差分が増えておらず、既存差分が保持されていること。
- ルート README から説明書へ、管理設計から説明書へ、設計書一覧から各文書へのリンクが利用先で成立すること。リンクが実際の文書と節へ接続し、確定した見出しのアンカーと一致すること。文書情報、コメント、管理索引の版数が整合していること。
- 非公開参照元が使用説明書に混在しないこと。
- 目次リンク不一致、例示IDの曖昧さが残っている間は、整合確認完了および正式公開完了としないこと。
- 解消済みの版数不一致の実績は [project-notes/CURRENT.md](../../project-notes/CURRENT.md) と [CHANGELOG.md](../../CHANGELOG.md) を参照する。その解消済みの不一致は、この公開阻害条件に含めないこと。使用説明書の追加を、この相違の解消としないこと。
- この準備工程を、生徒が取得できる公開状態としないこと。
- ローカル表示で表、見出し、リンクの構成を確認すること。
- 案内文書3件（root README、使用説明書、参考資料）の文書情報表は、現在の位置を維持し、初期状態で閉じた折りたたみ表示であること。表示名は「Document Info（文書情報）」であり、open 属性がないこと。管理用文書の文書情報表は折りたたまれていないこと。
- この確認項目の記載は、commit、push、Actions の成功を記録するものではない。

### 5.4 Deployment and Release Overview（デプロイ・リリース手順概要）

この表は手順の定義であり、各工程を完了した記録ではない。2026-10-10 の目的訂正は、明示指示により通常の commit / push までを作業範囲とする。正式承認、公開内容確認、Public 変更、生徒側での取得確認は後続工程である。

| Step（ステップ） | Task（作業内容） | Owner（担当） |
|---|---|---|
| 1 | 配布元確認 | 指示範囲の作業 |
| 2 | 指定パスへ無変更コピー | 指示範囲の作業 |
| 3 | 全件内容照合 | 指示範囲の作業 |
| 4 | 使用説明書の追加と、指摘に基づく管理文書の更新 | 指示範囲の作業 |
| 5 | validator と差分検査 | 指示範囲の作業 |
| 6 | 実差分の再提出 | 指示範囲の作業。再提出はレビュー合格ではない |
| 7 | 修正後の差分レビュー | 設計担当 |
| 8 | 原本不一致の修正と再配布 | 今回の修正範囲。中央原本の実差分レビューとGit反映を経て照合する |
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

本文書では、アプリの定期メンテナンス、バッチ、データ保持期間は対象外。理由: アプリの運用は扱わない。文書を更新するときは 5.4 の順に従う。原本とコピーが異なる場合は、[§5.2](#52-implementation-constraints-and-notes実装時の注意点制約) に従い停止する。解消済みの版数不一致は、現行の公開前課題にしない。実績は [project-notes/CURRENT.md](../../project-notes/CURRENT.md) と [CHANGELOG.md](../../CHANGELOG.md) を参照する。

### 5.7 配布元の管理と利用先の設定

過去の初期化時点の未commit・未pushという記述を現在状態として引き継がない。過去履歴は CURRENT に蓄積しない。現在のGit反映状態は、CURRENT と実際の Git で確認する。

配布元はこの Repository の既存管理ルールで運用を続ける。利用先で `AGENTS.md` と `CONSTITUTION.md` が任意であることと、配布元の必須管理資産は別である。手順A・手順B・LEARNINGの利用区分は 2026-10-10 の指示で撤回済みである。正式 Purpose は DISTRIBUTION のままである。

利用先の基本は設計7文書である。管理方式は設定の有無で変えない。設定ファイルの導入は利用先の持ち主が決める。導入する場合は、適用範囲、承認者、既存ルールとの整合を確認する。確認できない中央管理コピーをそのまま導入する手順にはしない。中央管理コピーの修正は中央原本側の手順であり、この節では行わない。共通前提、設定の有無による構成、AI への適用は [参考資料§1](../GOVERNED_DEVELOPMENT_GUIDE.md#1-管理方式の共通前提) に記載する。

非公開の原本へアクセスできない利用者も、7文書の取得、記入、仕様に従った実装を進められる。非公開の project-bootstrap や `solacom_main` を、利用先が当然に使える取得先として案内しない。使用するAIへ読むファイルを指定し、読めたことを確認する。製品が自動で読むとは扱わない。

説明の参照根拠は CONSTITUTION STANDARD_VERSION 1.7、AGENTS STANDARD_VERSION 1.5、DOCUMENT_GOVERNANCE_STANDARD 1.7 / Approved、NEW_REPOSITORY_SETUP_GUIDE 1.0 / Approved、設計テンプレート7文書、中央の DESIGN_DOCUMENT_STANDARD 0.9 / Draft、DOCUMENT_HISTORY_RULE 2.3 / Approved である。標準を利用先へ適用する範囲では、読める説明または参照用コピーを提供し、非公開リンクだけで提供済みとしない。

レビュー資料は管理側の証跡であり、生徒向け配布版ではない。既存レビューZIPの名称・SHA-256は、[CHANGELOG.md](../../CHANGELOG.md) と Git 履歴で確認する。CURRENT には過去履歴を蓄積しない。使用説明書へ載せない。レビュー提出、レビューPASS、正式承認、commit、push、Actions成功、公開は別々の状態として記録する。正式承認と Public 化は、この目的訂正の完了条件に含めない。

---

## 6. Open Issues（未決事項）

本文書の範囲に未決仕様はない。理由: 5.1 の事項は確定した引き継ぎである。解消済みの版数不一致は、未決の業務仕様でも現行の公開阻害条件でもない。解消済み実績は [project-notes/CURRENT.md](../../project-notes/CURRENT.md) と [CHANGELOG.md](../../CHANGELOG.md) を参照する。テンプレートの空の TBD 行は、本 Repository の未決事項ではない。

| ID | Open Issue（未決事項） | Owner（担当者） | Due Date（期限） | Status（ステータス） |
|---|---|---|---|---|
| — | 未決仕様はない。解消済みの版数不一致は、未決の業務仕様ではない。 | — | — | — |

---

## 7. Handoff to Detail Design（詳細設計への引き継ぎ）

- 索引と各文書の旧版数不一致は解消済みである。実績は [project-notes/CURRENT.md](../../project-notes/CURRENT.md) と [CHANGELOG.md](../../CHANGELOG.md) を参照する。現行の公開阻害条件にしない。配布コピーだけを独自に修正して版数を合わせない扱いは、[§5.2](#52-implementation-constraints-and-notes実装時の注意点制約) に従う。正式承認、独立レビュー、公開前確認、Public化は未完了である。
- この準備工程では Private を維持する。公開完了とは扱わない。
- commit / push は、明示指示の後に行う。
