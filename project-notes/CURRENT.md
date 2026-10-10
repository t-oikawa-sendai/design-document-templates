<!--
Program Name: DDT CURRENT
Language: Markdown
Function: 目的、確認時点のGit反映状態、現在地点、次作業を記録する
Created: 2026-10-09
Last Updated: 2026-10-10
Author: Takashi Oikawa
AI: Cursor
Memo: Document ID DDT-CURRENT-001。Version 0.10 / Draft。正式承認ではない
-->

# CURRENT

<!-- Document Info（文書情報） -->
| Item（項目） | Value（値） |
|---|---|
| Document ID（文書ID） | DDT-CURRENT-001 |
| Version（バージョン） | 0.10 |
| Status（ステータス） | Draft |
| Created Date（作成日） | 2026-10-09 |
| Last Updated（最終更新日） | 2026-10-10 |
| Owner（管理者） | Takashi Oikawa |
| Related Documents（関連文書） | [README.md](../README.md) / [生徒向け使用説明書](../docs/STUDENT_USAGE_GUIDE.md) / [7文書管理と設定ファイルの参考資料](../docs/GOVERNED_DEVELOPMENT_GUIDE.md) / [CHANGELOG.md](../CHANGELOG.md) / [管理設計](../docs/design/README.md) |

## Purpose（目的）

DISTRIBUTION。正式 Purpose は変更しない。2026-10-10 の目的文は次のとおりである。

> SDD（仕様駆動開発）で、AIが作成する設計文書を決まった7文書・決まった節へ収め、重複と冗長化を防ぐためのテンプレートを配布する。生徒は自分のリポジトリに配置して使う。

手順Aのみを今期の提供区分とする方針は、現行の確定事項から撤回済みである。経緯は Completed に残す。

## Completed（完了）

以下の既存記録は、それぞれの実測・工程時点の状態である。現在の提出段階はCurrentを参照する。

- 初期コミットは `0aa4e9e3af77688c6485035eb23b98061cd740d0`。2026-10-09 12:04:28 +0900。親コミットなし。ローカル作業ディレクトリへクローンした。
- 正式PurposeはDISTRIBUTIONと確定した。中央管理コピーと検証資産は既存配置を維持する。
- 設計担当レビューDDT-REVIEW-20261009-004は、当時の18文書に対してPASS。対象ZIPは `design-document-templates-terminology-review-20261009-210139.zip`、SHA-256は `9de15ad919fcce478192b4eece25c08a8d8ab435d453dad607930b42f4b03c77`。今回の再構成に対するPASSではない。
- 旧commit `4dfc3a1965ee1c4258a71b837fe5be14d858cff7` のpushはGH007で拒否された。メールだけをnoreplyへ変更したamendで、新commit `c7488965f98149dc73232490e42b62f699207d93` を作成した。親は初期コミット、Tree・名前・日時・本文は維持した。退避bundleは検証済みと報告された。
- 2026-10-09に新commit `c7488965f98149dc73232490e42b62f699207d93` の通常pushが成功した。Cursorから、fetch後のlocal HEAD・origin/main・GitHub mainの一致、clean、commit前のvalidator・差分検査成功が報告された。設計担当もGitHub mainのcommitを確認した。
- 同SHAのActions「Validate Documents」はsuccessと報告された。この既存runの成功は、今回の未反映の修正案の検証結果ではない。
- 既存7テンプレートは中央コミット `16c44976638b48c53ef16399b1d51217c540be0a` の `docs/standards/templates/design/` と全件一致していた。これは修正前の配布版の照合記録である。
- 講師判断として今期は手順Aのみとする、は 2026-10-10 の指示で撤回済みである。当時の初期値（既存文書ID、自分のOwner、初期化日のCreated Date / Last Updated、Version 0.1、Status Draft）は維持する。配布テンプレートの Version とは区別する。
- 2026-10-09 に、正本文書レビューの最終修正を両リポジトリの作業ツリーへ適用した。配布先の確認時点のGit反映基準は `c7488965f98149dc73232490e42b62f699207d93`（main、Private）。local HEAD、fetch済み origin/main、GitHub main はこの SHA で一致した。この修正は未commitであり、stage は空である。この SHA を、未commitの修正を含む CURRENT 自身の commit SHA としては扱わない。
- 中央原本のローカル HEAD は `18f5ed1c06999796f165d121a513afac5d6347a3`。fetch 後の origin/main と GitHub main は確認基準 `16c44976638b48c53ef16399b1d51217c540be0a`。公開範囲は Private。ローカル HEAD はその祖先で 2 commit 遅れ、対象外の未commit差分がその 2 commit の変更ファイルと重なる。HEAD は動かしていない。中央 `CHANGELOG.md` は確認基準の本文と一致せず、`solacom_main.patch` の `git apply --check` は終了コード 1（`CHANGELOG.md`）だった。このファイルは上書きしていない。
- 中央 `docs/standards/templates/design/README.md` と `04_UI_AND_FLOW_DESIGN.md` は、適用前の SHA-256 が確認基準と一致したため本文案を適用した。他 5 テンプレートは無変更。中央の Git 反映は未実施である。配布先 `templates/design/` の 7 文書は、修正後の中央作業ツリーからバイト単位でコピーした。README と 04 だけが配布先 HEAD からの差分であり、他 5 文書は `c7488965f98149dc73232490e42b62f699207d93` と一致する。これは再配布準備であり、反映済み原本からの再配布完了ではない。
- 配布先の `python3 scripts/validate-docs.py` は終了コード 0。検査対象 21 件はすべて PASS である。対象は `CHANGELOG.md`、`README.md`、`docs/GOVERNED_DEVELOPMENT_GUIDE.md`、`docs/NEW_REPOSITORY_SETUP_GUIDE.md`、`docs/STUDENT_USAGE_GUIDE.md`、`docs/design/` の 7 文書、`docs/standards/DOCUMENT_GOVERNANCE_STANDARD.md`、`project-notes/CURRENT.md`、`templates/design/` の 7 文書である。`git diff --check` と `git diff --cached --check` は終了コード 0。`git diff --cached --name-only` は空である。`git diff --stat templates/` は README と 04 の 2 文書である。ヘッダー検査の PASS は、本文が正しいことではない。
- 生徒向け説明書では、commit 識別子、レビュー資料名、中央原本のリポジトリ名、ローカル絶対パス、講師の旧表記は 0 件である。手順BとLEARNINGは §1 の講師用資料への案内 1 行だけである。所有 12 文書に講師の旧表記とローカル絶対パスはない。中央 7 テンプレートに講師の旧表記はない。説明書は 7 章、初期値は 6 項目、文書 ID は 7 件である。
- Mermaid のローカル表示は、既存 Chrome の headless で 3 図とも `RENDER PASS` である。目視でラベルの欠け、重なり、切れはない。GitHub 上の表示は未確認である。このローカル表示は、今回の未commit修正の表示確認であり、公開後の表示確認ではない。

