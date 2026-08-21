---
title: "セル範囲の削除 – Aspose.Cells Cloud API ドキュメント"
type: docs
url: /ja/conditional-formattings/delete-cell-area/
aliases: [  /ja/remove-cell-area-from-conditional-formatting/ ]
keywords: "Aspose.Cells Cloud, セル範囲の削除, 条件付き書式 API, Excel REST API"
description: "Aspose.Cells Cloud REST API を使用して、Excelワークシート内の条件付き書式から特定のセル範囲を削除します。ASP.NET、Java、Pythonの例を含みます。"
ArticleTitle: "セル範囲の削除 – Aspose.Cells Cloud API ドキュメント"
weight: 70
---

この REST API は、条件付き書式ルールからセル範囲を削除します。

## セキュリティと認証
Aspose.Cells Cloud API は安全であり、[JWT トークンベースの認証](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)が必要です。

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/area
```

### リクエストパラメータ

| パラメータ名     | 型      | 位置   | 説明                                         |
|------------------|---------|--------|----------------------------------------------|
| `name`           | 文字列  | パス   | Excelファイルの名前                          |
| `sheetName`      | 文字列  | パス   | 条件付き書式を含むワークシートの名前         |
| `startRow`       | 整数    | クエリ | 削除する範囲の最初の行の 0 から始まるインデックス |
| `startColumn`    | 整数    | クエリ | 削除する範囲の最初の列の 0 から始まるインデックス |
| `totalRows`      | 整数    | クエリ | 削除する範囲の行数                           |
| `totalColumns`   | 整数    | クエリ | 削除する範囲の列数                           |
| `folder`         | 文字列  | クエリ | ファイルが存在するクラウドストレージ内のフォルダ（オプション） |
| `storageName`    | 文字列  | クエリ | ストレージサービスの名前（オプション）       |

### エラーレスポンス

| HTTPステータス | コード            | 説明                                           | サンプル JSON                                                   |
|----------------|-------------------|------------------------------------------------|-----------------------------------------------------------------|
| 400            | `BadRequest`      | パラメータが不足または無効です。               | `{ "Code": "400", "Message": "Invalid request parameters." }` |
| 401            | `Unauthorized`    | JWT トークンが不足または無効です。              | `{ "Code": "401", "Message": "Authentication failed." }`      |
| 404            | `NotFound`        | ファイル、ワークシート、または条件付き書式が見つかりません。 | `{ "Code": "404", "Message": "Resource not found." }`         |
| 500            | `InternalError`   | 意図しないサーバーエラーです。                 | `{ "Code": "500", "Message": "Internal server error." }`      |

[OpenAPI仕様](https://apireference.aspose.cloud/cells/#/ConditionalFormattings/DeleteWorksheetConditionalFormattingArea)は、パブリックにアクセス可能なプログラミングインターフェースを定義し、ウェブブラウザから直接REST通信を実行できるようにします。

cURLコマンドラインツールを使用して、Aspose.Cells Cloudサービスに簡単にアクセスできます。以下の例は、cURLで**セル範囲の削除**エンドポイントを呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet1/conditionalFormattings/area?startRow=3&startColumn=3&totalRows=1&totalColumns=1" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## クラウドSDKファミリー
SDKを使用するのは、開発を高速化する最良の方法です。SDKが低レベルの詳細を処理するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDKの完全なリストについては、[GitHubリポジトリ](https://github.com/aspose-cells-cloud){:target="_blank" rel="noopener noreferrer"}をご確認ください。

以下のコード例は、さまざまなSDKを使用してAspose.Cellsウェブサービスを呼び出す方法を示しています：

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ConditionalFormatting-RemoveCellAreaFromConditionalFormatting-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-remove-cell-area-from-conditional-formatting.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-ConditionalFormatting-delete_worksheet_conditional_formatting_area-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-ConditionalFormatting-RemoveCellAreaFromConditionalFormatting-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-ConditionalFormatting-RemoveCellAreaFromConditionalFormatting-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "2bc4a93409f78b40b6bcf681c6a14bda" >}}

{{< /tab >}}

{{< /tabs >}}