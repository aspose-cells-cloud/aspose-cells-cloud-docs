---
title: "ワークシートからチャートを削除する"
type: docs
url: /charts/delete/
aliases: [/delete-a-chart-from-a-worksheet/]
weight: 40
keywords:
  - "Aspose.Cells"
  - "REST API"
  - "Delete Chart"
  - "Worksheet"
  - "Excel"
  - "Cloud SDK"
  - "Chart Deletion"
  - "API Reference"
description: "Aspose.Cells Cloud REST API を使用して、0 から始まるインデックスでワークシートのチャートを削除します。"
ArticleTitle: "Aspose.Cells Cloud REST API を使用してワークシートからチャートを削除する"
---

この REST API は、インデックスでワークシート上のチャートを削除します。

関連する操作については、**[チャートの追加](#)** および **[チャートの取得](#)** のページをご覧ください。

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}
```

### セキュリティと認証

Aspose.Cells Cloud API は安全であり、[JWT トークンベースの認証](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)が必要です。

### リクエストパラメータ

| パラメータ名     | 型     | 位置   | 説明                                      |
| -------------- | ------ | ------ | ----------------------------------------- |
| name           | 文字列  | パス   | ワークブックの名前。                      |
| sheetName      | 文字列  | パス   | ワークシートの名前。                      |
| chartIndex     | 整数   | パス   | 削除するチャートの 0 から始まるインデックス。 |
| folder         | 文字列  | クエリ | ワークブックが格納されているフォルダ。      |
| storageName    | 文字列  | クエリ | 使用するストレージの名前。                  |


### **レスポンス**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP ステータスコード**

| コード | 意味                      | 説明                                               |
|------|---------------------------|----------------------------------------------------|
| 200  | OK                        | フィルターが正常に適用された。応答には操作の詳細が含まれる。 |
| 400  | Bad Request               | パラメータが不足または無効（例：サポートされていないファイル形式）。 |
| 401  | Unauthorized              | JWT トークンが無効または不足している。                 |
| 413  | Payload Too Large         | アップロードされたファイルがサイズ制限を超えている。       |
| 500  | Internal Server Error     | 予期しないサーバーエラー。                             |

## SDK を使用して PutWorksheetAddChart API を活用する方法

### PutWorksheetAddChart API 仕様

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/Charts/DeleteWorksheetDeleteChart)は、パブリックにアクセス可能なプログラミングインターフェースを定義し、ウェブブラウザから直接 REST 通信を実行できるようにします。

cURL コマンドラインツールを使用して Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例は、cURL を使用して Cloud API にリクエストを行う方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0" \
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

API は以下のステータスコードを返します。

| コード | 説明                                     |
|------|------------------------------------------|
| 200  | チャートが正常に削除された                   |
| 400  | リクエストエラー（例：無効なインデックス）        |
| 401  | 認証エラー（JWT トークンが不足または無効）        |
| 404  | ワークブック、ワークシート、またはチャートが見つからない |
| 500  | サーバーエラー                             |

**エラー処理:** 詳細なエラー情報については、OpenAPI 仕様内の汎用エラーモデルを参照してください。

### Aspose.Cells Cloud SDK を使用する

SDK を使用すると、開発を高速化できます。SDK は低レベルの詳細を抽象化し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全な一覧については、[GitHub リポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-DeleteChart-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-DeleteOneChart-delete-single-chart.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-DeleteWorksheetDeleteChart-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-delete_worksheet_chart_by_index-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "DeleteChartExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-DeleteChart-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-DeleteOneChart-delete-single-chart.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-DeleteChart-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "b858c32efd7b745ebb75d61898ec50e0" >}}

{{< /tab >}}

{{< /tabs >}}
---