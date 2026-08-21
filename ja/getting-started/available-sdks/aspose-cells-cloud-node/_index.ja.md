---
title: "Aspose.Cells Cloud SDK for Node.js：変換、結合、分割、保護、検索、置換など"
second_title: "ドキュメント"
ArticleTitle: "Aspose.Cells Cloud SDK for Node.js：変換、結合、分割、保護、検索、置換など"
linktitle: "Aspose.Cells Cloud SDK for Node.js"
type: docs
url: /available-sdks/aspose-cells-cloud-node/
description: "Aspose.Cells Cloud SDK for Node.js は、真のクロスプラットフォーム対応を提供します。1つのインポートで、Windows、Linux、macOS の開発者が同じ使いやすい API にアクセスでき、すべての Excel オブジェクトを作成・変換・結合・分割・保護・操作できます。Office のインストールは不要で、プラットフォーム固有の調整も不要です。"
weight: 30
kwords: Node.js, Node.js SDK, Excel SDK for Node.js, Cloud SDK for Node.js, REST, チャート, ピボットテーブル, テーブル/リスト オブジェクト, スプレッドシート変換, PDF, CSV, JSON, Markdown, 結合, 分割, 保護, 検索, 置換
---

この SDK はオープンソースであり、MIT ライセンスの下で提供されています。Aspose.Cells Cloud の Node ライブラリのソースコードは[こちら](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node)からアクセスできます。

# **Aspose.Cells Cloud の Node ライブラリの使用方法**

Aspose.Cells Cloud SDK for Node は、Node プログラミング言語を使用して Microsoft Excel ファイルを操作および処理できる強力なライブラリです。この SDK を使用すると、ローカルマシンに追加のソフトウェアや依存関係をインストールすることなく、クラウド上で Excel ドキュメントを作成・編集・変換できます。

この記事では、Aspose.Cells Cloud SDK for Node を使用して、新しい Excel ワークブックの作成、セルへのデータ挿入、変更されたワークブックをクラウドに保存するなどの一般的なタスクを実行する方法について説明します。

## はじめに

Aspose.Cells Cloud SDK for Go を使用する前に、開発環境をセットアップし、必要な依存関係をインストールする必要があります。Aspose のウェブサイトの[この記事](https://docs.aspose.cloud/cells/quickstart/)を参照して、クライアント ID とクライアント シークレットを取得してください。

## Aspose.Cells Cloud の Node パッケージのインストール方法

Aspose.Cells Cloud SDK for Node は npm を使用してインストールできます。npm の手順は以下の通りです。

```Powershell

npm install asposecellscloud

```

## Aspose.Cells Cloud の package.json への依存関係の追加方法

node 設定ファイル：package.json

```Node

{
    "requires": true,
    "lockfileVersion": 1,
    "dependencies": {
        "@types/jest": "^26.0.24",
        "@types/request": "^2.48.7",
        "asposecellscloud": "24.4",
        "axios": "^1.5.1",
        "JSON": "^1.0.0",
        "mocha": "^10.2.0",
        "request": "^2.88.2",
        "request-debug": "^0.2.0"
    }
}

```

## Node パッケージを使用して Xlsx を他の形式に変換する方法

- Aspose.Cells Cloud ライブラリのインポート  
  まず、Aspose.Cells Cloud NodeJS SDK から必要なパッケージをプロジェクトにインポートします。
- 資格情報による API クライアントの設定  
  固有のクライアント ID とクライアント シークレットを使用して、API クライアントを認証します。
- 変換パラメータの準備  
  変換タスクのパラメータを定義します。これには、ソースファイル名、希望の出力形式、ストレージフォルダのパスなどが含まれます。
- ワークブック変換の実行  
  PostConvertWorkbook メソッドを呼び出して変換処理を実行し、レスポンスを処理します。

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_AvailableSDKs.ts" >}}