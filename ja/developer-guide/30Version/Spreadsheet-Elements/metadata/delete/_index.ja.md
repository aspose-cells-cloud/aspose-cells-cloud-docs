---
title: "Excel ファイルからメタデータを削除する"
second_title: "ドキュメント"
linktitle: "ストレージを使用せずに削除"
type: docs
url: /ja/metadata/delete/
keywords: "Aspose.Cells, メタデータ削除, Excel API, ワークブックプロパティ"
description: "Aspose.Cells Cloud API を使用してワークブックのメタデータ（著者、タイトル、カスタムデータ）を削除します。エンドポイント、認証、パラメータ、cURL および SDK のサンプルを含みます。"
weight: 55
ArticleTitle: "Excel ファイルからメタデータを削除する – Aspose.Cells Cloud ドキュメント"
---

**概要**  
「メタデータ削除」操作は、アップロードされた Excel ファイルからすべてのワークブックプロパティ（標準およびカスタム）を恒久的に削除し、処理済みファイルをレスポンスとして返します。

**前提条件**  
- 有効な Aspose.Cells Cloud JWT トークン（OAuth 2.0 認証フローで取得可能）。  
- API バージョン **v3.0**（この例で使用されるエンドポイント）。  
- SDK を使用する場合、使用言語に対応した Aspose.Cells Cloud SDK をインストールしてください（例：NuGet、Maven、npm、pip、CPAN、Go モジュール経由）。

この REST API は、1 つまたは複数の Excel ファイルから**メタデータ**を削除します。著者、タイトル、カスタムデータなどのワークブックプロパティを削除し、クリーニング済みのファイルを返します。

## API

```http
POST https://api.aspose.cloud/v3.0/cells/metadata/delete
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### **リクエストパラメータ**

| パラメータ名 | 型     | 位置       | 説明                                       |
| ------------ | ------ | ---------- | ------------------------------------------- |
| file         | file   | formData   | **メタデータ**削除のためにアップロードする Excel ファイル |
| type         | string | query      | 操作タイプ；**メタデータ**をすべて削除する場合は **all** を設定 |

<a href="https://apireference.aspose.cloud/cells/#/DeleteMetadata" target="_blank" rel="noopener noreferrer">OpenAPI 仕様</a> はパブリックにアクセス可能なプログラミングインタフェースを定義し、Web ブラウザから直接 REST 通信を実行できるようにします。

cURL コマンドラインツールを使用して、Aspose.Cells Web サービスを簡単にアクセスできます。以下の例は、cURL を使用して Cloud API にアクセスする方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/metadata/delete?type=all" \
  -X POST \
  -H "Authorization: Bearer <jwt token>" \
  -F "file=@file1.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Files": [
    {
      "Filename": "file1.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

**エラーレスポンス**には以下が含まれる可能性があります：

- **400 Bad Request** – ファイルが欠落している、または無効な `type` 値。
- **401 Unauthorized** – 無効または欠落している JWT トークン。
- **500 Internal Server Error** – サーバー側での処理エラー。

API は、各ケースに対して詳細情報を含む `Error` フィールドを持つ JSON オブジェクトを返します。

| コード | 意味 | 説明 |
|------|---------|-------------|
| 200 | OK | メタデータ削除完了、ファイル返却 |
| 400 | Bad Request | ファイルが欠落している、または無効な `type` |
| 401 | Unauthorized | 無効または欠落している JWT |
| 500 | Internal Server Error | サーバー処理失敗 |

## Cloud SDK ファミリー

SDK を使用することは、開発を高速化する最良の方法です。SDK は低レベルの詳細を処理するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全な一覧については、<a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub リポジトリ</a> をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteMetadata.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteMetadata.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteMetadata.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteMetadata.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteMetadata.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteMetadata.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteMetadata.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteMetadata.go" >}}

{{< /tab >}}

{{< /tabs >}}