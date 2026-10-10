<!--
Program Name: DDT CURRENT
Language: Markdown
Function: 目的、確認時点のGit反映状態、現在地点、次作業を記録する
Created: 2026-10-09
Last Updated: 2026-10-10
Author: Takashi Oikawa
AI: Cursor
Memo: Document ID DDT-CURRENT-001。Version 0.16 / Draft。正式承認ではない
-->

# CURRENT

<!-- Document Info（文書情報） -->
| Item（項目） | Value（値） |
|---|---|
| Document ID（文書ID） | DDT-CURRENT-001 |
| Version（バージョン） | 0.16 |
| Status（ステータス） | Draft |
| Created Date（作成日） | 2026-10-09 |
| Last Updated（最終更新日） | 2026-10-10 |
| Owner（管理者） | Takashi Oikawa |
| Related Documents（関連文書） | [README.md](../README.md) / [生徒向け使用説明書](../docs/STUDENT_USAGE_GUIDE.md) / [7文書管理と設定ファイルの参考資料](../docs/GOVERNED_DEVELOPMENT_GUIDE.md) / [CHANGELOG.md](../CHANGELOG.md) / [管理設計](../docs/design/README.md) |

## Purpose（目的）

DISTRIBUTION。正式 Purpose は変更しない。開発目的の正本は [要求定義](../docs/design/01_REQUEST_DEFINITION.md) §5.1 である。

手順Aのみを今期の提供区分とする方針は、現行の確定事項から撤回済みである。経緯は [CHANGELOG.md](../CHANGELOG.md) と、この編集前の CURRENT を確認できる Git 履歴を参照する。

## Completed（完了）

直近の GitHub 確認済み工程は、README 修正の commit `fb56e5c8daf269bc89a8973c7a61dd497f154e40`（メッセージ `docs: link each template file and state the shared method`）と、同 SHA の Actions「Validate Documents」run `38027589329` の success である。job `validate-docs` も success である。https://github.com/t-oikawa-sendai/design-document-templates/actions/runs/38027589329 この成功は、今回の重複整理の検証結果ではない。

過去工程のレビュー資料名、ハッシュ、工程結果は、[CHANGELOG.md](../CHANGELOG.md) と、commit `fb56e5c8daf269bc89a8973c7a61dd497f154e40` の `project-notes/CURRENT.md` で確認する。版数不一致の解消済み実績は、CHANGELOG の 2026-10-10 の記録（公開阻害条件から外した件）で確認する。編集前の詳細文は、同じ commit の `docs/design/06_OPERATION_AND_HANDOFF.md` §5.1 にある。

## Current（現在）

Private・Draft。正式 Purpose は DISTRIBUTION のままである。2026-10-10 の作業開始時に実測した配布先は、branch `main`、local HEAD と fetch 後の origin/main が `fb56e5c8daf269bc89a8973c7a61dd497f154e40` で一致し、作業ツリーは clean だった。公開範囲は Private である。HEAD はその後動かしていない。この整理は未commitであり、stage には載せていない。

いま行っているのは、レビューに基づく案内と管理用設計書の重複・参照の整理である。この CURRENT は、その commit 前の記録である。設計担当の実差分レビュー PASS の前には commit しない。自己検証を PASS として扱わない。今回の作業ではcommit・pushを行わない。設計担当レビュー後、利用者の明示指示を待つ。その SHA、Push 成功、Actions 成功は、この本文へ追記するための amend をしない。正式承認、独立レビュー、Public化は未実施である。

## Next（次）

1. 今回の重複整理について、配布先の設計担当の実差分レビューを受ける。自己検証を PASS として扱わない。
2. 設計担当レビュー後、利用者の明示指示を待つ。レビューPASSをcommit・pushの許可とは扱わない。
3. Push 後の SHA と Actions は最終報告で確認する。この本文へ追記するための amend はしない。
4. 独立レビュー、正式承認、公開前確認、Public化は、その後の指示で進める。

## Blockers（阻害要因）

- 独立レビュー、正式承認、Public化は未完了である。今回の作業を公開承認とは扱わない。commit `fb56e5c8daf269bc89a8973c7a61dd497f154e40` の Actions 成功は、今回の重複整理の PASS ではない。
- 今回の整理の GitHub 上の表示は未確認である。
- 自己検証は、設計担当レビュー PASS ではない。

## Related Decisions（関連Decision）

新しいDecision番号やF/O/R仕様IDは採番しない。目的文、SSOT、設定ファイルの任意性は [要求定義](../docs/design/01_REQUEST_DEFINITION.md)、[要件定義](../docs/design/02_REQUIREMENTS_DEFINITION.md)、[使用説明書](../docs/STUDENT_USAGE_GUIDE.md)、[参考資料](../docs/GOVERNED_DEVELOPMENT_GUIDE.md) に記録する。