- 設計担当は、ZIP `design-document-templates-final-review-20261009-224229.zip` を受領し、SHA-256 `5540722ab4b197c34a557938ea99f69e58efb8b776e3075fd7e5f7a4ed3c6ed8` と本文・実差分を確認した。レビュー `DDT-REVIEW-20261009-005` は配布先19文書と中央テンプレート2文書についてPASS。CURRENT・CHANGELOGの実測追記も確認した。新規文書patchの絶対パスは、設計側で相対パスに直し、受領した19文書の復元一致を確認した。
- 設計担当は中央CHANGELOGの収録未適用案も全文確認し、既存履歴を保持した追記を承認した。中央のローカルCHANGELOGは、旧HEAD `18f5ed1c06999796f165d121a513afac5d6347a3` のGit Blobと一致し、独自の未commit編集はなかった。
- 利用者はPushまで進めることを明示指示した。正式承認・Public化の指示とは区別する。
- 中央で旧HEADから確認基準 `16c44976638b48c53ef16399b1d51217c540be0a` へ比較基準を同期し、作業ファイルの内容・削除状態と対象外の変更を保持したことを確認した。承認済み3文書だけをcommitし、通常pushした。中央のlocal HEAD・fetch後のorigin/main・GitHub mainは `93a3fce46780cf134ea0ebc4a610c96571040fd2` で一致した。
- 配布先7テンプレートは、中央の反映済みcommit `93a3fce46780cf134ea0ebc4a610c96571040fd2` の7文書と全件バイト一致し、原本からの再配布を確認した。配布先の変更対象は従来の14文書のまま。既存保護6資産は変更していない。
- 2026-10-09 の commit `7e02ccc6305c74ae08e2bf0436cb6f38604a2c75` は、通常 push 済みの過去実績である。2026-10-10 の確認で、local HEAD、fetch 後の origin/main、GitHub main はこの SHA で一致し、作業ツリーは clean、公開範囲は Private だった。同 SHA の Actions「Validate Documents」run `37941377205` は success である。https://github.com/t-oikawa-sendai/design-document-templates/actions/runs/37941377205 この成功は、今回の目的訂正の検証結果ではない。
- 第2版の「リンク0件」を不合格とした判断は、所有者の最新指示で撤回済みである。今回の目的訂正とは別である。参考資料へのリンクを root README と使用説明書に置く。
- 2026-10-10 の目的訂正について、commit 前に次を確認した。`python3 scripts/validate-docs.py` は終了コード 0、検査対象 21 件は PASS。`git diff --check` は終了コード 0。差分は指定12文書のみ。`templates/design/` の7文書、`CONSTITUTION.md`、`AGENTS.md`、`docs/standards/`、`docs/NEW_REPOSITORY_SETUP_GUIDE.md`、`scripts/validate-docs.py`、`.github/workflows/validate-docs.yml` の SHA-256 は編集前と一致した。新規 F/O/R-ID は作っていない。変更した構成図はローカルの Chrome headless で表示を確認した。この箇条書きを書いた時点では、その commit の Push と Actions は未実施である。
- 目的訂正の commit `5270504a9f58470852cb476fe5fcf557e11bb3ae`（親 `7e02ccc6305c74ae08e2bf0436cb6f38604a2c75`）は、その後の通常 push で GitHub main に到達した。2026-10-10 の再確認で、local HEAD、fetch 後の origin/main、GitHub main はこの SHA で一致し、作業ツリーは clean、公開範囲は Private だった。Actions「Validate Documents」run `37999067578` は success、head SHA は同 commit、job `validate-docs` も success である。https://github.com/t-oikawa-sendai/design-document-templates/actions/runs/37999067578 これは目的訂正の過去実績であり、今回の FAQ 更新の検証結果ではない。構成図の GitHub 表示は、未ログインの確認では Private のため開けず、未確認のままである。
- 2026-10-10 の FAQ 更新について、commit 前に次を確認した。使用説明書の §1〜6 は版数の更新以外変更がなく、FAQ は6問である。参考資料の §1〜7 は版数の更新以外変更がなく、§8 に確認日と公式URL 5件がある。5件の公式URLは指定の完全なURLのまま HTTP 200 で開けた。`python3 scripts/validate-docs.py` は終了コード 0、検査対象 21 件は PASS。`git diff --check` は終了コード 0。差分は使用説明書、参考資料、CURRENT、CHANGELOG の4文書のみ。保護資産と7テンプレートの SHA-256 は編集前と一致した。新規の仕様IDは作っていない。管理設計READMEの索引は管理設計7文書の一覧であり、この版数変更では更新していない。この箇条書きを書いた時点では、その Push と Actions は未実施である。
- FAQ 更新の commit `f76360bdd91bbfca6ae53be3e666e88bab160104`（メッセージ `docs: explain design migration and AI reading setup`）は、その後 GitHub main に到達した。2026-10-10 の README 構成見直しの開始前に、local HEAD、fetch 後の origin/main、GitHub main はこの SHA で一致し、作業ツリーは clean、公開範囲は Private だった。Actions「Validate Documents」run `38001977735` は success である。https://github.com/t-oikawa-sendai/design-document-templates/actions/runs/38001977735 これは FAQ 更新の過去実績であり、README 構成見直しの検証結果ではない。CURRENT に残っていた `5270504a9f58470852cb476fe5fcf557e11bb3ae` は目的訂正の過去 SHA であり、この HEAD ではない。

