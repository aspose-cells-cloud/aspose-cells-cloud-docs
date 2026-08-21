---
title: "すべてのハイパーリンクを取得する – Aspose.Cells Cloud REST API"
type: docs
url: /hyperlinks/get-all/
aliases:
  [/get-hyperlink-from-excel-worksheet/, /get-hyperlinks-from-excel-worksheet/]
keywords: "Aspose.Cells, すべてのハイパーリンクを取得する, Excel API, REST API, クラウド SDK, cURL の例, スプレッドシートのハイパーリンク"
description: "Aspose.Cells Cloud REST API (v3.0) を使用して、Excel ファイル内のワークシートからすべてのハイパーリンクを取得します。HTTPS エンドポイント、必要なパラメータ、cURL の例、レスポンススキーマ、および SDK のコードサンプルを含みます。"
weight: 10
ArticleTitle: "すべてのハイパーリンクを取得する – Aspose.Cells Cloud REST API ドキュメント"
---

この REST API は、Excel ワークブック内の特定のワークシートから**すべてのハイパーリンク**を取得します。

## セキュリティと認証

Aspose.Cells Cloud API は安全であり、[JWT トークンによる認証](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)が必要です。

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks
```

### リクエストパラメータ

| パラメータ名   | 型     | 位置   | 必須 | デフォルト | 説明                         |
| -------------- | ------ | ------ | ---- | ---------- | ----------------------------- |
| name           | string | path   | はい | –          | Excel ドキュメントの名前です。 |
| sheetName      | string | path   | はい | –          | ワークシートの名前です。       |
| folder         | string | query  | いいえ | –        | ドキュメントが格納されているフォルダです。 |
| storageName    | string | query  | いいえ | –        | 使用するストレージサービスの名前です。 |

[OpenAPI スペック](https://apireference.aspose.cloud/cells/#/Hyperlinks/GetWorksheetHyperlinks) は、パブリックに利用可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST のやり取りを実行できるようにしています。

cURL コマンドラインツールを使用して Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例では、cURL を使って API を呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/hyperlinks" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Hyperlinks": {
    "Count": 4,
    "HyperlinkList": [
      {
        "link": {
          "Href": "/0",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "link": {
          "Href": "/1",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "link": {
          "Href": "/2",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "link": {
          "Href": "/3",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      }
    ],
    "link": null
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

JSON レスポンスには `Hyperlinks` オブジェクトが含まれます。

- **Count** – ワークシート内のハイパーリンクの総数。
- **HyperlinkList** – 各要素が `link` オブジェクトを保持する配列です。`Href` プロパティにはハイパーリンクのアドレスが格納され、`Rel`、`Title`、`Type` には追加のメタデータが含まれます（単純なリンクでは通常 `null` になります）。

### エラーレスポンス

| HTTP コード | 理由                                             | 例ボディ                                                            |
| ----------- | ------------------------------------------------ | ------------------------------------------------------------------- |
| **400**     | 不正リクエスト – パラメータが不足または無効です。 | `{ "Code":"400", "Message":"Invalid parameter value." }`            |
| **401**     | 認証エラー – JWT トークンが不足または無効です。    | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404**     | 見つかりません – ワークブックまたはワークシートが存在しません。 | `{ "Code":"404", "Message":"File not found." }`                     |
| **500**     | サーバ内部エラー – 予期しないサーバ障害が発生しました。 | `{ "Code":"500", "Message":"An unexpected error occurred." }`       |

## クラウド SDK ファミリー

SDK を使用すると、この機能を統合する最も速い方法です。SDK は低レベルの詳細を処理するため、ビジネスロジックに集中できます。Aspose.Cells Cloud SDK の完全なリストについては、[GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetHyperlinks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetHyperlinks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetHyperlinks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetHyperlinks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetHyperlinks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetHyperlinks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetHyperlinks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetHyperlinks.go" >}}

{{< /tab >}}

{{< /tabs >}}