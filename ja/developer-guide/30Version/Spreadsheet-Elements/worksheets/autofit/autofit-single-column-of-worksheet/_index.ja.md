---
title: "Aspose.Cells Cloud API を使用して Excel の列を自動調整する – クイックガイド"
second_title: "ドキュメント"
linktitle: "列"
type: docs
url: /ja/worksheets/autofit/column/
aliases: [  /ja/autofit-single-column-of-worksheet/ ]
keywords: "Aspose.Cells Cloud, 列の自動調整, Excel API, REST API, SDK, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go"
description: "Aspose.Cells Cloud REST API を使用して Excelワークシート内の列（または列の範囲）を自動的にリサイズする方法を学びます。cURLおよびSDK（C#、Java、Python など）の使用例と、リクエスト・レスポンスの詳細を含みます。"
weight: 10
---

この REST API は、Excel ワークシート上の単一の列または連続した列の範囲の幅を自動的に調整します。

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autofitcolumns
```

### リクエストパラメータ

| パラメータ名         | タイプ     | 位置   | 説明                                                                                          |
| -------------------- | ---------- | ------ | --------------------------------------------------------------------------------------------- |
| name                 | string     | path   | Excel ファイルの名前。                                                                        |
| sheetName            | string     | path   | ワークシートの名前。                                                                          |
| firstColumn          | integer    | query  | 自動調整する最初の列の 0 から始まるインデックス。                                              |
| lastColumn           | integer    | query  | 自動調整する最後の列の 0 から始まるインデックス。                                              |
| autoFitterOptions    | object     | body   | 自動調整動作を制御するオプション（[AutoFitterOptions](/cells/auto-filter-options) 参照）。     |
| firstRow             | integer    | query  | 列幅を計算する際に考慮される最初の行の 0 から始まるインデックス。                              |
| lastRow              | integer    | query  | 列幅を計算する際に考慮される最後の行の 0 から始まるインデックス。                              |
| folder               | string     | query  | ファイルが配置されているストレージ内のフォルダー。                                            |
| storageName          | string     | query  | ストレージサービスの名前。                                                                    |

### エラーレスポンス

| HTTP ステータス | 意味                                     | 例（JSON ボディ）                                           |
| --------------- | ---------------------------------------- | ------------------------------------------------------------ |
| 400             | 無効なパラメータ                         | `{"Code":400,"Message":"Invalid parameter 'firstColumn'."}` |
| 401             | 認証エラー – JWT トークンが欠落または無効 | `{"Code":401,"Message":"Authorization failed."}`            |
| 404             | ファイルまたはワークシートが見つからない | `{"Code":404,"Message":"Worksheet 'Sheet1' not found."}`    |
| 500             | サーバー内部エラー                       | `{"Code":500,"Message":"An unexpected error occurred."}`    |

[OpenAPI スペック](https://apireference.aspose.cloud/cells/#/Worksheets/PostAutofitWorksheetColumns) はパブリックに利用可能なプログラミングインターフェースを定義しており、Web ブラウザから直接 REST 操作を実行できます。

**cURL** コマンドラインツールを使用して Aspose.Cells Cloud サービスを呼び出すことができます。以下の例は、列の自動調整エンドポイントを呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleAutoFit.xlsx/worksheets/Sheet1/autofitcolumns?firstColumn=2&lastColumn=2" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"AutoFitMergedCells": true, "IgnoreHidden": true, "OnlyAuto": true}'
```

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

## クラウド SDK ファミリー

SDK を使用すると、API をアプリケーションに統合する最も速い方法です。SDK は低レベルの詳細を処理するため、ビジネスロジックの開発に集中できます。Aspose.Cells Cloud SDK の完全なリストは [GitHub リポジトリ](https://github.com/aspose-cells-cloud) を参照してください。

以下のコード例は、さまざまな SDK を使用して列の自動調整エンドポイントを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}