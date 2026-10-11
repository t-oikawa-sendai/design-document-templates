<!--
Program Name: DDT CURRENT
Language: Markdown
Function: 目的、確認時点のGit反映状態、現在地点、次作業を記録する
Created: 2026-10-09
Last Updated: 2026-10-11
Author: Takashi Oikawa
AI: Cursor
Memo: Document ID DDT-CURRENT-001。Version 0.18 / Draft。正式承認ではない
-->

# CURRENT

<!-- Document Info（文書情報） -->
| Item（項目） | Value（値） |
|---|---|
| Document ID（文書ID） | DDT-CURRENT-001 |
| Version（バージョン） | 0.18 |
| Status（ステータス） | Draft |
| Created Date（作成日） | 2026-10-09 |
| Last Updated（最終更新日） | 2026-10-11 |
| Owner（管理者） | Takashi Oikawa |
| Related Documents（関連文書） | [README.md](../README.md) / [生徒向け使用説明書](../docs/STUDENT_USAGE_GUIDE.md) / [7文書管理と設定ファイルの参考資料](../docs/GOVERNED_DEVELOPMENT_GUIDE.md) / [CHANGELOG.md](../CHANGELOG.md) / [管理設計](../docs/design/README.md) |

## Purpose（目的）

DISTRIBUTION。正式 Purpose は変更しない。開発目的の正本は [要求定義](../docs/design/01_REQUEST_DEFINITION.md) §5.1 である。

手順Aのみを今期の提供区分とする方針は、現行の確定事項から撤回済みである。経緯は [CHANGELOG.md](../CHANGELOG.md) と、この編集前の CURRENT を確認できる Git 履歴を参照する。

## Completed（完了）

直近の Git 反映済み HEAD は `fa8a5a48608131edd2e16e283de73cf93f23b1c7`（メッセージ `docs: consolidate shared guidance and document references`）である。branch は `main` で、確認時点の `origin/main` も同じ SHA である。この SHA は、この候補の親である。この候補自身の commit SHA ではない。

過去工程のレビュー資料名、ハッシュ、工程結果は、[CHANGELOG.md](../CHANGELOG.md) と、この HEAD の履歴で確認する。

## Current（現在）

Private・Draft。正式 Purpose は DISTRIBUTION のままである。公開範囲は Private である。

この候補に含むファイルは次の4件である。

- `AGENTS.md` Version 1.6、blob `655831c74eb62c1d072ae3e7eea6104847703c43`
- `CONSTITUTION.md` STANDARD_VERSION 1.8、blob `481017bc141ff22668b616a668866815af0ee4aa`
- `CHANGELOG.md` Version 0.18 / Draft
- `project-notes/CURRENT.md` Version 0.18 / Draft

`AGENTS.md` と `CONSTITUTION.md` は、中央原本 `solacom_main` の commit `d5564ccdcfecdb485b079ec952813c31b4145822` から無変換でコピーする。バイト一致を確認した。

この候補は未commitである。commit・push、更新後 SHA の Actions、独立レビュー、Persona導入は未実施である。

作業ツリーに残っている別作業は保留中であり、この候補の内容ではない。テンプレート7件と管理設計文書の更新は、この候補に含めていない。未commitの 0.17 履歴は、反映済み履歴としてこの候補に入れていない。

候補4ファイルを基点コミットのツリーへ重ねた検証用ツリーの local validator は PASS である。この結果は、作業ツリー上の別作業の検証結果ではない。

## Next（次）

1. この候補の差分を確認する。
2. 作業ツリーを上書きせず、この候補の4ファイルだけを stage する手順は、別指示の後に実行する。
3. commit・push は、その後の明示指示を待つ。
4. 独立レビュー、正式承認、公開前確認、Public化は未完了である。

## Blockers（阻害要因）

- この候補の commit・push、更新後 SHA の Actions、独立レビュー、Persona導入は未実施である。候補の作成は、これらの完了ではない。
- 作業ツリー上の別作業は保留中である。この候補は、その別作業の完了記録ではない。

## Related Decisions（関連Decision）

新しいDecision番号やF/O/R仕様IDは採番しない。目的文、SSOT、設定ファイルの任意性は [要求定義](../docs/design/01_REQUEST_DEFINITION.md)、[要件定義](../docs/design/02_REQUIREMENTS_DEFINITION.md)、[使用説明書](../docs/STUDENT_USAGE_GUIDE.md)、[参考資料](../docs/GOVERNED_DEVELOPMENT_GUIDE.md) に記録する。
