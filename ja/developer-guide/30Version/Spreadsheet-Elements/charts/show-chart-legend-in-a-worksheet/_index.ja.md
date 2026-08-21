---
title: "ワークシート内のチャート凡例を表示する"
type: docs
url: /charts/legend/show/
aliases: [/show-chart-legend-in-a-worksheet/]
weight: 100
keywords: "Aspose.Cells Cloud, チャート凡例 API, Excel チャート凡例, REST PUT チャート凡例, Aspose API v3.0"
description: "Aspose.Cells Cloud REST API（v3.0）を使用して、Excelワークシート内のチャートに凡例を表示する方法を学びます。エンドポイントの詳細、パラメータ、cURLの例、SDKスニペットを含みます。"
---

このREST APIを使用すると、Excelワークブックのワークシート内に配置されたチャートに**凡例**（データ系列を識別する説明用ボックス）を表示できます。

## REST API

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/legend
```

### リクエストパラメータ

| パラメータ名   | タイプ    | 位置   | 説明                                     |
| -------------- | ------- | ------ | ----------------------------------------- |
| name           | string  | path   | ワークブックのファイル名。               |
| sheetName      | string  | path   | チャートを含むワークシート名。           |
| chartIndex     | integer | path   | チャートの0から始まるインデックス。      |
| folder         | string  | query  | ワークブックが格納されているフォルダ。   |
| storageName    | string  | query  | ストレージサービスの名前。               |

[OpenAPI仕様書](https://apireference.aspose.cloud/cells/#/Charts/PutWorksheetChartLegend)では、パブリックに利用可能なプログラミングインタフェースが定義されており、Webブラウザから直接RESTインタフェースを操作できます。

認証は、**Authorization**ヘッダにBearer JWTトークンを指定して行います。

cURLコマンドラインツールを使用すれば、Aspose.Cellsウェブサービスに簡単にアクセスできます。以下の例では、cURLを使用した呼び出し方法を示します。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/legend" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

このAPIが返すHTTPステータスコードは以下の通りです：

- **200 OK** – 凡例の表示が正常に完了しました。
- **400 Bad Request** – 無効なパラメータが指定されました。
- **401 Unauthorized** – 認証に失敗しました。
- **404 Not Found** – 指定されたワークブック、ワークシート、またはチャートが存在しません。
- **500 Internal Server Error** – サーバーで予期しないエラーが発生しました。

{{< /tab >}}

{{< /tabs >}}

## クラウドSDKファミリ

SDKを使用することは、開発を高速化する最良の方法です。SDKは低レベルの詳細な処理を処理し、開発者はプロジェクトのタスクに集中できます。Aspose.Cells Cloud SDKの完全な一覧については、[GitHubリポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例では、さまざまなSDKを使用してAspose.Cellsウェブサービスを呼び出す方法を示します：

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-ShowChartLegend-1.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-ShowChartLegend-show-chart-legend.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-PutWorksheetChartLegend-.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-show_legend_in_chart-.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "ShowChartLegendInAWorksheet.py" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-ShowChartLegend-1.js" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-ShowChartLegend-show-chart-legend.java" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-ShowChartLegend-1.pl" >}}
{{< /tab >}}

{{< tab tabNum="10" >}}
{{< gist "aspose-cells-cloud-gists" "f9f1d14e3b6985c0a44ec7acdd4f56b2" >}}
{{< /tab >}}

{{< /tabs >}}

---