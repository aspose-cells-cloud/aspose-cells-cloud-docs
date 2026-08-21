---
title: "Excelワークシートのページ数を取得する"
second_title: "Document"
linktitle: "PageCount"
type: docs
url: /worksheets/page-count/
keywords: "Aspose.Cells, Excel API, ワークシートのページ数, REST, クラウドSDK, Excelのページ分割"
description: "Aspose.Cells Cloud REST API（v3.0）を使用してExcelワークシートの印刷可能ページ数を取得します。HTTPSリクエスト形式、認証手順、cURLのサンプル、完全なJSONレスポンス、HTTPステータスコード、およびSDKコードサンプルを含みます。"
weight: 10
ArticleTitle: "Excelワークシートのページ数を取得する – Aspose.Cells Cloud API"
---

このREST APIは、ワークシートの**ページ数**を返します。

**認証:** Aspose.Cells Cloudのすべてのエンドポイントは、OAuth2フローで取得したBearerトークンを必要とします。以下のcURLの例に示すように、`Authorization`ヘッダーにトークンを含めてください。

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pagecount
```

### リクエストパラメーター

| パラメーター   | タイプ   | 位置     | 説明                             |
| ------------- | -------- | -------- | --------------------------------- |
| name          | string   | path     | ドキュメント名。                 |
| sheetName     | string   | path     | ワークシート名。                 |
| folder        | string   | query    | ドキュメントが格納されているフォルダー。 |
| storageName   | string   | query    | ストレージ名。                   |

[OpenAPI仕様](https://apireference.aspose.cloud/cells/#/Worksheets/GetPageCount)は、パブリックに利用可能なプログラミングインターフェースを定義し、ウェブブラウザーから直接RESTインタラクションを実行できるようにします。

**cURL** コマンドラインツールを使用すると、Aspose.Cellsウェブサービスに簡単にアクセスできます。以下の例では、cURLでAPIを呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/worksheets/Sheet1/pagecount" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <access_token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "PageCount": 3
}
```

{{< /tab >}}

{{< /tabs >}}

### レスポンスの詳細

| HTTPステータス | 意味                                         |
| -------------- | --------------------------------------------- |
| **200**        | 成功 – 上記のJSONペイロードが返されます。    |
| **401**        | 認証エラー – トークンが不足しているか無効です。 |
| **404**        | 見つかりません – ファイルまたはワークシートが存在しません。 |
| **500**        | サーバーエラー – 予期しないサーバー状態です。   |

### バージョン履歴

_APIバージョン **v3.0**（2025年リリース）。新しいバージョンを使用している場合は、更新されたエンドポイントのドキュメントを参照してください。_

## クラウドSDKファミリー

SDKを使用すると、開発速度が最も速くなります。SDKは低レベルの詳細を抽象化し、ビジネスロジックに集中できるようにします。Aspose.Cells Cloud SDKの完全な一覧は[GitHubリポジトリ](https://github.com/aspose-cells-cloud)をご覧ください。

以下のコード例は、さまざまなSDKを使用してAspose.Cellsウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetPageCount.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetPageCount.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetPageCount.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetPageCount.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetPageCount.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetPageCount.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetPageCount.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetPageCount.go" >}}

{{< /tab >}}

{{< /tabs >}}

### 注意事項

- ページ数は、ページ区切り、余白、スケーリングを考慮した印刷レイアウトに基づいて算出されます。非表示の行や列は結果に影響を与えることがあります。
- リクエストを実行する前に、対象のワークシートが存在し、ファイルが指定された`folder`および`storageName`に格納されていることを確認してください。