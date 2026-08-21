---
title: "Aspose.Cells Cloud Docker イメージタグ"
second_title: "ドキュメント"
ArticleTitle: "Aspose.Cells Cloud Docker イメージタグ"
linktype: "画像タグ"
type: docs
url: /ja/docker/tag-list/
description: "Windows Server（2016～2022）および Linux 向けの最新の Aspose.Cells Cloud Docker イメージタグを検索します。プルコマンド、アーキテクチャの詳細、アップグレードに関する注意事項を一箇所で確認できます。"
weight: 30
keywords:
  - "Aspose.Cells Cloud Docker イメージタグ"
  - "Docker プルコマンド"
  - "Windows Server Docker タグ"
  - "Linux Docker タグ"
  - "Aspose.Cells Cloud"
---

Aspose.Cells Cloud では、Windows Server（2016、2019、2022）および Linux 向けの実行可能な Docker イメージを提供しています。  
各イメージは、製品リリースとターゲットオペレーティングシステムを識別する **タグ** でバージョン管理されています。  
以下のタグを使用して、必要な正確なイメージをプルし、付随するプルおよび実行の例を参照してすぐに立ち上げてください。

*最終更新日: 2026-07-01*

**前提条件:** Docker Engine 20.10 以降がインストールされており、有効な Aspose.Cells Cloud ライセンスキーを保有していることを確認してください。これらのイメージは、指定された Windows Server バージョンまたは Linux x64 向けにビルドされています。

## Windows Server 2016 向けイメージ ##

タグ | アーキテクチャ | Dockerfile | 備考
---|---|---|---
✅ `ltsc2016.23.5.0` | x64 | Dockerfile は公開されていません。ビルドの詳細については [リリースノート](https://github.com/aspose-cells/dockerfiles/tree/main/ltsc2016) を参照してください。 | Windows Server 2016 向けの新しいタグは今後提供されません。これが最終リリースバージョンです。

```bash
docker pull aspose/cells:ltsc2016.23.5.0
docker run -d --name cells-ws2016 -p 8080:80 aspose/cells:ltsc2016.23.5.0
```

追加リソース: [Docker ダウンロード](/cells/docker/downloads/)、[リリースノート](/cells/release-notes/)、[前提条件](/cells/docker/prerequisites/)。  
詳細は [Docker 概要](/cells/docker/) を参照してください。

## Windows Server 2019 向けイメージ ##

タグ | アーキテクチャ | Dockerfile | 備考
---|---|---|---
✅ `ltsc2019.25.10.0` | x64 | Dockerfile は公開されていません。ビルドの詳細については [リリースノート](https://github.com/aspose-cells/dockerfiles/tree/main/ltsc2019) を参照してください。 | —
```bash
docker pull aspose/cells:ltsc2019.25.10.0
docker run -d --name cells-ws2019 -p 8080:80 aspose/cells:ltsc2019.25.10.0
```

追加リソース: [Docker ダウンロード](/cells/docker/downloads/)、[リリースノート](/cells/release-notes/)、[前提条件](/cells/docker/prerequisites/)。  
詳細は [Docker 概要](/cells/docker/) を参照してください。

## Windows Server 2022 向けイメージ ##

タグ | アーキテクチャ | Dockerfile | 備考
---|---|---|---
✅ `ltsc2022.25.10.0` | x64 | Dockerfile は公開されていません。ビルドの詳細については [リリースノート](https://github.com/aspose-cells/dockerfiles/tree/main/ltsc2022) を参照してください。 | —
```bash
docker pull aspose/cells:ltsc2022.25.10.0
docker run -d --name cells-ws2022 -p 8080:80 aspose/cells:ltsc2022.25.10.0
```

追加リソース: [Docker ダウンロード](/cells/docker/downloads/)、[リリースノート](/cells/release-notes/)、[前提条件](/cells/docker/prerequisites/)。  
詳細は [Docker 概要](/cells/docker/) を参照してください。

## Linux 向けイメージ ##

タグ | アーキテクチャ | Dockerfile | 備考
---|---|---|---
✅ `linux.25.10.0` | x64 | Dockerfile は公開されていません。ビルドの詳細については [リリースノート](https://github.com/aspose-cells/dockerfiles/tree/main/linux) を参照してください。 | —
```bash
docker pull aspose/cells:linux.25.10.0
docker run -d --name cells-linux -p 8080:80 aspose/cells:linux.25.10.0
```

追加リソース: [Docker ダウンロード](/cells/docker/downloads/)、[リリースノート](/cells/release-notes/)、[前提条件](/cells/docker/prerequisites/)。  
詳細は [Docker 概要](/cells/docker/) を参照してください。

**バージョン変更ログ**

タグ | 変更内容
---|---
`ltsc2016.23.5.0` | Windows Server 2016 向けの最終リリース。セキュリティパッチおよびパフォーマンス改善を含みます。
`ltsc2019.25.10.0` | Aspose.Cells 25.10.0 に更新。新しい数式サポートおよびバグ修正を追加。
`ltsc2022.25.10.0` | 2019 タグと同様ですが、Windows Server 2022 ランタイム向けに最適化されています。
`linux.25.10.0` | Aspose.Cells 25.10.0 を含む Linux ベースイメージ。更新された依存関係および Linux 固有の最適化を含みます。
---