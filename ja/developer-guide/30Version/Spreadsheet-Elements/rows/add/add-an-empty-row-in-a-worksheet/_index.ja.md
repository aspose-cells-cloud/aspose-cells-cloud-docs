---
title: "Excelワークシートに空の行を追加する"
ArticleTitle: "Aspose.Cells Cloud API を使用して Excel ワークシートに空の行を追加する"
second_title: "ドキュメント"
linktitle: "行"
type: docs
url: /rows/add/row/
aliases: [/add-an-empty-row-in-a-worksheet/]
keywords: "Aspose.Cells Cloud, Excel, 空の行を追加, ワークシート, REST API, 行の挿入, クラウドスプレッドシート"
description: "Aspose.Cells Cloud REST API を使用して Excel ワークシートに空の行を挿入します。複数の SDK（C#、Java、Python、Go、PHP、Ruby、Node.js、Perl、Android、Swift）をサポートし、迅速な開発を実現します。"
weight: 20
---

この REST API は、Excel ワークシートに新しい行を追加します。指定された 0 から始まるインデックス位置に空の行を挿入します。

**前提条件：**  
- 有効な Aspose Cloud アクセストークン（Bearer JWT）を `Authorization` ヘッダーに含める必要があります。  
- 対象のワークブックは Aspose Cloud ストレージにアップロード済みであり、`folder` および `storageName` パラメータがその場所を指している必要があります。

**注意事項：**  
- `rowIndex` は 0 から始まるインデックスです。インデックス 0 に挿入すると、ワークシートの最上部に行が追加されます。  
- Excel ワークシートの最大行数は 1,048,576 行です。この上限を超えて挿入を試みるとエラーが発生します。

## PutInsertWorksheetRow API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/{rowIndex}
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### **リクエストパラメータ**

| パラメータ名 | 型      | 位置   | 説明                                        |
|------------|---------|--------|---------------------------------------------|
| name       | 文字列   | path   | ワークブックのファイル名。                  |
| sheetName  | 文字列   | path   | ワークシートの名前。                        |
| rowIndex   | 整数    | path   | 新しい行を挿入する 0 から始まるインデックス。 |
| folder     | 文字列   | query  | ストレージ内のワークブックが存在するフォルダのパス。 |
| storageName| 文字列   | query  | 使用する Aspose Cloud ストレージの名前。     |

[OpenAPI スペック](https://apireference.aspose.cloud/cells/#/Cells/PutInsertWorksheetRow) はパブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST アクセスを可能にします。

cURL コマンドラインツールを使用すると、Aspose.Cells Web サービスに簡単にアクセスできます。以下の例は、cURL を使用してクラウド API にリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/10" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

> **注意:** すべての Aspose.Cells Cloud エンドポイントは HTTPS を使用する必要があります。本番環境での呼び出しには、安全な `https://` スキームを使用してください。

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**HTTP ステータスコード**

| コード | 意味                         | 説明                                         |
|-------|-----------------------------|----------------------------------------------|
| 200   | OK                          | フィルターの適用に成功。レスポンスには操作の詳細が含まれます。 |
| 400   | Bad Request                 | パラメータが不足または無効（例：サポートされていないファイル形式）。 |
| 401   | Unauthorized                | JWT トークンが無効または不足しています。        |
| 413   | Payload Too Large           | アップロードされたファイルがサイズ制限を超えています。 |
| 500   | Internal Server Error       | 予期しないサーバーエラーが発生しました。         |

*エラーレスポンスの例（例：行インデックスがワークシートの上限を超えた場合）：*

```json
{
  "Code": 400,
  "Status": "Bad Request",
  "Message": "Row index out of range. Maximum rows allowed: 1048576."
}
```

## Cloud SDK Family

SDK を使用すると、開発を迅速に進めることができます。SDK は低レベルの詳細を抽象化し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全なリストについては、<a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub リポジトリ</a> をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutInsertWorksheetRow.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutInsertWorksheetRow.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutInsertWorksheetRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutInsertWorksheetRow.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutInsertWorksheetRow.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutInsertWorksheetRow.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutInsertWorksheetRow.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutInsertWorksheetRow.go" >}}

{{< /tab >}}

{{< /tabs >}}