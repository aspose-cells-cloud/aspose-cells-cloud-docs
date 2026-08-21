---
title: "ワークシート内のチャート凡例を更新する"
type: docs
url: /charts/legend/update/
aliases: [/update-chart-legend-in-a-worksheet/]
weight: 160
keywords: "Aspose.Cells, クラウド, Excel, チャート, 凡例, REST API, 更新, ワークシート, cURL, SDK"
description: "Aspose.Cells Cloud REST API を使用して Excel ワークシート内のチャート凡例を更新する方法。cURL リクエストの例と複数のプログラミング言語向けの SDK コードスニペットを紹介します。"
ArticleTitle: "ワークシート内のチャート凡例を更新する – Aspose.Cells Cloud API ガイド"
---

この REST API は、チャートの凡例を更新します。

**前提条件:** このエンドポイントを使用するには、有効な Aspose Cloud JWT トークンが必要であり、対象のワークブックはサポートされているストレージの場所（デフォルトは Aspose Cloud ストレージ）に保存されている必要があります。ワークブック名、ワークシート名、およびチャートのインデックスが正しいことを確認してください。

チャート凡例は、チャート内のデータ系列の名前と記号を表示します。凡例を更新することで、フォントスタイル、色、影などの外観をカスタマイズできます。

## PostWorksheetChartLegend API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/legend
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>を必要とします。

### リクエストパラメータ

| パラメータ名 | 型     | 位置   | 説明                                   |
| ------------ | ------ | ------ | --------------------------------------- |
| name         | string | path   | ワークブック名。                         |
| sheetName    | string | path   | ワークシート名。                         |
| chartIndex   | integer | path  | 変更するチャートのインデックス。          |
| legend       | object | body   | 凡例設定を定義する JSON オブジェクト。     |
| folder       | string | query  | ワークブックが格納されているフォルダー。   |
| storageName  | string | query  | ストレージ名。                           |

[OpenAPI スペック](https://apireference.aspose.cloud/cells/#/Charts/PostWorksheetChartLegend) はパブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザーから直接 REST によるやり取りを可能にします。

cURL コマンドラインツールを使用して、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例は、cURL を使用してクラウド API を呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.com/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/legend" \
-d '{"Font":{"Color":{"A":"1","R":"255","G":"0","B":"0"},"DoubleSize":10.0,"IsBold":true,"IsItalic":false,"IsStrikeout":false,"IsSubscript":false,"IsSuperscript":false,"Name":"Arial","Size":15,"Underline":"None"},"Shadow":true}' \
-X POST \
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

## クラウド SDK ファミリー

SDK を使用すると開発が加速します。SDK が低レベルの詳細を処理するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全な一覧は [GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-UpdateChartLegend-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-UpdateChartLegend-update-chart-legend.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-PostWorksheetChartLegend-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-update_chart_legend-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-UpdateChartLegend-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "UpdateChartLegendInWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-UpdateChartLegend-update-chart-legend.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-UpdateChartLegend-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "74fffa317bc5ba65dc6536005e5bb683" >}}

{{< /tab >}}

{{< /tabs >}}