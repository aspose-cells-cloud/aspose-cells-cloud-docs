---
title: "すべてのワークシートを取得する"
second_title: "Document"
linktitle: "すべて"
type: docs
url: /worksheets/get-all/
aliases: [/get-worksheet-count/]
keywords: "Aspose.Cells, Cloud API, Get Worksheets, Excel, REST, SDK"
description: "Aspose.Cells Cloud REST API（v3.0）を使用して、Excelワークブック内のワークシートのリストを取得します。cURLの例、SDKスニペット、およびレスポンス形式を含みます。"
weight: 10
---

この REST API は、ワークブックに含まれるワークシートに関する情報を返します。

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets
```

### **リクエストパラメータ**

| パラメータ名     | タイプ   | 位置   | 説明                                |
| ---------------- | -------- | ------ | ----------------------------------- |
| name             | string   | path   | Excelドキュメントの名前です。       |
| folder           | string   | query  | ドキュメントを含むフォルダーです。  |
| storageName      | string   | query  | 使用するストレージの名前です。      |

[OpenAPI仕様](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheets)は、パブリックにアクセス可能なプログラミングインターフェースを定義し、Webブラウザから直接RESTインタラクションを実行できるようにします。

cURLコマンドラインツールを使用してAspose.Cells Cloudサービスにアクセスできます。以下の例では、ワークシートを取得するためのGETリクエストを示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Worksheets": {
    "WorksheetList": [
      {
        "link": {
          "Href": "/Sheet1",
          "Rel": "self"
        }
      },
      {
        "link": {
          "Href": "/Sheet2",
          "Rel": "self"
        }
      }
    ],
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets",
      "Rel": "self"
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## エラーハンドリング

このエンドポイントから返される典型的なHTTPステータスコード：

| コード | 意味                   | 説明                               |
| ------ | ---------------------- | ---------------------------------- |
| 400    | Bad Request            | 必須パラメータ（例：`name`）が不足しています。 |
| 401    | Unauthorized           | 無効または不足しているJWTトークンです。     |
| 404    | Not Found              | 指定されたワークブックが存在しません。      |
| 500    | Internal Server Error  | 予期しないサーバーの状態です。              |

エラーレスポンスはJSON形式で返されます。例：

```json
{
  "Code": "401",
  "Message": "Invalid access token."
}
```

## Cloud SDKファミリー

SDKを使用することは、開発を迅速化する最良の方法です。SDKが低レベルの詳細を処理するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDKの完全な一覧については、[GitHubリポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例は、さまざまなSDKを使用してAspose.Cellsウェブサービスを呼び出す方法を示しています：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheets.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheets.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheets.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheets.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheets.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheets.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheets.go" >}}

{{< /tab >}}

{{< /tabs >}}