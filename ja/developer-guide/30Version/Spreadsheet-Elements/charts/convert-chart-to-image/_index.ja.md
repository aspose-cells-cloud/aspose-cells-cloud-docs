---
title: "Excel チャートを画像に変換 – Aspose.Cells Cloud REST API"
type: docs
url: /ja/charts/to-image/
aliases: [  /ja/convert-charts-to-image/ ]
weight: 50
keywords: "Aspose.Cells Cloud, チャートを画像に変換, Excel チャート変換, REST API, 画像形式, PNG, JPEG, BMP, TIFF, GIF"
description: "Aspose.Cells Cloud REST API を使用して Excel チャートオブジェクトを PNG、JPEG、BMP、TIFF、または GIF 画像に変換する方法を学びます。エンドポイントの詳細、パラメーター、cURL の例、SDK スニペット、レスポンス例、エラー処理を含みます。"
ArticleTitle: "Excel チャートを画像に変換 – Aspose.Cells Cloud REST API"
---

この REST API は、**Aspose.Cells Cloud** を使用して **Excel チャート**を画像に変換する方法を示します。

## PutWorksheetAddChart API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartNumber}?format={format}
```

サポートされる画像形式は `png`、`jpeg`、`bmp`、`tiff`、`gif` です。

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメーター

| パラメーター名 | 型     | 位置   | 説明                 |
| -------------- | ------ | ------ | --------------------- |
| name           | string | path   | ドキュメント名。      |
| sheetName      | string | path   | シート名。            |
| chartNumber    | integer| path   | チャート番号。        |
| format         | string | query  | エクスポートするファイル形式。 |
| folder         | string | query  | ドキュメントフォルダー。 |
| storageName    | string | query  | ストレージ名。        |

### **レスポンス**

エンドポイントは、リクエストされた形式の画像ファイルをバイナリストリーム（例：`byte[]`）として返します。レスポンスの `Content‑Type` ヘッダーは、選択された画像形式に応じて `image/png`、`image/jpeg` などの値になります。

**HTTP ステータスコード**

| コード | 意味             | 説明                                         |
|------|------------------|----------------------------------------------|
| 200  | OK               | フィルターが正常に適用された。レスポンスには操作の詳細が含まれます。 |
| 400  | Bad Request      | パラメーターが不足している、または無効です（例：サポートされていないファイル形式）。 |
| 401  | Unauthorized     | JWT トークンが無効または不足しています。      |
| 413  | Payload Too Large| アップロードされたファイルがサイズ制限を超えています。 |
| 500  | Internal Server Error | 予期しないサーバーエラーが発生しました。 |

## SDK を使用した PutWorksheetAddChart API の利用方法

### PutWorksheetAddChart API の仕様

<a href="https://apireference.aspose.cloud/cells/#/Charts/GetWorksheetChart" rel="noopener noreferrer">OpenAPI 仕様</a>は、パブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザーから直接 REST アクセスを実行できるようにします。

cURL コマンドラインツールを使用して、Aspose.Cells Web サービスに簡単にアクセスできます。以下の例は、cURL を使用して Cloud API にリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0?format=jpg" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your_jwt_token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```text
byte[]
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、開発を迅速に進めることができます。SDK は低レベルの詳細を処理し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全なリストについては、<a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub リポジトリー</a>をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています。

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" tabName4="Node.js" tabName5="Python" tabName6="Android" tabName7="Objective C" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-ConvertChartToImage-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-GetWorksheetChartWithFormat-.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-get_chart_in_specified_format-.rb" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-ConvertChartToImage-1.js" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "ConvertChartToImage.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-ConvertChartToImage-convert-chart-to-image.java" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

例は近日公開予定です。

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-ConvertChartToImage-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "d22256010a610e1351ab15969a7adeef" >}}

{{< /tab >}}

{{< /tabs >}}