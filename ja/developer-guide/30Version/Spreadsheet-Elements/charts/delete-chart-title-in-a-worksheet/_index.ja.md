---
title: "ワークシート内のチャート タイトルを削除する"
type: docs
url: /ja/charts/delete-chart-title/
aliases: [  /ja/delete-chart-title-in-a-worksheet/ ]
weight: 150
keywords: "Aspose.Cells, クラウド API, チャート タイトルの削除, Excel, REST, SDK"
description: "Aspose.Cells Cloud REST API (v4.0) を使用して Excel ワークシートからチャート タイトルを削除する方法を学びます。cURL、SDK の例、およびエラー処理を含みます。"
---

この REST API は、チャートのタイトルを削除します。

## REST API

```bash
DELETE https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/title
```

### セキュリティと認証

Aspose.Cells Cloud API は安全であり、[JWT トークンベースの認証](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)が必要です。

### リクエストパラメータ

| パラメータ名   | 型     | 位置   | 説明                         |
| -------------- | ------ | ------ | ----------------------------- |
| name           | 文字列 | パス   | ワークブック ファイル名。     |
| sheetName      | 文字列 | パス   | ワークシート名。              |
| chartIndex     | 整数 | パス   | チャートの 0 から始まるインデックス。  |
| folder         | 文字列 | クエリ | ワークブックを含むフォルダ。 |
| storageName    | 文字列 | クエリ | ストレージ名。                |

### **レスポンス**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP ステータスコード**

| コード | 意味                   | 説明                                             |
|------|------------------------|--------------------------------------------------|
| 200  | OK                     | フィルターが正常に適用され、レスポンスに操作の詳細が含まれます。 |
| 400  | Bad Request            | パラメータが不足または無効です（例：サポートされていないファイル形式）。 |
| 401  | Unauthorized           | JWT トークンが無効または不足しています。 |
| 413  | Payload Too Large      | アップロードされたファイルがサイズ制限を超えています。 |
| 500  | Internal Server Error  | 予期しないサーバーエラーが発生しました。 |

## SDK を使用した DeleteWorksheetChartTitle API の使い方

### DeleteWorksheetChartTitle API の仕様

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/Charts/DeleteWorksheetChartTitle)は、パブリックにアクセス可能なプログラミング インターフェースを定義し、Web ブラウザから直接 REST アクセスを実行できるようにします。

cURL コマンドラインツールを使用すると、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例は、認証に必要な **Bearer JWT** トークンを含む呼び出し方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v4.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/title" \
  -X DELETE \
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

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、開発を高速化できます。SDK は低レベルの詳細を処理し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全な一覧は [GitHub リポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-DeleteChartTitle-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-DeleteChartTitle-delete-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-DeleteWorksheetChartTitle-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-hide_title_in_chart-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "DeleteChartExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-DeleteChartTitle-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-DeleteChartTitle-delete-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-DeleteChartTitle-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "3898d60ea8f7ea7bb460ffb5d7d29504" >}}

{{< /tab >}}

{{< /tabs >}}

---