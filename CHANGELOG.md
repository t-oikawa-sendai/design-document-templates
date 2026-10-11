<!--
Program Name: DDT CHANGELOG
Language: Markdown
Function: design-document-templates の変更履歴正本
Created: 2026-10-09
Last Updated: 2026-10-11
Author: Takashi Oikawa
AI: Cursor
Memo: Document ID DDT-CHANGELOG-001。Version 0.19 / Draft。正式承認ではない
-->

# CHANGELOG

<!-- Document Info（文書情報） -->
| Item（項目） | Value（値） |
|---|---|
| Document ID（文書ID） | DDT-CHANGELOG-001 |
| Version（バージョン） | 0.19 |
| Status（ステータス） | Draft |
| Created Date（作成日） | 2026-10-09 |
| Last Updated（最終更新日） | 2026-10-11 |
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
| 0.19 | 2026-10-11 | project-notes/CURRENT.md、CHANGELOG.md | Fixed | 再配布 commit `4edcddc501ce099b2d9dd8152400c53503c3bc39`（メッセージ `docs: redistribute governance standards`）の後に残っていた CURRENT の現況を訂正した。対象版は CURRENT 0.19、CHANGELOG 0.19、いずれも Draft。再配布はその commit で commit し、`main` へ通常 push 済みである。記録作成時点の local HEAD、origin/main、GitHub main は同 SHA で一致した。この SHA は再配布 commit および記録作成時点の確認値である。同 SHA の Actions「Validate Documents」run `38140991881` は success、job `validate-docs` も success である。https://github.com/t-oikawa-sendai/design-document-templates/actions/runs/38140991881 この Actions 成功は再配布 commit の検証結果である。独立レビューは、中央原本と DDT の制御2文書（AGENTS.md、CONSTITUTION.md）が合格、総合は条件付き合格であり、S-1 対応結果の確認が残る。repository-governance のレビュー担当の確認は未完了であり、再配布 commit `ffa743eb1f0ae1db39864c579641c17c36791134` への追加レビューが必要である。Persona導入と公開の完了は記録しない。保留中のテンプレート7件、管理設計文書、0.17 履歴は、この履歴に含めていない。過去行の未commitは当時の記録として維持する。本行は、この訂正の commit SHA、push 結果、再レビュー完了を含まない。 | Takashi Oikawa |
| 0.18 | 2026-10-11 | AGENTS.md、CONSTITUTION.md、project-notes/CURRENT.md、CHANGELOG.md | Changed | 中央原本 `solacom_main` の commit `d5564ccdcfecdb485b079ec952813c31b4145822` から、`docs/standards/project-bootstrap/AGENTS_SOURCE.md` を `/AGENTS.md` へ、`docs/standards/project-bootstrap/CONSTITUTION.md` を `/CONSTITUTION.md` へ無変換でコピーした。AGENTS は Version 1.6、blob `655831c74eb62c1d072ae3e7eea6104847703c43`。CONSTITUTION は STANDARD_VERSION 1.8、blob `481017bc141ff22668b616a668866815af0ee4aa`。バイト一致を確認した。この候補に含む文書は AGENTS.md、CONSTITUTION.md、CHANGELOG.md、project-notes/CURRENT.md の4件である。版は CURRENT 0.18、CHANGELOG 0.18、いずれも Draft。記録時点の実 HEAD は `fa8a5a48608131edd2e16e283de73cf93f23b1c7` であり、この候補の親である。この候補自身は未commitである。commit・push、更新後 SHA の Actions、独立レビュー、Persona導入は未実施である。作業ツリーに残る別作業は保留中であり、この候補の反映内容ではない。未commitの 0.17 履歴は、反映済み履歴としてこの候補に入れていない。テンプレート7件と管理設計文書の更新は、この候補に含めていない。候補4ファイルを基点コミットのツリーへ重ねた検証用ツリーの local validator は PASS である。この結果は、作業ツリー上の別作業の検証結果ではない。 | Takashi Oikawa |
| 0.16 | 2026-10-10 | project-notes/CURRENT.md、CHANGELOG.md | Fixed | 今回のcommit・push許可に関する誤記を訂正した。今回の作業ではcommit・pushを行わない。設計担当レビュー後、利用者の明示指示を待つ。レビューPASSをcommit・pushの許可とは扱わない。版は CURRENT 0.16、CHANGELOG 0.16、いずれも Draft。他の9文書は変更していない。本行は commit 前の記録であり、今回の Push と Actions 成功は含まない。基点は配布先 `fb56e5c8daf269bc89a8973c7a61dd497f154e40`。自己検証は設計担当レビュー PASS ではない。正式承認、独立レビュー、Public化は未実施である。 | Takashi Oikawa |
| 0.15 | 2026-10-10 | README.md、docs/STUDENT_USAGE_GUIDE.md、docs/GOVERNED_DEVELOPMENT_GUIDE.md、docs/design/README.md、docs/design/01_REQUEST_DEFINITION.md、docs/design/02_REQUIREMENTS_DEFINITION.md、docs/design/03_DATA_AND_SECURITY_DESIGN.md、docs/design/04_UI_AND_FLOW_DESIGN.md、docs/design/06_OPERATION_AND_HANDOFF.md、project-notes/CURRENT.md、CHANGELOG.md | Changed | 案内の共通前提を参考資料§1へ集約し、使用説明書とルートREADMEの重複説明を参照へ置き換えた。管理用02 §5.5を12文書の内訳の記載先とし、03の内訳再掲、04 §5.4の同一手順、06の長い受け入れセルと旧§8を、参照と§5.7へ整理した。CURRENTの過去工程は、CHANGELOGと編集前のGit履歴への参照へ置き換えた。版は README 0.11、使用説明書 0.9、参考資料 0.7、管理設計 README 0.12、01 は 0.8、02 は 0.11、03 と 04 は 0.7、06 は 0.10、CURRENT 0.15、CHANGELOG 0.15、いずれも Draft。05 は 0.6 のままである。本行は commit 前の記録であり、今回の Push と Actions 成功は含まない。基点は配布先 `fb56e5c8daf269bc89a8973c7a61dd497f154e40`。同 SHA の Actions 成功は、この整理の検証結果ではない。前回の README 修正のレビュー PASS は、この修正の PASS ではない。正式承認、独立レビュー、Public化は未実施である。 | Takashi Oikawa |
| 0.14 | 2026-10-10 | README.md、docs/design/02_REQUIREMENTS_DEFINITION.md、docs/design/README.md、project-notes/CURRENT.md、CHANGELOG.md | Changed | ルート README の7文書の名称・役割表に、実ファイル名の列を追加した。各ファイル名は `templates/design/` の該当ファイルへの相対リンクである。設定ファイルの導入説明を、AGENTS.md と CONSTITUTION.md の役割、利用の任意、設定の有無にかかわらず同じ7文書管理方式を適用する文章へ置き換えた。メリット・デメリットと参考資料へのリンクは維持し、配布元の設定ファイルを利用先へコピーする案内は加えていない。版は README 0.10、02 は 0.10、管理設計 README 0.11、CURRENT 0.14、CHANGELOG 0.14、いずれも Draft。本行は commit 前の記録であり、今回の Push と Actions 成功は含まない。基点は配布先 `515f859b1368c09a47fde730bd64f9e92225be6b`。前回の文書情報表の折りたたみのレビュー PASS は、この修正の PASS ではない。正式承認、独立レビュー、Public化は未実施である。 | Takashi Oikawa |
| 0.13 | 2026-10-10 | README.md、docs/STUDENT_USAGE_GUIDE.md、docs/GOVERNED_DEVELOPMENT_GUIDE.md、docs/design/02_REQUIREMENTS_DEFINITION.md、docs/design/06_OPERATION_AND_HANDOFF.md、docs/design/README.md、project-notes/CURRENT.md、CHANGELOG.md | Changed | 案内文書3件の文書情報表を、現在の位置のまま、初期状態で閉じた折りたたみ表示にした。表示名は「Document Info（文書情報）」である。管理用文書の文書情報表は折りたたんでいない。テンプレートの値を記入欄へ変える提案は不採用であり、この変更に含めていない。版は README 0.9、使用説明書 0.8、参考資料 0.6、02 と 06 は 0.9、管理設計 README 0.10、CURRENT 0.13、CHANGELOG 0.13、いずれも Draft。本行は commit 前の記録であり、今回の Push と Actions 成功は含まない。基点は配布先 `d36d04960e2fb3f1a2fb2747b71da3ebda550e52`。前回の説明追加のレビュー PASS は、この表示変更の PASS ではない。中央同期とテンプレート再配布は対象外である。正式承認、独立レビュー、Public化は未実施である。 | Takashi Oikawa |
| 0.12 | 2026-10-10 | README.md、docs/STUDENT_USAGE_GUIDE.md、docs/GOVERNED_DEVELOPMENT_GUIDE.md、docs/design/ の7文書、project-notes/CURRENT.md、CHANGELOG.md | Changed | 同じ管理方式を、設定がある場合とない場合でAIへ適用する方法を追加した。参考資料に共通前提、利用先の構成図、適用方法を置き、使用説明書§6の指示例全文は再掲していない。案内と管理設計は、その記載先を参照する。版は README 0.8、使用説明書 0.7、参考資料 0.5、管理設計 README 0.9、01 は 0.7、02 と 06 は 0.8、03〜05 は 0.6、CURRENT 0.12、CHANGELOG 0.12、いずれも Draft。本行は commit 前の記録であり、今回の Push と Actions 成功は含まない。基点は配布先 `5595eaa2ebf777064b370cc3043160bc3cb727d3`。前回の再配布と案内修正のレビュー PASS は、この追加変更の PASS ではない。中央同期とテンプレート再配布は対象外である。正式承認、独立レビュー、Public化は未実施である。 | Takashi Oikawa |
| 0.11 | 2026-10-10 | README.md、docs/STUDENT_USAGE_GUIDE.md、docs/GOVERNED_DEVELOPMENT_GUIDE.md、docs/design/ の01・02・06・README、project-notes/CURRENT.md、CHANGELOG.md、templates/design/ の7文書 | Changed | 中央の反映済み commit から7テンプレートを無変換で再配布した。FAQを6問の確定順序と Q/A 形式へ更新し、取得方法、承認前確認、製品表の参照先を案内へ集約した。解消済みの版数不一致を公開阻害条件から外した。版は README 0.7、使用説明書 0.6、参考資料 0.4、管理設計 README 0.8、01 は 0.6、02 と 06 は 0.7、CURRENT 0.11、CHANGELOG 0.11、いずれも Draft。本行は commit 前の記録であり、今回の Push と Actions 成功は含まない。正式承認と Public 化は未実施である。 | Takashi Oikawa |
| 0.10 | 2026-10-10 | README.md、docs/design/02_REQUIREMENTS_DEFINITION.md、docs/design/06_OPERATION_AND_HANDOFF.md、docs/design/README.md、project-notes/CURRENT.md、CHANGELOG.md | Changed | ルート README の不足を補い、使用説明書と参考資料との重複を整理した。02 に掲載内容と重複の扱いを定義し、06 に受け入れ条件を追加した。7文書の名称と役割を README に掲載し、使用説明書 §3 の文書 ID・記載例・説明全文は転載しない。版は README 0.6、02 と 06 は 0.6、管理設計 README 0.7、CURRENT 0.10、CHANGELOG 0.10、いずれも Draft。Status は Draft のままなので、使用説明書が初回承認版とする 1.0 にはしていない。本行は commit 前の記録であり、今回の Push と Actions 成功は含まない。基点 `f76360bdd91bbfca6ae53be3e666e88bab160104`。正式承認と Public 化は未実施である。 | Takashi Oikawa |
| 0.9 | 2026-10-10 | docs/STUDENT_USAGE_GUIDE.md、docs/GOVERNED_DEVELOPMENT_GUIDE.md、project-notes/CURRENT.md、CHANGELOG.md | Changed | 使用説明書のFAQを、既存設計の移行と設定なしの開始を含む6問へ更新した。参考資料へ、使用するAIごとのWeb版・Desktop版の比較と公式URLを追記した。版は使用説明書 0.5、参考資料 0.3、CURRENT 0.9、CHANGELOG 0.9、いずれも Draft。管理設計7文書の版数は変更しない。本行はcommit前の記録であり、今回のPushとActions成功は含まない。基点 `5270504a9f58470852cb476fe5fcf557e11bb3ae` の過去Pushとは区別する。独立レビュー、正式承認、Public化は未実施である。 | Takashi Oikawa |
| 0.8 | 2026-10-10 | README.md、docs/STUDENT_USAGE_GUIDE.md、docs/GOVERNED_DEVELOPMENT_GUIDE.md、docs/design/ の7文書、project-notes/CURRENT.md、CHANGELOG.md | Changed | 目的文をSDDとSSOTに合わせ、利用先の設定ファイルを任意とした。手順A・手順B・LEARNINGの利用区分は撤回済みである。正式PurposeはDISTRIBUTIONのまま。更新後の版は、root README 0.5、使用説明書 0.4、参考資料 0.2、管理設計README 0.6、01〜06 は 0.5、CURRENT 0.8、CHANGELOG 0.8、いずれも Draft である。第2版の「リンク0件」不合格とは区別する。本行はcommit前の記録であり、今回のPushとActions成功は含まない。独立レビュー、正式承認、Public化は未実施である。 | Takashi Oikawa |
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
