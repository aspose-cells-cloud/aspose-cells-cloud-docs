---
title: "ワークシートのハイパーリンクを取得する"
type: docs
url: /ja/hyperlinks/get/
keywords: "Aspose.Cells Cloud, ワークシートのハイパーリンクを取得する, ExcelハイパーリンクAPI, REST, JWT認証, Excelワークシート, APIエンドポイント"
description: "Aspose.Cells Cloud API (v3.0) を使用して Excel ワークシートから特定のハイパーリンクを取得します。エンドポイント、パラメータ、cURL の例、認証の詳細、エラーハンドリング、および SDK スニペットを含みます。"
weight: 10
ArticleTitle: "Aspose.Cells Cloud API – ワークシートのハイパーリンクを取得する"
---

この REST API は、**Aspose.Cells Get Hyperlink API** を使用してワークシートの**ハイパーリンク**を取得します。

## セキュリティと認証

Aspose.Cells Cloud API は安全であり、[JWT トークンベースの認証](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)が必要です。  
エンドポイントを呼び出す前に、クライアント ID とシークレットを使用して JWT アクセストークンを取得し、`Authorization: Bearer <jwt token>` ヘッダーに含めてください。

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks/{hyperlinkIndex}
```

### リクエストパラメータ

| パラメータ名     | 型     | 位置   | 説明                                    |
| -------------- | ------ | ------ | --------------------------------------- |
| name           | string | path   | Excel ファイルの名前。                  |
| sheetName      | string | path   | リンクを含むワークシートの名前。        |
| hyperlinkIndex | integer | path  | 取得するハイパーリンクの 0 から始まるインデックス。 |
| folder         | string | query  | ドキュメントが保存されているフォルダ。  |
| storageName    | string | query  | ストレージサービスの名前。              |

### エラーレスポンス

| HTTP コード | 理由                                               | 例ボディ                                                            |
| --------- | -------------------------------------------------- | ------------------------------------------------------------------- |
| **400**   | Bad Request（不正なリクエスト） – パラメータが不足または無効です。 | `{ "Code":"400", "Message":"Invalid parameter value." }`            |
| **401**   | Unauthorized（認証されていません） – JWT トークンが不足または無効です。 | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404**   | Not Found（見つかりません） – ワークブックまたはワークシートが存在しません。 | `{ "Code":"404", "Message":"File not found." }`                     |
| **500**   | Internal Server Error（内部サーバーエラー） – 予期しないサーバー障害。 | `{ "Code":"500", "Message":"An unexpected error occurred." }`       |

[OpenAPI スペック](https://apireference.aspose.cloud/cells/#/Hyperlinks/GetWorksheetHyperlink) はパブリックにアクセス可能なプログラミングインタフェースを定義し、Web ブラウザから直接 REST によるやり取りを可能にします。

cURL コマンドラインツールを使用して Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例は、cURL を使用してクラウド API を呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/hyperlinks/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Hyperlink": {
    "Address": "https://docs.aspose.cloud/display/cellscloud/Get+Hyperlink+from+Excel+Worksheet",
    "Area": {
      "EndColumn": 0,
      "EndRow": 1,
      "StartColumn": 0,
      "StartRow": 1
    },
    "ScreenTip": null,
    "TextToDisplay": "https://docs.aspose.cloud/display/cellscloud/Get+Hyperlink+from+Excel+Worksheet",
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet1/hyperlinks/1",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## クラウド SDK ファミリー

SDK を使用することが開発を高速化する最良の方法です。SDK は低レベルの詳細を処理し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全な一覧については、[GitHub リポジトリ](https://github.com/aspose-cells-cloud) を確認してください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetHyperlink.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetHyperlink.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetHyperlink.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetHyperlink.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetHyperlink.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetHyperlink.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetHyperlink.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetHyperlink.go" >}}

{{< /tab >}}

{{< /tabs >}}
---