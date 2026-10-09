<!--
Program Name: DDT CURRENT
Language: Markdown
Function: このRepositoryの目的、完了、現在地点、次作業、阻害要因を記録する
Created: 2026-10-09
Last Updated: 2026-10-09
Author: Takashi Oikawa
AI: Cursor
Memo: Document ID DDT-CURRENT-001。Version 0.5 / Draft。正式承認ではない
-->

# CURRENT

<!-- Document Info（文書情報） -->
| Item（項目） | Value（値） |
|---|---|
| Document ID（文書ID） | DDT-CURRENT-001 |
| Version（バージョン） | 0.5 |
| Status（ステータス） | Draft |
| Created Date（作成日） | 2026-10-09 |
| Last Updated（最終更新日） | 2026-10-09 |
| Owner（管理者） | Takashi Oikawa |
| Related Documents（関連文書） | [../README.md](../README.md) / [../docs/STUDENT_USAGE_GUIDE.md](../docs/STUDENT_USAGE_GUIDE.md) / [../CONSTITUTION.md](../CONSTITUTION.md) / [../AGENTS.md](../AGENTS.md) / [../CHANGELOG.md](../CHANGELOG.md) / [../docs/design/README.md](../docs/design/README.md) |

---

## Purpose（目的）

DISTRIBUTION。このリポジトリの目的は、生徒が自身のプロジェクトの設計書を作成するためのテンプレートの配布及び使用方法のガイドラインである。

## Completed（完了）

- 新規 Repository を Initial commit として作成した。日時は 2026-10-09 12:04:28 +0900。親コミットはない。
- GitHub の公開範囲は Private である。
- ローカル `/Users/takashioikawa/Dev/design-document-templates` へクローンした。
- local HEAD、fetch 後の origin/main、GitHub main は基準 SHA `0aa4e9e3af77688c6485035eb23b98061cd740d0` で一致した。
- 必須 Governance 文書 10 件と検証資産 2 件の配置を確認した。
- 初期状態の `python3 scripts/validate-docs.py` は終了コード 0 だった。
- 利用者は 2026-10-09 に正式 Purpose を DISTRIBUTION と確定した。
- `templates/design/` の 7 文書を基準 SHA から無変更で配置した。Git Blob SHA は指示書の照合値、および `solacom_main` コミット `16c44976638b48c53ef16399b1d51217c540be0a` の `docs/standards/templates/design/` と全件一致した。
- 初期化後の `python3 scripts/validate-docs.py` は終了コード 0、`git diff --check` は終了コード 0 だった。原本の Version 相違は未解消である。
- レビュー資料 `design-document-templates-review-20261009-135410.zip` を作成し、設計担当が受領した。SHA-256 は `b6acbe8e03cb674aed1d514f29cbe738a1452c42baba3f1fbf64239384cde516`。収録は 29 件である。
- 設計担当が実差分を確認した。指摘がある。指摘は、使用説明の不足、フォルダ構成図の不足、CHANGELOG の分類、02 の文書数の表現、01〜05 の「本节」、Private 維持の記述である。
- 2026-10-09 に `docs/STUDENT_USAGE_GUIDE.md` Version 0.1 / Draft を追加し、管理 10 文書を Version 0.2 / Draft へ更新して指摘を修正した。配布 7 文書は変更していない。原本の Version 相違は未解消である。正式承認、commit、push、公開は未実施である。
- 更新後の `python3 scripts/validate-docs.py` は終了コード 0。検査対象 20 件はすべて PASS である。対象は `CHANGELOG.md`、`README.md`、`docs/NEW_REPOSITORY_SETUP_GUIDE.md`、`docs/STUDENT_USAGE_GUIDE.md`、`docs/design/` の7文書、`docs/standards/DOCUMENT_GOVERNANCE_STANDARD.md`、`project-notes/CURRENT.md`、`templates/design/` の7文書である。`git diff --check` は終了コード 0 で、出力は空である。ヘッダー検査の PASS は、本文が正しいことではない。
- 説明書の2つの Mermaid 図と 05 の図の表示確認は未実施である。ローカルに Mermaid の表示手段はなく、表示のために依存や CI は追加していない。
- 設計担当の commit 前レビュー（DDT-REVIEW-20261009-002）は FAIL である。理由は、`docs/design/README.md` の目次第2項目のリンク先が見出しと一致しない1件である。
- 2026-10-09 に、そのリンク先だけを `#2-problem--solution--benefit-summary問題解決効果の概要` へ修正した。見出し本文は変更していない。`docs/design/README.md`、`project-notes/CURRENT.md`、`CHANGELOG.md` を Version 0.3 / Draft とした。01〜06 は 0.2 / Draft のままである。配布7文書は変更していない。
- 修正後の `python3 scripts/validate-docs.py` は終了コード 0。検査対象 20 件はすべて PASS である。`git diff --check` は終了コード 0 で、出力は空である。`git diff --cached` は空である。HEAD は基準 SHA `0aa4e9e3af77688c6485035eb23b98061cd740d0` のままである。開始 ZIP からバイトが変わったファイルは、上記3文書だけである。ヘッダー検査の PASS は、本文が正しいことではない。
- その時点では、設計担当レビュー PASS、正式承認、commit、push、公開は未実施だった。
- 設計担当の commit 前再レビュー（DDT-REVIEW-20261009-003）は、受領 ZIP `design-document-templates-anchor-review-20261009-204801.zip` の時点で PASS である。SHA-256 は `7fbfdb36ec0de6224e1fca467a9221351320a55595c8aca8c5b7acf9da758424` である。この PASS は、用語・目的文の変更前の ZIP に対する判定である。
- 2026-10-09 に、管理・案内11文書で「テンプレート」へ用語を統一し、指定の目的文を配置した。root README は Version 0.3 / Draft、管理設計 README は 0.4 / Draft、01〜06 は 0.3 / Draft、使用説明書は 0.2 / Draft、CURRENT と CHANGELOG は 0.4 / Draft である。この時点では、用語・目的文変更後のレビュー PASS、正式承認、commit、push、公開は未実施だった。
- 修正後の `python3 scripts/validate-docs.py` は終了コード 0。検査対象 20 件はすべて PASS である。`git diff --check` は終了コード 0 で、出力は空である。`git diff --cached` は空である。HEAD は基準 SHA `0aa4e9e3af77688c6485035eb23b98061cd740d0` のままである。開始 ZIP からバイトが変わったファイルは、管理・案内11文書だけである。説明書 §4.1 と管理 05 の図ラベルは一致している。Mermaid の表示確認は未実施である。ヘッダー検査の PASS は、本文が正しいことではない。

