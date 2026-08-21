---
title: "Excelワークシート内の列をコピーする"
second_title: "Document"
linktitle: "コピー"
type: docs
url: /ja/columns/copy/
aliases:
  [/copy-columns-in-excel-worksheet/, /copy-columns-in-an-excel-worksheet/]
keywords: "Aspose.Cells, 列のコピー, Excel API, REST, クラウドSDK, cURL, C#, Java, Python, Ruby, Node.js, Go, Perl"
description: "Aspose.Cells Cloud REST API（v3.0）を使用してExcelワークシート内の1つまたは複数の列をコピーする方法を学びます。リクエスト構文、必要なパラメータ、認証詳細、エラー処理、およびC#、Java、Python、Ruby、Node.js、Go、PerlなどのSDKの使用例を含みます。"
articleTitle: "Aspose.Cells Cloud APIを使用してExcelワークシート内で列をコピーする"
weight: 30
---

このREST APIは、Excelワークシート内の**列**をコピーします。**列のコピー**操作により、単一の列または列の範囲を複製し、同じワークシート内の指定された位置にコピーを挿入できます。このエンドポイントを使用すると、大規模なスプレッドシートを操作する際に効率的に列をコピーでき、追加の列管理タスクのために[列の追加](/columns/add/)や[列の非表示](/columns/hide/)などの関連操作を参照してください。

## セキュリティと認証
Aspose.Cells Cloud APIは安全であり、[JWTトークンベースの認証](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)が必要です。

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/copy
```

### リクエストパラメータ

| パラメータ名               | 型      | 位置   | 説明                                                                                     |
| -------------------------- | ------- | ------ | --------------------------------------------------------------------------------------- |
| **name**                   | 文字列  | パス   | ワークブック名。                                                                        |
| **sheetName**              | 文字列  | パス   | ワークシート名。                                                                        |
| **sourceColumnIndex**      | 整数    | クエリ | コピー元の列の0始まりのインデックス。                                                   |
| **destinationColumnIndex** | 整数    | クエリ | コピーされた列を挿入する0始まりのインデックス。                                         |
| **columnNumber**           | 整数    | クエリ | コピーする連続する列の数。                                                              |
| **worksheet**              | 文字列  | クエリ | _(オプション)_ ワークシート名がパスと異なる場合に使用するワークシート識別子。           |
| **folder**                 | 文字列  | クエリ | Aspose Cloudストレージ内のワークブックが格納されているフォルダへのパス。                |

この操作の完全な契約は[OpenAPI仕様](https://apireference.aspose.cloud/cells/#/Cells/PostCopyWorksheetColumns)で定義されています。

### cURLの例

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/copy?sourceColumnIndex=1&destinationColumnIndex=12&columnNumber=10" \
     -H "Authorization: Bearer $ASPOSE_TOKEN" \
     -H "accept: application/json"
```

### レスポンス

```json
{
  "Code": 200,
  "Status": "OK"
}
```

## エラー処理

APIは、エラーを説明するJSONペイロードを含む標準的なHTTPステータスコードを返します。

| ステータスコード | 意味                                             | 例のJSONボディ                                                       |
| ---------------- | ------------------------------------------------ | ------------------------------------------------------------------- |
| **400**          | 不正リクエスト – 無効なパラメータ                | `{ "Code": 400, "Message": "Invalid column index." }`               |
| **401**          | 認証エラー – トークンの欠落または無効            | `{ "Code": 401, "Message": "Access token is invalid or expired." }` |
| **404**          | 見つかりません – ワークブックまたはワークシートが存在しません | `{ "Code": 404, "Message": "Workbook not found." }`                 |
| **500**          | サーバーエラー – 予期しない状態                  | `{ "Code": 500, "Message": "An unexpected error occurred." }`       |

> **トラブルシューティング方法:** アクセストークンが有効であること、ワークブック名とワークシート名が正しいこと、および`sourceColumnIndex`、`destinationColumnIndex`、`columnNumber`がワークシートの列範囲内にあることを確認してください。

## クラウドSDKファミリー

SDKを使用すると、開発スピードを大幅に向上させることができます。SDKは低レベルの詳細を処理するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDKの完全な一覧については、[GitHubリポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例は、さまざまなSDKを使用してAspose.Cells Webサービスを呼び出す方法を示しています：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCopyWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCopyWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCopyWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCopyWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCopyWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCopyWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCopyWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCopyWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "列のコピーAPIを呼び出す際の認証方法は？",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "クライアントIDとシークレットを使用してAspose CloudからOAuth2アクセストークンを取得し、リクエストヘッダーに`Authorization: Bearer <access_token>`として含めてください。"
      }
    },
    {
      "@type": "Question",
      "name": "`sourceColumnIndex`と`destinationColumnIndex`の違いは？",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "`sourceColumnIndex`はコピー元の列の0始まりのインデックスです。`destinationColumnIndex`はコピーされた列を挿入する0始まりのインデックスです。"
      }
    },
    {
      "@type": "Question",
      "name": "コピー操作が失敗した場合のレスポンスは？",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "APIは200以外のステータスコード（例：400は不正リクエスト、401は認証エラー）を返します。レスポンスボディには、エラーを説明する`Code`フィールドと`Message`フィールドを含むJSONオブジェクトが含まれます。"
      }
    }
  ]
}
</script>
---