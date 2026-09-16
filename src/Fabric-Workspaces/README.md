# src/Fabric-Workspaces/

案件に Fabric item (Power BI コンポーネント等) が含まれる場合、このディレクトリ配下で管理します。Power Platform 側は [../PP-Solutions/](../PP-Solutions/) を参照してください。

## 配置ルール (暫定)

- Fabric Workspace の Git 連携出力形式に準拠 (Workspace 直下に item ごとフォルダ)。
- 環境ごとに `Dev/` `Stg/` `Prd/` の 3 フォルダを配置し、各フォルダを 1 つの Fabric Workspace として扱います。
- 各 Workspace 配下は Fabric 側の [Source code format](https://learn.microsoft.com/fabric/cicd/git-integration/source-code-format) に従い、item 種別ごとにフォルダが自動生成されます (Report / Semantic model / Notebook / Lakehouse 等)。

```
src/Fabric-Workspaces/
├── Dev/    (Fabric Dev Workspace の Git 連携先)
├── Stg/    (Fabric Stg Workspace の Git 連携先)
└── Prd/    (Fabric Prd Workspace の Git 連携先)
```

この構成は 1 案件で 1 系統の Workspace を使う前提です。**複数の Workspace を使い分ける場合はフォルダ構成を変更できます**。変更後の構成と切り替え手順は、基盤管理担当から配布されるリリース運用ガイドに記載されています。

## CI/CD

Fabric item の CI/CD (Git integration 方式・認証 SPN・環境昇格フロー等) は別バックログで設計予定。現時点ではフォルダ枠のみ用意した状態です。
