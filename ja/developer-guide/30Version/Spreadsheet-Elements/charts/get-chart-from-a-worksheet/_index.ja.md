---
title: "ワークシートからチャートを取得する"
type: docs
url: /charts/get/
aliases: [/get-chart-from-a-worksheet/]
weight: 10
keywords: "Aspose.Cells Cloud, Get Chart, Worksheet, REST API, Excel, Chart API, chart retrieval, Excel chart"
description: "Aspose.Cells Cloud REST API を使用して、ワークシートからチャートのメタデータおよびエクスポート形式を含むチャート情報を取得します。"
ArticleTitle: "ワークシートからチャートを取得する – Aspose.Cells Cloud API"
---

この REST API は、チャート情報を取得します。

**前提条件** – このエンドポイントを呼び出すには、有効な Aspose.Cells Cloud アカウント、アクティブなストレージロケーション、および JWT アクセストークンが必要です。API リクエストを行う前に、認証ガイドの手順に従ってトークンを取得してください。

## GetWorksheetChart API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartNumber}
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメータ

| パラメータ名 | 型     | 位置   | 説明                                     |
| ------------ | ------ | ------ | ----------------------------------------- |
| name         | string | path   | Excel ファイルの名前。                   |
| sheetName    | string | path   | チャートを含むワークシートの名前。       |
| chartNumber  | integer| path   | 取得するチャートの 0 から始まるインデックス。|
| format       | string | query  | 期望されるエクスポート形式（例: png, jpeg）。|
| folder       | string | query  | ドキュメントが保存されているフォルダのパス。|
| storageName  | string | query  | ストレージサービスの名前。               |

### **レスポンス**

```json
{
  "Code": 200,
  "Status": "OK",
  "Chart": {
    "Name": "Chart 1",
    "Type": "Bar",
    "Top": 50,
    "Left": 100,
    "Width": 400,
    "Height": 300,
    "DataRange": "A1:B5",
    "ShowLegend": true,
    "Format": "png"
  }
}
```

**HTTP ステータスコード**

| コード | 意味                     | 説明                                               |
|--------|--------------------------|----------------------------------------------------|
| 200    | OK                       | フィルターが正常に適用され、レスポンスに操作の詳細が含まれます。 |
| 400    | Bad Request              | パラメータが不足または無効（例: 未対応のファイル形式）。 |
| 401    | Unauthorized             | JWT トークンが無効または不足しています。             |
| 413    | Payload Too Large        | アップロードされたファイルがサイズ制限を超えています。 |
| 500    | Internal Server Error    | 予期しないサーバーエラーが発生しました。             |

## SDK を使用して GetWorksheetChart API を利用する方法

### GetWorksheetChart API の仕様

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/Charts/GetWorksheetChart) はパブリックに利用可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST による操作を実行できるようにします。

cURL コマンドラインツールを使用すると、Aspose.Cells Web サービスに簡単にアクセスできます。以下の例は、cURL を使用して Cloud API にリクエストを行う方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Chart": {
    "Name": "Chart 1",
    "Type": "Bar",
    "Top": 50,
    "Left": 100,
    "Width": 400,
    "Height": 300,
    "DataRange": "A1:B5",
    "ShowLegend": true,
    "Format": "png"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK を使用する

SDK を使用すると、開発を迅速に進められます。SDK が低レベルの詳細を処理するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全なリストについては、[GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスにリクエストを行う方法を示しています。

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-GetChart-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-GetChart-get-chart-from-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-GetWorksheetChart-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-get_worksheet_charts_info-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetChartAreaFromWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-GetChart-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-GetChart-get-chart-from-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-GetChart-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "6fbcaeac3bd9fe1d22319418799757bd" >}}

{{< /tab >}}

{{< /tabs >}}