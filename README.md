<!--
Program Name: DDT Root README
Language: Markdown
Function: 生徒向けの配布Repository入口。設計書テンプレートの一覧と利用方法を示す
Created: 2026-10-09
Last Updated: 2026-10-09
Author: Takashi Oikawa
AI: Cursor
Memo: Document ID DDT-README-001。Version 0.3 / Draft。正式承認ではない
-->

# design-document-templates

<!-- Document Info（文書情報） -->
| Item（項目） | Value（値） |
|---|---|
| Document ID（文書ID） | DDT-README-001 |
| Version（バージョン） | 0.3 |
| Status（ステータス） | Draft |
| Created Date（作成日） | 2026-10-09 |
| Last Updated（最終更新日） | 2026-10-09 |
| Owner（管理者） | Takashi Oikawa |
| Related Documents（関連文書） | [CHANGELOG.md](./CHANGELOG.md) / [docs/STUDENT_USAGE_GUIDE.md](./docs/STUDENT_USAGE_GUIDE.md) / [docs/design/README.md](./docs/design/README.md) / [templates/design/README.md](./templates/design/README.md) / [project-notes/CURRENT.md](./project-notes/CURRENT.md) |

現在の版は Version 0.3 / Draft である。変更履歴は [CHANGELOG.md](./CHANGELOG.md) を参照する。

---

## Purpose（目的）

このリポジトリの目的は、生徒が自身のプロジェクトの設計書を作成するためのテンプレートの配布及び使用方法のガイドラインである。文書の役割と利用手順の詳細は [Student Usage Guide（生徒向け使用説明書）](./docs/STUDENT_USAGE_GUIDE.md) に記載する。

## Distributed Templates（配布テンプレート）

配布内容は、設計テンプレート7文書と、生徒向け使用説明書1文書である。設計テンプレートが8件になったという意味ではない。

使用説明書は [Student Usage Guide（生徒向け使用説明書）](./docs/STUDENT_USAGE_GUIDE.md) である。既存7テンプレートは次のとおりである。

| File（ファイル） | Document（文書） |
|---|---|
| [templates/design/README.md](./templates/design/README.md) | Design Documents Index（設計書一覧） |
| [templates/design/01_REQUEST_DEFINITION.md](./templates/design/01_REQUEST_DEFINITION.md) | Request Definition（要求定義） |
| [templates/design/02_REQUIREMENTS_DEFINITION.md](./templates/design/02_REQUIREMENTS_DEFINITION.md) | Requirements Definition（要件定義） |
| [templates/design/03_DATA_AND_SECURITY_DESIGN.md](./templates/design/03_DATA_AND_SECURITY_DESIGN.md) | Data and Security Design（データ・セキュリティ設計） |
| [templates/design/04_UI_AND_FLOW_DESIGN.md](./templates/design/04_UI_AND_FLOW_DESIGN.md) | UI and Flow Design（UI・フロー設計） |
| [templates/design/05_ARCHITECTURE_DESIGN.md](./templates/design/05_ARCHITECTURE_DESIGN.md) | Architecture Design（アーキテクチャ設計） |
| [templates/design/06_OPERATION_AND_HANDOFF.md](./templates/design/06_OPERATION_AND_HANDOFF.md) | Operation and Handoff Design（運用・詳細設計引き継ぎ） |

## How to Use（利用方法）

1. [Student Usage Guide（生徒向け使用説明書）](./docs/STUDENT_USAGE_GUIDE.md) で、文書の役割と利用手順を確認する。
2. `templates/design/` のREADMEと01〜06、計7文書を取得する。
3. 自分のプロジェクトの `docs/design/` へ同じ階層で配置する。記入済み文書は上書きしない。
4. 説明書の読み込み一覧・初回指示文を使い、自分の最新文書と課題文をAIへ渡す。
5. 文書情報・記入欄を自分の内容へ更新し、一覧、参照先、図・画像を確認する。

詳細は使用説明書に記載する。この README に説明書の全文は重複掲載しない。

## Notes（注意）

- 現在は Private の準備中である。生徒が取得できる公開状態ではない。
- 管理ファイル一式のコピーは、7テンプレートを利用する条件ではない。B（管理ルールを導入した開発）は、先生が導入を確認した場合の手順である。
- root の README を、自分のプロジェクトの README へ上書きしない。
- テンプレート内の `../../CHANGELOG.md` は、利用先プロジェクトの root CHANGELOG への参照である。7文書だけの取得に CHANGELOG 本体は含まれない。
- 画像パスは記入例である。画像を準備してから、自分の設計書で参照する。
- 管理側の設計方針への入口は [docs/design/README.md](./docs/design/README.md) である。配布テンプレートの一覧とは別である。
