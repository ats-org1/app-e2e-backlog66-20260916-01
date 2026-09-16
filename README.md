# Power Platform 案件リポジトリ

基盤管理担当が払い出した Power Platform 案件 1 件分のリポジトリです。Solution のソースを保持し、STG 環境・PRD 環境へのリリース操作をここから行います。

---

## 使い方

リリース操作は `Actions` タブのワークフローから行います。**どのボタンをどの順で押すか、承認時に何を確認するかは、払い出し時に基盤管理担当から案内されるリリース運用ガイドを参照してください。**

不明点、実行の失敗、設定の変更は基盤管理担当へ問い合わせてください。ワークフロー定義とリポジトリ設定は基盤管理担当が管理しています。

## 構成

| パス | 内容 |
| --- | --- |
| `.github/workflows/` | リリース操作のワークフロー |
| `src/PP-Solutions/` | Power Platform Solution のソース ([配置ルール](src/PP-Solutions/README.md)) |
| `src/Fabric-Workspaces/` | Fabric item のソース ([配置ルール](src/Fabric-Workspaces/README.md)) |
| `scripts/` | ローカル検証用の補助スクリプト。ワークフローからは使いません |

