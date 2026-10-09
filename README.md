<!--
Program Name: DDT Root README
Language: Markdown
Function: 配布入口、利用早見、7文書管理の概要を示す
Created: 2026-10-09
Last Updated: 2026-10-10
Author: Takashi Oikawa
AI: Cursor
Memo: Document ID DDT-README-001。Version 0.5 / Draft。正式承認ではない
-->

# design-document-templates

<!-- Document Info（文書情報） -->
| Item（項目） | Value（値） |
|---|---|
| Document ID（文書ID） | DDT-README-001 |
| Version（バージョン） | 0.5 |
| Status（ステータス） | Draft |
| Created Date（作成日） | 2026-10-09 |
| Last Updated（最終更新日） | 2026-10-10 |
| Owner（管理者） | Takashi Oikawa |
| Related Documents（関連文書） | [CHANGELOG.md](./CHANGELOG.md) / [使用説明書](./docs/STUDENT_USAGE_GUIDE.md) / [設計テンプレート](./templates/design/README.md) / [7文書管理と設定ファイルの参考資料](./docs/GOVERNED_DEVELOPMENT_GUIDE.md) |

## Purpose（目的）

> SDD（仕様駆動開発）で、AIが作成する設計文書を決まった7文書・決まった節へ収め、重複と冗長化を防ぐためのテンプレートを配布する。生徒は自分のリポジトリに配置して使う。

SDDは、仕様書を先に書き、AIはその仕様に従って実装する進め方です。設計内容と承認は、利用先リポジトリの持ち主が判断します。

詳しい使い方は [使用説明書](./docs/STUDENT_USAGE_GUIDE.md) を参照してください。テンプレートは [設計テンプレート](./templates/design/README.md) にあります。

| 手順 | 行うこと | 参照先 |
|---|---|---|
| 1. 取得・初期化 | 設計書READMEと01〜06の7文書を取得し、自分の `docs/design/` へ置いて初期値にする。 | [設計テンプレート](./templates/design/README.md)、[説明書§4](./docs/STUDENT_USAGE_GUIDE.md#4-取得と配置)、[説明書§5](./docs/STUDENT_USAGE_GUIDE.md#5-自分の文書にする) |
| 2. 設計記入・確認 | 最新の7文書を渡し、指定した節を記入して、持ち主が内容を確認する。 | [説明書§6](./docs/STUDENT_USAGE_GUIDE.md#6-aiへの指示) |
| 3. 仕様変更・実装 | 先に該当設計書を更新して承認し、その仕様に従って実装と確認を行う。 | [説明書§6](./docs/STUDENT_USAGE_GUIDE.md#6-aiへの指示) |

## 7文書で管理するメリット

> AI任せにすると、似た内容の「設計文書もどき」が大量に生成され、どれが正しい仕様か分からなくなることがあります。記載先を決まった7文書・節に限定し、同じ内容は再掲せず参照することで、SSOT（正しい情報の管理元を一つに定める原則）を守り、文書の乱立・重複・矛盾を防ぎます。

| 構成 | メリット | デメリット・注意点 |
|---|---|---|
| 7文書による管理 | 仕様の記載先が決まり、情報を探しやすい。AIによる重複・冗長化を抑え、仕様変更と実装の対応を確認しやすい。 | AIに対象文書・節と管理方法を伝える必要がある。7文書間の整合確認が必要。 |
| 7文書＋設定ファイル | 管理ルールを共通化でき、毎回の指示を短くできる。複数AIでの作業や引き継ぎがしやすい。 | 設定ファイルの理解・更新と、設計書との整合確認が必要。AIが読み、従っているかの確認も必要。 |

> 設定ファイルの導入は任意です。AGENTS.md・CONSTITUTION.mdがなくても7文書で管理できます。詳しい使い方は、[7文書管理と設定ファイルの参考資料](./docs/GOVERNED_DEVELOPMENT_GUIDE.md)を参照してください。
