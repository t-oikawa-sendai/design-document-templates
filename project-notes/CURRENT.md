<!--
Program Name: DDT CURRENT
Language: Markdown
Function: 目的、確認時点のGit反映状態、現在地点、次作業を記録する
Created: 2026-10-09
Last Updated: 2026-10-11
Author: Takashi Oikawa
AI: Cursor
Memo: Document ID DDT-CURRENT-001。Version 0.19 / Draft。正式承認ではない
-->

# CURRENT

<!-- Document Info（文書情報） -->
| Item（項目） | Value（値） |
|---|---|
| Document ID（文書ID） | DDT-CURRENT-001 |
| Version（バージョン） | 0.19 |
| Status（ステータス） | Draft |
| Created Date（作成日） | 2026-10-09 |
| Last Updated（最終更新日） | 2026-10-11 |
| Owner（管理者） | Takashi Oikawa |
| Related Documents（関連文書） | [README.md](../README.md) / [生徒向け使用説明書](../docs/STUDENT_USAGE_GUIDE.md) / [7文書管理と設定ファイルの参考資料](../docs/GOVERNED_DEVELOPMENT_GUIDE.md) / [CHANGELOG.md](../CHANGELOG.md) / [管理設計](../docs/design/README.md) |

## Purpose（目的）

DISTRIBUTION。正式 Purpose は変更しない。開発目的の正本は [要求定義](../docs/design/01_REQUEST_DEFINITION.md) §5.1 である。

手順Aのみを今期の提供区分とする方針は、現行の確定事項から撤回済みである。経緯は [CHANGELOG.md](../CHANGELOG.md) と、この編集前の CURRENT を確認できる Git 履歴を参照する。

## Completed（完了）

Governance再配布は、commit `4edcddc501ce099b2d9dd8152400c53503c3bc39`（メッセージ `docs: redistribute governance standards`）で commit し、`main` へ通常 push した。この SHA は再配布 commit である。記録作成時点の local HEAD、`origin/main`、GitHub `main` は、この SHA で一致した。この一致は、記録作成時点の確認値である。

同 SHA の Actions「Validate Documents」run `38140991881`（event: push、status: completed、conclusion: success）である。job `validate-docs` も success である。https://github.com/t-oikawa-sendai/design-document-templates/actions/runs/38140991881 この Actions 成功は、再配布 commit の検証結果である。

過去工程のレビュー資料名、ハッシュ、工程結果は、[CHANGELOG.md](../CHANGELOG.md) と、再配布 commit の親 `fa8a5a48608131edd2e16e283de73cf93f23b1c7` の履歴で確認する。

## Current（現在）

Private・Draft。正式 Purpose は DISTRIBUTION のままである。公開範囲は Private である。

再配布 commit `4edcddc501ce099b2d9dd8152400c53503c3bc39` の制御文書は、中央原本 `solacom_main` の commit `d5564ccdcfecdb485b079ec952813c31b4145822` からの無変換コピーである。バイト一致を確認した。

- `AGENTS.md` Version 1.6、blob `655831c74eb62c1d072ae3e7eea6104847703c43`
- `CONSTITUTION.md` STANDARD_VERSION 1.8、blob `481017bc141ff22668b616a668866815af0ee4aa`

この現況訂正の対象版は、`project-notes/CURRENT.md` Version 0.19 / Draft と `CHANGELOG.md` Version 0.19 / Draft である。

独立レビューでは、中央原本と DDT の制御2文書（`AGENTS.md`、`CONSTITUTION.md`）が合格である。総合は条件付き合格である。S-1 対応結果の確認が残る。repository-governance はレビュー担当の確認が未完了であり、再配布 commit `ffa743eb1f0ae1db39864c579641c17c36791134` への追加レビューが必要である。

Persona導入と公開は完了していない。正式承認、公開前確認、Public化は未完了である。

テンプレート7件と管理設計文書の更新、および保留中の 0.17 履歴は、この現況訂正に含めていない。

## Next（次）

1. 独立レビューの残件を確認する。S-1 対応結果の確認が残る。
2. repository-governance の再配布 commit `ffa743eb1f0ae1db39864c579641c17c36791134` について、レビュー担当の追加レビューが必要である。
3. 正式承認、公開前確認、Public化は未完了である。

## Blockers（阻害要因）

- S-1 対応結果の確認が残る。中央原本と DDT の制御2文書の合格、および総合の条件付き合格は、この確認の完了ではない。
- repository-governance のレビュー担当の確認は未完了である。再配布 commit `ffa743eb1f0ae1db39864c579641c17c36791134` への追加レビューが必要である。
- テンプレート7件と管理設計文書の更新、および保留中の 0.17 履歴は、この現況訂正の反映内容ではない。

## Related Decisions（関連Decision）

新しいDecision番号やF/O/R仕様IDは採番しない。目的文、SSOT、設定ファイルの任意性は [要求定義](../docs/design/01_REQUEST_DEFINITION.md)、[要件定義](../docs/design/02_REQUIREMENTS_DEFINITION.md)、[使用説明書](../docs/STUDENT_USAGE_GUIDE.md)、[参考資料](../docs/GOVERNED_DEVELOPMENT_GUIDE.md) に記録する。