## Current（現在）

Private・Draft。正式 Purpose は DISTRIBUTION のままである。作業基点は FAQ 更新の反映済み commit `f76360bdd91bbfca6ae53be3e666e88bab160104` である。いま行っているのは、ルート README の構成見直しである。掲載内容と重複の扱いは要件定義、受け入れ条件は運用・引き継ぎに定義し、README はそれに合わせる。この CURRENT は、その commit 前の記録である。設計担当の実差分レビュー PASS の前には commit しない。PASS 後の通常 commit と通常 push は、利用者の明示許可がある。その SHA、Push 成功、Actions 成功は、この本文へ追記するための amend をしない。正式承認、独立レビュー、Public化は未実施である。

## Next（次）

1. 設計担当の実差分レビューを受ける。自己検証を PASS として扱わない。
2. PASS 後、承認対象パスだけを通常 commit し、通常 push する。拒否や競合を force push で回避しない。
3. Push 後の SHA と Actions は最終報告で確認する。この本文へ追記するための amend はしない。
4. 独立レビュー、正式承認、公開前確認、Public化は、その後の指示で進める。

## Blockers（阻害要因）

- 独立レビュー、正式承認、Public化は未完了である。今回の Push を公開承認とは扱わない。旧レビューの PASS は、今回の README 差分レビューの PASS ではない。
- 目的訂正で変更した構成図の GitHub 上の表示は未確認である。
- 旧不具合と、撤回済みの手順A・手順B・LEARNINGの提供区分は、現行の阻害要因にしない。

## Related Decisions（関連Decision）

新しいDecision番号やF/O/R仕様IDは採番しない。目的文、SSOT、設定ファイルの任意性は [要求定義](../docs/design/01_REQUEST_DEFINITION.md)、[要件定義](../docs/design/02_REQUIREMENTS_DEFINITION.md)、[使用説明書](../docs/STUDENT_USAGE_GUIDE.md)、[参考資料](../docs/GOVERNED_DEVELOPMENT_GUIDE.md) に記録する。
