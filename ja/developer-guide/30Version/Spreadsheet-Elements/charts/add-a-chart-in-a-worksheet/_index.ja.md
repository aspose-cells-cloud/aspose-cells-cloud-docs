---
title: "ワークシートにチャートを追加する"
type: docs
url: /ja/charts/add/
aliases: [  /ja/add-a-chart-in-a-worksheet/ ]
weight: 20
description: "Aspose.Cells Cloud API v3.0 を使用して Excel ワークシートにチャートを追加する方法を学びます。エンドポイント、パラメータ、cURL の例、SDK スニペットを含みます。"
keywords:
  - "add chart Aspose.Cells"
  - "Aspose.Cells add chart API"
  - "chart API REST"
  - "Aspose.Cells SDK examples"
ArticleTitle: "ワークシートにチャートを追加する – Aspose.Cells Cloud API ガイド"
---

この REST API は、ワークシートに新しいチャートを追加します。

**前提条件**  
この操作を呼び出す前に、有効な JWT アクセストークンを取得し、対象のワークブックが指定されたフォルダまたはストレージの場所に保存されていることを確認してください。

## PutWorksheetAddChart API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>を必要とします。

### リクエストパラメータ

| パラメータ名              | 型      | 位置     | 説明                                                                                                                                                                                |
| ------------------------- | ------- | -------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **name**                  | string  | path     | ワークブック名。                                                                                                                                                                    |
| **sheetName**             | string  | path     | ワークシート名。                                                                                                                                                                    |
| **chartType**             | string  | query    | チャートの種類（チャートリソースの **Type** プロパティを参照）。サポートされているチャート種別には **Bar**、**Column**、**Line**、**Pie**、**Scatter**、**Area**、**Doughnut**、**Radar** などがあります。 |
| **upperLeftRow**          | integer | query    | チャート領域の左上行インデックス（0 始まり）。                                                                                                                                      |
| **upperLeftColumn**       | integer | query    | チャート領域の左上列インデックス（0 始まり）。                                                                                                                                      |
| **lowerRightRow**         | integer | query    | チャート領域の右下行インデックス（0 始まり）。                                                                                                                                      |
| **lowerRightColumn**      | integer | query    | チャート領域の右下列インデックス（0 始まり）。                                                                                                                                      |
| **area**                  | string  | query    | プロットする値を提供する範囲（例: `A1:B5`）。                                                                                                                                       |
| **isVertical**            | boolean | query    | チャートの向きが垂直かどうかを示します。                                                                                                                                            |
| **categoryData**          | string  | query    | カテゴリ軸の値の範囲（例: `D1:E10`）。                                                                                                                                              |
| **isAutoGetSerialName**   | boolean | query    | **true** の場合、系列名が自動的に生成されます。                                                                                                                                     |
| **title**                 | string  | query    | チャートのタイトル。                                                                                                                                                                |
| **folder**                | string  | query    | ワークブックを含むフォルダ。                                                                                                                                                        |
| **storageName**           | string  | query    | ストレージ名。                                                                                                                                                                      |
| **dataLabels**            | boolean | query    | **true** の場合、データラベルを表示します。                                                                                                                                         |
| **dataLabelsPosition**    | string  | query    | データラベルの位置（例: `Above`）。                                                                                                                                                 |
| **pivotTableSheet**       | string  | query    | ピボットテーブルを含むシート名。                                                                                                                                                    |
| **pivotTableName**        | string  | query    | ピボットテーブル名。                                                                                                                                                                |

### **応答**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP ステータスコード**

| コード | 意味             | 説明                                                                 |
| ------ | ---------------- | -------------------------------------------------------------------- |
| 200    | OK               | フィルターが正常に適用され、応答には操作の詳細が含まれます。         |
| 400    | Bad Request      | パラメータが不足している、または無効です（例: サポートされていないファイル形式）。 |
| 401    | Unauthorized     | JWT トークンが無効または不足しています。                             |
| 413    | Payload Too Large| アップロードされたファイルがサイズ制限を超えています。               |
| 500    | Internal Server Error | 予期しないサーバーエラーが発生しました。                            |

## SDK を使用した PutWorksheetAddChart API の使用方法

### PutWorksheetAddChart API 仕様

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/Charts/PutWorksheetAddChart) は、パブリックに利用可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST 相互作用を実行できるようにします。

cURL コマンドラインツールを使用して、Aspose.Cells Web サービスに簡単にアクセスできます。以下の例は、cURL を使用して Cloud API にリクエストを行う方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/charts?chartType=Bar&area=B1:F2&title=SalesState" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
# この操作にはリクエストボディは不要です
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

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、開発を最速で進めることができます。SDK は低レベルの詳細を抽象化し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全な一覧については、[GitHub リポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスにリクエストを行う方法を示しています。

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Objective C" tabName8="Perl" tabName9="Android" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-AddChart-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-AddChart-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-PutWorksheetAddChart-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-add_new_chart_to_worksheet-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "AddChartToWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-AddChart-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-AddChart-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Examples-Android-chart-AddChart-AddChart.jave" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "7fa79c30fca0c594c18c0f3937b6bcc9" >}}

{{< /tab >}}

{{< /tabs >}}