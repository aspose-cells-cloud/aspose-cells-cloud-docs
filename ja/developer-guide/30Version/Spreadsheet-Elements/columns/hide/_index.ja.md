---
title: "Excelワークシートで列を非表示にする"
second_title: "Document"
linktitle: "Hide"
type: docs
url: /columns/hide/
aliases:
  - /hide-columns-in-excel-worksheet/
  - /hide-columns-in-an-excel-worksheet/
keywords: "Aspose.Cells Cloud, 列非表示 API, Excel 列の非表示, REST API による列非表示, Aspose.Cells SDK, スプレッドシート自動化"
description: "Aspose.Cells Cloud REST API（v3.0）を使用して、Excelワークシートの1つまたは複数の列を非表示にする方法を学びます。エンドポイント、パラメータ、cURLの例、SDKコードサンプル、エラー処理を含みます。"
weight: 40
---

この REST API はワークシート内の列を非表示にします。

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/hide
```

### リクエストパラメータ

| パラメータ名     | 型      | 位置   | 説明                                                                     |
| ---------------- | ------- | ------ | ------------------------------------------------------------------------ |
| name             | string  | path   | ワークブックファイルの名前。                                             |
| sheetName        | string  | path   | 列を非表示にするワークシートの名前。                                     |
| startColumn      | integer | query  | 非表示にする最初の列の 0 から始まるインデックス。                        |
| totalColumns     | integer | query  | **startColumn** から始まる連続して非表示にする列の数。                  |
| folder           | string  | query  | ワークブックを含むフォルダへのパス。                                     |
| storageName      | string  | query  | ファイルが配置されているストレージサービスの名前。                       |

[OpenAPI スペック](https://apireference.aspose.cloud/cells/#/Cells/PostHideWorksheetColumns) は公開可能なプログラミングインタフェースを定義し、ウェブブラウザから直接 REST でのやり取りを可能にします。

**cURL** コマンドラインツールを使用して、Aspose.Cells ウェブサービスを簡単に呼び出すことができます。以下の例は、cURL を使用して列を非表示にする方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/hide?startColumn=1&totalColumns=1" \
     -H "accept: application/json" \
     -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**考えられるレスポンスコード**

| HTTP コード | 意味                                     | 例（エラー）                                            |
| ----------- | ---------------------------------------- | ------------------------------------------------------- |
| 200         | 成功                                     | `{ "Code": 200, "Status": "OK" }`                       |
| 400         | 不正なリクエスト（例：無効なパラメータ） | `{ "Code": 400, "Message": "Invalid column range." }`   |
| 401         | 認証エラー（トークンの不足または不正）   | `{ "Code": 401, "Message": "Invalid access token." }`   |
| 404         | 見つからない（ワークブックまたはワークシート） | `{ "Code": 404, "Message": "File not found." }`        |
| 500         | サーバ内部エラー                         | `{ "Code": 500, "Message": "Unexpected error." }`       |

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK ファミリー

SDK を使用すると、開発を最も速く行えます。SDK は低レベルの詳細を抽象化し、ビジネスロジックの開発に集中できるようにします。Aspose.Cells Cloud SDK の完全なリストは [GitHub リポジトリ](https://github.com/aspose-cells-cloud) を確認してください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostHideWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostHideWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostHideWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostHideWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostHideWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostHideWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostHideWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostHideWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}