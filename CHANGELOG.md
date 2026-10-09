<!--
Program Name: DDT CHANGELOG
Language: Markdown
Function: design-document-templates の変更履歴正本
Created: 2026-10-09
Last Updated: 2026-10-09
Author: Takashi Oikawa
AI: Cursor
Memo: Document ID DDT-CHANGELOG-001。Version 0.7 / Draft。正式承認ではない
-->

# CHANGELOG

<!-- Document Info（文書情報） -->
| Item（項目） | Value（値） |
|---|---|
| Document ID（文書ID） | DDT-CHANGELOG-001 |
| Version（バージョン） | 0.7 |
| Status（ステータス） | Draft |
| Created Date（作成日） | 2026-10-09 |
| Last Updated（最終更新日） | 2026-10-09 |
| Owner（管理者） | Takashi Oikawa |
| Related Documents（関連文書） | [README.md](./README.md) / [docs/STUDENT_USAGE_GUIDE.md](./docs/STUDENT_USAGE_GUIDE.md) / [CONSTITUTION.md](./CONSTITUTION.md) / [AGENTS.md](./AGENTS.md) / [docs/design/README.md](./docs/design/README.md) |

---

## Purpose（目的）

本ファイルは、design-document-templates の変更履歴正本である。

この Repository で確認した事実と、この Repository で実施した事実だけを記録する。他 Repository の過去履歴は転記しない。過去履歴は独自に復元しない。

## What to Record（記録対象）

利用者・開発者・運用担当者・レビュー担当者の判断に影響する重要変更を記録する。
意味・仕様・運用・構成に影響しない軽微な変更（明白な誤字、空白調整など）は原則記録不要。

## Category Definitions（変更分類）

| Category（変更分類） | Japanese（日本語） | Usage（用途） |
|---|---|---|
| Added | 追加 | 新しい機能、章、文書、運用項目 |
| Changed | 変更 | 既存仕様、構成、手順の変更 |
| Fixed | 修正 | 誤り、不整合、不具合の修正 |
| Removed | 削除 | 機能、記述、文書の廃止 |
| Security | セキュリティ | セキュリティまたは個人情報保護上の変更 |

Git 履歴は差分確認の補助として利用する。CHANGELOG の代替とはしない。

## Change History（変更履歴）

新しい履歴を上、古い履歴を下に記載する。同日の記録は確認できた工程順で並べ、時刻不明の記録に時刻を補わない。各行のVersionは対象文書・対象工程の値であり、数値順には並べない。過去行の未実施は、その記録時点の状態を示す。

Governance 導入 Baseline は、Governance 導入成功後に記録する。
導入前に成功した事実として記録しない。

原本の Version 相違が未解消である間は、整合確認完了、正式公開完了とは記録しない。正式承認、commit、push、生徒向け公開の完了とは区別する。

