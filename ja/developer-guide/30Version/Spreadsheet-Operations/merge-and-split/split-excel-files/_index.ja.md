---
title: "Excelワークブックを複数のファイルに分割する"
ArticleTitle: "Aspose.Cells Cloud API を使用して Excel ワークブックを複数のファイルに分割する方法"
second_title: "ドキュメント"
linktitle: "Excelファイルを分割する"
type: docs
url: /ja/split-multi-excel-files/
aliases: [  /ja/split/multi-files/ ]
keywords: "Excel, Aspose.Cells Cloud, REST API, ワークブックの分割, 複数ファイル, JPEG, PNG, PDF, CSV, JSON"
description: "Aspose.Cells Cloud REST API を使用すると、Excelワークブックを複数のファイルにさまざまな形式で分割できます。このドキュメントでは、リクエストパラメーター、cURL の使用例、および C#、Java、PHP、Ruby、Node.js、Python、Perl、Go などの言語向けの SDK コードサンプルを提供しています。"
weight: 130
---

この REST API は、Excel **ワークブック**を複数のファイルにさまざまな形式で分割します。

> **前提条件** – この API を使用するには、有効な JWT トークンを取得し、サポートされている SDK のバージョンを使用していること、およびワークブックがサポートされているストレージの場所に格納されていることを確認してください。また、API はプラットフォームのガイドラインに記載されているファイルサイズ制限を適用します。

## PostWorkbookSplit API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/split
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメーター

| パラメーター名     | 型     | 位置       | 説明                                                                                         | 必須   |
| ------------------ | ------ | ---------- | -------------------------------------------------------------------------------------------- | ------ |
| files[]            | file   | formData   | **分割**する1つまたは複数の Excel ワークブック。リクエストでは `file1`、`file2` などを使用します。 | はい     |
| format             | string | クエリ     | 分割されたファイルの出力形式。                                                               | いいえ   |
| from               | integer | クエリ     | 開始ワークシートのインデックス。                                                             | いいえ   |
| to                 | integer | クエリ     | 終了ワークシートのインデックス。                                                             | いいえ   |
| horizontalResolution | integer | クエリ     | 画像の水平解像度。                                                                           | いいえ   |
| verticalResolution | integer | クエリ     | 画像の垂直解像度。                                                                           | いいえ   |
| outFolder          | string | クエリ     | 分割されたファイルの出力フォルダー。                                                         | いいえ   |
| splitNameRule      | string | クエリ     | 分割されたファイルに適用する命名ルール。                                                     | いいえ   |
| folder             | string | クエリ     | 元のワークブックを含むフォルダー。                                                           | いいえ   |
| storageName        | string | クエリ     | 使用するストレージの名前。                                                                   | いいえ   |

### **レスポンス**

```json
{
    "Status":"OK",
    "Code":200,
    "Files": [
      {
        "Filename" : "[file1 name]",
        "Filesize" : [file size],
        "FileContent" : "[Base64String]"
      },
      {
        "Filename" : "[file2 name]",
        "Filesize" : [file size],
        "FileContent" : "[Base64String]"
      },
      {
        "Filename" : "[file3 name]",
        "Filesize" : [file size],
        "FileContent" : "[Base64String]"
      }
    ]
}
```

**HTTP ステータスコード**

| コード | 意味                     | 説明                                               |
|------|--------------------------|----------------------------------------------------|
| 200  | OK                       | フィルターが正常に適用された。レスポンスには操作の詳細が含まれます。 |
| 400  | Bad Request              | パラメーターが不足しているか無効である（例：サポートされていないファイル形式）。 |
| 401  | Unauthorized             | JWT トークンが無効または不足している。               |
| 413  | Payload Too Large        | アップロードされたファイルがサイズ制限を超過している。 |
| 500  | Internal Server Error    | サーバー内で予期しないエラーが発生した。             |

## SDK を使用した PostWorkbookSplit API の利用方法

### PostWorkbookSplit API の仕様

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbookSplit) はパブリックにアクセス可能なプログラミングインターフェースを定義し、ウェブブラウザから直接 REST のやり取りを実行できるようにします。

**cURL** コマンドラインツールを使用すると、Aspose.Cells Web サービスに簡単にアクセスできます。以下の例は、cURL を使用して Cloud API にリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/test.xlsx/split?format=jpeg&from=1&to=1&horizontalResolution=0&verticalResolution=0" -H "accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Result": {
    "Documents": [
      {
        "Id": 1,
        "link": {
          "Href": "413e3375-c163-4d5c-8b84-8f95f63902f6.png",
          "Rel": null,
          "Title": null,
          "Type": null
        }
      }
    ]
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、開発を最も効率的に進めることができます。SDK が低レベルの詳細を処理するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全なリストについては、[GitHub リポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスにリクエストを送信する方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorkbookSplit.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorkbookSplit.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorkbookSplit.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorkbookSplit.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorkbookSplit.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorkbookSplit.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorkbookSplit.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorkbookSplit.go" >}}

{{< /tab >}}

{{< /tabs >}}
---