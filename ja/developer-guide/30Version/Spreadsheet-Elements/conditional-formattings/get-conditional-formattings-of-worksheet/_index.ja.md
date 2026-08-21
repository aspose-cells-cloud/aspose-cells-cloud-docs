---
title: "条件書式ルールの取得"
type: docs
url: /conditional-formattings/get-all/
aliases: [/get-conditional-formattings-of-worksheet/]
keywords: "Aspose.Cells Cloud, REST API, Excel, 条件書式, ワークシート, 条件書式 API"
description: "Aspose.Cells Cloud REST API を使用してワークシートに適用されているすべての条件書式ルールを取得します。リクエスト構文、認証手順、パラメーター、簡潔なレスポンス例、エラー処理を含みます。"
weight: 20
---

この REST API は、ワークシートに適用されている条件書式ルールを取得します。

## セキュリティと認証
Aspose.Cells Cloud API は安全であり、[JWT トークンベースの認証](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)が必要です。

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings
```

### リクエストパラメーター

| パラメーター名 | 型     | 位置   | 説明                                   |
| -------------- | ------ | ------ | ------------------------------------- |
| name           | string | path   | Excel ファイルの名前。                 |
| sheetName      | string | path   | ワークシートの名前。                   |
| folder         | string | query  | ファイルが格納されているフォルダーのパス。 |
| storageName    | string | query  | ストレージサービスの名前（オプション）。 |

### エラーレスポンス

| HTTP コード | 理由                                         | 例ボディ                                                             |
| ----------- | -------------------------------------------- | -------------------------------------------------------------------- |
| **400**     | 不正リクエスト – パラメーターが不足しているか、無効です。 | `{ "Code":"400", "Message":"Invalid parameter value." }`            |
| **401**     | 認証エラー – JWT トークンが不足しているか、無効です。     | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404**     | 見つかりません – ワークブックまたはワークシートが存在しません。 | `{ "Code":"404", "Message":"File not found." }`                     |
| **500**     | サーバーエラー – 予期しないサーバー障害が発生しました。   | `{ "Code":"500", "Message":"An unexpected error occurred." }`       |

<a href="https://apireference.aspose.cloud/cells/#/ConditionalFormattings/GetWorksheetConditionalFormattings" target="_blank">OpenAPI スペック</a> はパブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザーから直接 REST 操作を実行できるようにします。

cURL コマンドラインツールを使用して Aspose.Cells Web サービスに簡単にアクセスできます。以下の例では、cURL を使って Cloud API にリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet1/conditionalFormattings" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <access_token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Status": "OK",
  "ConditionalFormattings": {
    "Count": 1,
    "ConditionalFormattingList": [
      {
        "sqref": "A1:B10",
        "FormatConditions": [
          {
            "Priority": 1,
            "Type": "CellValue",
            "Operator": "GreaterThan",
            "Formula1": "100",
            "Style": {
              "Font": {
                "Color": { "A": 255, "R": 255, "G": 0, "B": 0 },
                "IsBold": true
              }
            }
          }
        ]
      }
    ]
  }
}
```

_上記の例は、ペイロードを簡潔に保つために最も関連性の高いフィールドのみを表示しています。_

**レスポンスパラメーター**

| パラメーター                            | 型     | 説明                                      |
|----------------------------------------|--------|-------------------------------------------|
| Status                                 | string | リクエストの結果ステータス（例: **OK**）。 |
| ConditionalFormattings                 | object | 条件書式データを格納するコンテナー。       |
| ConditionalFormattings.Count           | integer| 返された条件書式ルールの数。              |
| ConditionalFormattings.ConditionalFormattingList | array | 条件書式オブジェクトのリスト。             |
| ConditionalFormattingList[].sqref      | string | 書式が適用されるセル範囲（例: **A1:B10**）。 |
| ConditionalFormattingList[].FormatConditions | array | 範囲に対する書式条件オブジェクトのコレクション。 |
| FormatConditions[].Priority            | integer| 条件の評価優先度。                         |
| FormatConditions[].Type                | string | 条件の種類（例: **CellValue**）。         |
| FormatConditions[].Operator            | string | 条件で使用される演算子（例: **GreaterThan**）。 |
| FormatConditions[].Formula1            | string | 条件の最初の数式または値。                 |
| FormatConditions[].Style               | object | 条件が満たされた場合に適用されるスタイル。 |
| Style.Font.Color                       | object | フォント用の RGBA 色定義。                |
| Style.Font.IsBold                      | boolean| フォントが太字かどうかを示します。         |

**HTTP ステータスコード**

| コード | 意味                         | 説明                                      |
|------|-----------------------------|-------------------------------------------|
| 200  | OK                          | フィルターが正常に適用された。レスポンスには操作の詳細が含まれる。 |
| 400  | 不正リクエスト              | パラメーターが不足しているか、無効（例: 未対応のファイル形式）。 |
| 401  | 認証エラー                  | JWT トークンが無効または不足している。     |
| 413  | ペイロードが大きすぎます     | アップロードされたファイルがサイズ制限を超えています。 |
| 500  | サーバーエラー              | 予期しないサーバーエラーが発生しました。   |

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK ファミリー

SDK を使用すると、開発を最適化できます。SDK が低レベルの詳細を処理するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全なリストは <a href="https://github.com/aspose-cells-cloud" target="_blank">GitHub リポジトリー</a> をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています。

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ConditionalFormatting-GetWorksheetConditionalFormatting-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-get-conditional-formatting-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-ConditionalFormatting-get_worksheet_conditional_formattings-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-ConditionalFormatting-GetWorksheetConditionalFormatting-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-ConditionalFormatting-GetWorksheetConditionalFormatting-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "b2a10009556f14d1f939a8433925c5f6" >}}

{{< /tab >}}

{{< /tabs >}}
---