- 設計担当の用語・目的文変更後の commit 前再レビュー（DDT-REVIEW-20261009-004）は、受領 ZIP `design-document-templates-terminology-review-20261009-210139.zip` の実体確認により PASS である。SHA-256 は `9de15ad919fcce478192b4eece25c08a8d8ab435d453dad607930b42f4b03c77` である。指定11文書の変更、指定目的文、用語残存0件、配布7文書の不変、および両 patch の復元一致を確認した。
- 設計担当は同レビューで、Private・Draft の準備状態を保存する commit / push と既存 Actions 確認を明示指示した。中央原本の修正・再配布、正式承認、Mermaid 表示確認、公開前確認、Public 変更、生徒側での取得確認は完了していない。

## Current（現在）

用語・目的文変更の commit 前レビューは PASS。Private・Draft の公開前準備段階。Git の反映状態は、実際の HEAD、origin/main、GitHub main で確認する。

## Next（次）

中央原本の修正と再配布:

- 原本 README 一覧の 01〜06 が Version 0.1、個別ヘッダーが 0.2 である相違を、中央原本で修正して再配布する
- 原本 README の目次第2項目のリンク不一致を、中央原本で修正して再配布する

公開前:

- 正式承認
- 公開対象の最終差分に対する commit 前レビューと、明示指示後の commit / push
- 公開対象 commit の Actions 確認
- 公開前確認
- Public への変更
- 生徒側での取得確認

## Blockers（阻害要因）

- 配布テンプレート README の一覧は 01〜06 を Version 0.1 と表示し、各設計書の Document Info は Version 0.2 である。この Repository の配布コピーは修正しない。中央正本の修正と再配布は別工程である。
- 配布テンプレート README の目次第2項目は、見出しに対して連続ハイフンが欠ける。管理用 `docs/design/README.md` は今回修正した。原本側は中央正本の修正と再配布へ引き継ぐ。
- B の生徒向け管理ルール導入経路と承認権限の確定は、B を実際に提供するときの準備条件である。A の説明書作成を止める条件ではない。

## Related Decisions（関連Decision）

- なし。今回の確定内容は [01_REQUEST_DEFINITION.md](../docs/design/01_REQUEST_DEFINITION.md) と [02_REQUIREMENTS_DEFINITION.md](../docs/design/02_REQUIREMENTS_DEFINITION.md) に記録する。存在しない Decision 番号は記録しない。
