---
title: "ワークシートからチャートの凡例を取得する"
type: docs
url: /charts/legend/get/
aliases: [/get-chart-legend-from-a-worksheet/]
weight: 80
keywords: "Aspose.Cells, チャートの凡例, REST API, Excel, クラウドSDK, チャート凡例の取得, ワークシート, スプレッドシート"
description: "Aspose.Cells Cloud REST API (v3.0) を使用して、Excel ブック内の特定のワークシートにあるチャートの凡例を取得します。エンドポイント、パラメータ、cURL サンプル、SDK スニペットを含みます。"
---

**Get Chart Legend** 操作は、Excel ブック内のワークシートに存在するチャートの凡例情報を返します。このエンドポイントは **Aspose.Cells Cloud API v3.0** の一部であり、凡例の位置、フォント、サイズ、書式などのプロパティを読み取る場合に使用できます。

## **REST API**

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/legend
```

### セキュリティと認証

Aspose.Cells Cloud API は安全であり、[JWT トークンによる認証](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)が必要です。

### リクエストパラメータ

| パラメータ名 | 型     | 位置   | 説明                             |
|------------|------|------|----------------------------------|
| name       | 文字列 | path | ブックファイル名。                  |
| sheetName  | 文字列 | path | ワークシート名。                    |
| chartIndex | 整数  | path | チャートの 0 から始まるインデックス。  |
| folder     | 文字列 | query | ブックが保存されているフォルダのパス。 |
| storageName| 文字列 | query | ストレージ名。                      |

### **レスポンス**

```json
{
  "Legend": {
    "Position": "Right",
    "LegendEntries": {
      "link": {
        "Href": "/legendEntries",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "Area": {
      "BackgroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
      "FillFormat": {
        "Type": "Automatic",
        "SolidFill": null,
        "PatternFill": null,
        "TextureFill": null,
        "GradientFill": null,
        "ImageData": null
      },
      "ForegroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
      "Formatting": "Automatic",
      "InvertIfNegative": false,
      "Transparency": 0.0
    },
    "AutoScaleFont": true,
    "BackgroundMode": "Automatic",
    "Border": {
      "BeginArrowLength": "Medium",
      "BeginArrowWidth": "Medium",
      "BeginType": "None",
      "CapType": "Flat",
      "Color": { "A": 0, "R": 0, "G": 0, "B": 0 },
      "CompoundType": "Single",
      "DashType": "Solid",
      "EndArrowLength": "Medium",
      "EndArrowWidth": "Medium",
      "EndType": "None",
      "GradientFill": null,
      "IsAuto": true,
      "IsAutomaticColor": true,
      "IsVisible": true,
      "JoinType": "Round",
      "Style": "Solid",
      "Transparency": 0.0,
      "Weight": "HairLine",
      "WeightPt": 0.0
    },
    "Font": {
      "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
      "DoubleSize": 10.0,
      "IsBold": false,
      "IsItalic": false,
      "IsStrikeout": false,
      "IsSubscript": false,
      "IsSuperscript": false,
      "Name": "Arial",
      "Size": 10,
      "Underline": "None"
    },
    "IsAutomaticSize": true,
    "IsInnerMode": null,
    "Shadow": false,
    "ShapeProperties": null,
    "Width": 823,
    "Height": 1043,
    "X": 3125,
    "Y": 1466,
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/legend",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 0,
  "Status": "0"
}
```

**HTTP ステータスコード**

| コード | 意味              | 説明                                      |
|------|-------------------|-------------------------------------------|
| 200  | OK                | フィルターが正常に適用され、レスポンスに操作の詳細が含まれます。 |
| 400  | Bad Request       | パラメータが不足または無効です（例：サポートされていないファイル形式）。 |
| 401  | Unauthorized      | JWT トークンが無効または不足しています。             |
| 413  | Payload Too Large | アップロードされたファイルがサイズ制限を超えています。        |
| 500  | Internal Server Error | 予期しないサーバーエラーが発生しました。             |

## SDK を使用した GetWorksheetChartLegend API の使用方法

### GetWorksheetChartLegend API 仕様

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/Charts/GetWorksheetChartLegend) はパブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST 通信を実行できるようにします。

cURL コマンドラインツールを使用すると、Aspose.Cells Web サービスに簡単にアクセスできます。以下の例では、cURL を使用してクラウド API を呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/legend" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Legend": {
    "Position": "Right",
    "LegendEntries": {
      "link": {
        "Href": "/legendEntries",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "Area": {
      "BackgroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
      "FillFormat": {
        "Type": "Automatic",
        "SolidFill": null,
        "PatternFill": null,
        "TextureFill": null,
        "GradientFill": null,
        "ImageData": null
      },
      "ForegroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
      "Formatting": "Automatic",
      "InvertIfNegative": false,
      "Transparency": 0.0
    },
    "AutoScaleFont": true,
    "BackgroundMode": "Automatic",
    "Border": {
      "BeginArrowLength": "Medium",
      "BeginArrowWidth": "Medium",
      "BeginType": "None",
      "CapType": "Flat",
      "Color": { "A": 0, "R": 0, "G": 0, "B": 0 },
      "CompoundType": "Single",
      "DashType": "Solid",
      "EndArrowLength": "Medium",
      "EndArrowWidth": "Medium",
      "EndType": "None",
      "GradientFill": null,
      "IsAuto": true,
      "IsAutomaticColor": true,
      "IsVisible": true,
      "JoinType": "Round",
      "Style": "Solid",
      "Transparency": 0.0,
      "Weight": "HairLine",
      "WeightPt": 0.0
    },
    "Font": {
      "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
      "DoubleSize": 10.0,
      "IsBold": false,
      "IsItalic": false,
      "IsStrikeout": false,
      "IsSubscript": false,
      "IsSuperscript": false,
      "Name": "Arial",
      "Size": 10,
      "Underline": "None"
    },
    "IsAutomaticSize": true,
    "IsInnerMode": null,
    "Shadow": false,
    "ShapeProperties": null,
    "Width": 823,
    "Height": 1043,
    "X": 3125,
    "Y": 1466,
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/legend",
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

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、開発を迅速化できます。SDK は低レベルの詳細を処理し、プロジェクトのタスクに集中できるようになります。Aspose.Cells Cloud SDK の完全な一覧については、[GitHub リポジトリ](https://github.com/aspose-cells-cloud) を確認してください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています。

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-GetChartLegend-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-GetChartLegend-get-chart-legend.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-GetWorksheetChartLegend-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-get_chart_legend-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetChartLegendFromWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-GetChartLegend-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-GetChartLegend-get-chart-legend.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-GetChartLegend-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "76b8d73d934c0f03675299687805040f" >}}

{{< /tab >}}

{{< /tabs >}}

---