| Version（バージョン） | Date（日付） | Document（文書） | Category（変更分類） | Changes（内容） | Author（作成者） |
|---|---|---|---|---|---|
| 0.7 | 2026-10-09 | project-notes/CURRENT.md、CHANGELOG.md | Changed | 受領ZIPの設計担当レビューDDT-REVIEW-20261009-005のPASSと、利用者のPush指示を記録した。中央の未同期と履歴未適用を解消し、承認済み3文書を通常pushした中央commit `93a3fce46780cf134ea0ebc4a610c96571040fd2` からの無変換再配布を確認した。本行は配布先commit前の確認記録。Private・Draftを維持し、独立レビュー・正式承認・Public化は未実施である。 | Takashi Oikawa |
| — | 2026-10-09 | project-notes/CURRENT.md、CHANGELOG.md、templates/design/ | Changed | 最終修正の実測を記録した。配布先 validator は終了コード 0、検査対象 21 件 PASS。`git diff --check` と cached check は終了コード 0、stage は空、HEAD は `c7488965f98149dc73232490e42b62f699207d93` のまま。中央テンプレート README と 04 を作業ツリーで修正し、7文書をバイトコピーした。これは再配布準備である。中央 `CHANGELOG.md` は未適用。中央の Git 反映、実差分レビュー、正式承認、commit / push、公開は未実施。Mermaid はローカル 3 図が RENDER PASS。GitHub 上の表示は未確認。 | Takashi Oikawa |
| 0.6 | 2026-10-09 | README.md、docs/STUDENT_USAGE_GUIDE.md、docs/GOVERNED_DEVELOPMENT_GUIDE.md、docs/design/、project-notes/CURRENT.md、CHANGELOG.md | Changed | 正本文書レビューに対応して手順A専用説明書へ再構成し、管理ルールの説明を講師用参考資料へ分離した。今期Aのみと初期値を反映し、用語補足・講師表記・現在状態の記録・ローカルパス表記を修正した。今回の実差分レビュー、正式承認、commit / push、公開は未実施。中央原本の修正と再配布の実行結果は別途検証して記録する。 | Takashi Oikawa |
| — | 2026-10-09 | Repository Git反映 | Fixed | GH007への対処としてメールだけをnoreplyへ変更し、Tree等を維持したcommit `c7488965f98149dc73232490e42b62f699207d93` の通常pushに成功した。local HEAD・origin/main・GitHub mainは同SHAで一致、Actions Validate Documents successと報告された。今回の再構成より前の確認記録。 | Takashi Oikawa |
| 0.5 | 2026-10-09 | project-notes/CURRENT.md、CHANGELOG.md | Changed | 用語・目的文変更後のレビュー DDT-REVIEW-20261009-004 の PASS と、Private・Draft の準備状態に対する Git 反映指示を CURRENT へ記録し、現在地点と後続工程を更新した。両文書は Version 0.5 / Draft。正式承認・公開承認ではない。 | Takashi Oikawa |
| 0.4 | 2026-10-09 | README.md、docs/design/ の7文書、docs/STUDENT_USAGE_GUIDE.md、project-notes/CURRENT.md、CHANGELOG.md | Changed | 管理・案内11文書の用語を「テンプレート」へ統一し、指定の目的文を配置した。更新後の版は、root README 0.3 / Draft、管理設計 README 0.4 / Draft、01〜06 は 0.3 / Draft、使用説明書 0.2 / Draft、CURRENT 0.4 / Draft、CHANGELOG 0.4 / Draft である。用語・目的文変更後のレビュー PASS、正式承認、commit、push、公開は未実施である。 | Takashi Oikawa |
| 0.3 | 2026-10-09 | docs/design/README.md、project-notes/CURRENT.md、CHANGELOG.md | Fixed | 管理用設計 README の目次第2項目のリンク先を、見出しに対応する `#2-problem--solution--benefit-summary問題解決効果の概要` へ修正した。レビュー判定と実施状態の記録を更新した。3文書は Version 0.3 / Draft である。設計担当レビュー PASS、正式承認、commit、push、公開は未実施である。 | Takashi Oikawa |
| 0.2 | 2026-10-09 | README.md、project-notes/CURRENT.md、docs/design/ の7文書 | Changed | 使用説明書への案内、文書の役割、AI読込み、フォルダ構成、利用手順を更新し、Version 0.2 / Draft とした。この準備工程では Private を維持する。正式承認ではない。 | Takashi Oikawa |
| 0.1 | 2026-10-09 | docs/STUDENT_USAGE_GUIDE.md | Added | 生徒向け使用説明書の初版 Version 0.1 / Draft を追加した。設計テンプレート7文書とは別の案内文書である。正式承認、commit、push、生徒向け公開は未実施である。 | Takashi Oikawa |
| 0.2 | 2026-10-09 | CHANGELOG.md、docs/design/02_REQUIREMENTS_DEFINITION.md、docs/design/03_DATA_AND_SECURITY_DESIGN.md | Fixed | 変更分類を Added / Changed / Fixed / Removed / Security の5値へ戻した。確定した文書数と、未指定の人数・業務データ件数を区別した。CHANGELOG は Version 0.2 / Draft である。原本の Version 相違は未解消である。 | Takashi Oikawa |
| 0.1 | 2026-10-09 | README.md、project-notes/CURRENT.md、CHANGELOG.md、docs/design/ の7文書 | Added | Repository 固有文書10件を、新しい文書 ID の初版 Version 0.1 / Draft として作成した。旧 Template の Approved と過去日付は、この文書 ID の承認実績として引き継いでいない。 | Takashi Oikawa |
| 0.4 / 0.2 | 2026-10-09 | templates/design/ の7文書 | Added | 基準 SHA `0aa4e9e3af77688c6485035eb23b98061cd740d0` の `docs/design/` 7文書を、`templates/design/` へ無変更で追加した。Git Blob SHA は指示書の照合値、および `solacom_main` コミット `16c44976638b48c53ef16399b1d51217c540be0a` の `docs/standards/templates/design/` と全件一致した。README の文書 Version は 0.4、01〜06 は 0.2 のままである。原本 README 一覧の Version 0.1 と各設計書 Version 0.2 の相違は残っている。 | Takashi Oikawa |
| — | 2026-10-09 12:04:28 +0900 | Repository 初期コミット | Added | Initial commit。親コミットはない。この日時は、後続の確認日・検証日とは別である。Git の作成者名は `oikawa@sendai` である。 | oikawa@sendai |
