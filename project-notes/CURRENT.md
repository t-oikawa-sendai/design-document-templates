<!--
Program Name: DDT CURRENT
Language: Markdown
Function: 目的、確認時点のGit反映状態、現在地点、次作業を記録する
Created: 2026-10-09
Last Updated: 2026-10-12
Author: Takashi Oikawa
AI: Cursor
Memo: Document ID DDT-CURRENT-001。Version 0.20 / Draft。正式承認ではない。GOV-01の親は現況訂正 commit 7f6c5a6ad4c27ce75271acea068049a6e5716893 である。GOV-01の commit 識別は Git 履歴を正とする。Version 0.17の対象ファイルは未commitの保留である
-->

# CURRENT

<!-- Document Info（文書情報） -->
| Item（項目） | Value（値） |
|---|---|
| Document ID（文書ID） | DDT-CURRENT-001 |
| Version（バージョン） | 0.20 |
| Status（ステータス） | Draft |
| Created Date（作成日） | 2026-10-09 |
| Last Updated（最終更新日） | 2026-10-12 |
| Owner（管理者） | Takashi Oikawa |
| Related Documents（関連文書） | [README.md](../README.md) / [生徒向け使用説明書](../docs/STUDENT_USAGE_GUIDE.md) / [7文書管理と設定ファイルの参考資料](../docs/GOVERNED_DEVELOPMENT_GUIDE.md) / [CHANGELOG.md](../CHANGELOG.md) / [管理設計](../docs/design/README.md) |

## Purpose（目的）

DISTRIBUTION。正式 Purpose は変更しない。開発目的の正本は [要求定義](../docs/design/01_REQUEST_DEFINITION.md) §5.1 である。

手順Aのみを今期の提供区分とする方針は、現行の確定事項から撤回済みである。経緯は [CHANGELOG.md](../CHANGELOG.md) と、この編集前の CURRENT を確認できる Git 履歴を参照する。

## Completed（完了）

Governance再配布は、commit `4edcddc501ce099b2d9dd8152400c53503c3bc39`（メッセージ `docs: redistribute governance standards`）で commit し、`main` へ通常 push した。この SHA は再配布 commit である。

同 SHA の Actions「Validate Documents」run `38140991881`（event: push、status: completed、conclusion: success）である。job `validate-docs` も success である。https://github.com/t-oikawa-sendai/design-document-templates/actions/runs/38140991881 この Actions 成功は、再配布 commit の検証結果である。記録は GitHub main の Version 0.19 にある。

現況訂正は、commit `7f6c5a6ad4c27ce75271acea068049a6e5716893`（メッセージ `docs: correct recorded redistribution state`）である。GOV-01 着手時点の 2026-10-12 の実測で、local HEAD、`origin/main`、GitHub main はこの SHA で一致した。この SHA は現況訂正の commit であり、再配布 commit の後続であり、GOV-01 の親である。GOV-01 反映後の HEAD ではない。

過去工程のレビュー資料名、ハッシュ、工程結果は、[CHANGELOG.md](../CHANGELOG.md) と、再配布 commit の親 `fa8a5a48608131edd2e16e283de73cf93f23b1c7` の履歴で確認する。

## Current（現在）

Private・Draft。正式 Purpose は DISTRIBUTION のままである。公開範囲は Private である。

GOV-01 の親は、現況訂正 commit `7f6c5a6ad4c27ce75271acea068049a6e5716893` である。この SHA を GOV-01 反映後の HEAD とは扱わない。GOV-01 の commit 識別は Git 履歴を正とし、本文に commit SHA は記録しない。

再配布 commit `4edcddc501ce099b2d9dd8152400c53503c3bc39` の制御文書は、中央原本 `solacom_main` の commit `d5564ccdcfecdb485b079ec952813c31b4145822` からの無変換コピーである。バイト一致は、GitHub main の Version 0.19 に確認済みとして記録されている。

- `AGENTS.md` Version 1.6、blob `655831c74eb62c1d072ae3e7eea6104847703c43`
- `CONSTITUTION.md` STANDARD_VERSION 1.8、blob `481017bc141ff22668b616a668866815af0ee4aa`

この整合の対象版は、`project-notes/CURRENT.md` Version 0.20 / Draft と `CHANGELOG.md` Version 0.20 / Draft である。この2文書が GOV-01 の対象である。Version 0.17 の対象ファイルは GOV-01 に含めていない。2026-10-12 の作業ツリーで、`python3 scripts/validate-docs.py` は PASS、`git diff --check` は PASS である。既存の未commit差分に由来する失敗はなかった。

Claude独立レビューの記録は、GitHub main の Version 0.19 と同じ結果である。中央原本と DDT の制御2文書（`AGENTS.md`、`CONSTITUTION.md`）は合格である。総合は条件付き合格である。S-1 対応結果の確認が残る。repository-governance はレビュー担当の確認が未完了であり、再配布 commit `ffa743eb1f0ae1db39864c579641c17c36791134` への追加レビューが必要である。

Persona導入と公開は完了していない。正式承認、公開前確認、Public化は未完了である。

保留中の Version 0.17 作業は未commitのままである。対象は `docs/design/README.md`、`docs/design/01_REQUEST_DEFINITION.md`、`docs/design/03_DATA_AND_SECURITY_DESIGN.md`、`docs/design/05_ARCHITECTURE_DESIGN.md`、`templates/design/` の7文書である。この保留は GOV-01 の反映内容ではない。今回の GOV-01 は、この保留作業を再開していない。

## Next（次）

1. S-1 対応結果の確認が残る。
2. repository-governance の再配布 commit `ffa743eb1f0ae1db39864c579641c17c36791134` について、レビュー担当の追加レビューが必要である。
3. Version 0.17 の保留作業は未commitのまま残る。今回の整合では再開しない。
4. 正式承認、公開前確認、Public化は未完了である。

## Blockers（阻害要因）

- S-1 対応結果の確認が残る。中央原本と DDT の制御2文書の合格、および総合の条件付き合格は、この確認の完了ではない。
- repository-governance のレビュー担当の確認は未完了である。再配布 commit `ffa743eb1f0ae1db39864c579641c17c36791134` への追加レビューが必要である。

## Related Decisions（関連Decision）

新しいDecision番号やF/O/R仕様IDは採番しない。目的文、SSOT、設定ファイルの任意性は [要求定義](../docs/design/01_REQUEST_DEFINITION.md)、[要件定義](../docs/design/02_REQUIREMENTS_DEFINITION.md)、[使用説明書](../docs/STUDENT_USAGE_GUIDE.md)、[参考資料](../docs/GOVERNED_DEVELOPMENT_GUIDE.md) に記録する。
