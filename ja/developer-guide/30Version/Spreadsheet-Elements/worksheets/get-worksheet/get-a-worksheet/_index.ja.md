---
title: "Aspose.Cells Cloud API を使用してワークシートをエクスポート – 対応フォーマット、cURL および SDK サンプル"
second_title: "ドキュメント"
linktitle: "ワークシートのエクスポート"
type: docs
url: /ja/worksheets/get-worksheet/
keywords: "Aspose.Cells Cloud Get Worksheet, ワークシートのエクスポート, Excel API, REST, CSV, PDF, PNG, JPEG, GIF, BMP, TIFF, EMF, XPS, OTS, XLS, XLSX, XLSB, XLSM, ODS, FODS, Numbers, クラウド API"
description: "Aspose.Cells Cloud REST API を使用して Excel ファイルから単一のワークシートをエクスポートする方法を学習します。エンドポイント、パラメーター、修正済み cURL の例、認証詳細、エラーハンドリング、および C#、Java、Python などの SDK スニペットを含みます。"
weight: 10
ArticleTitle: "Aspose.Cells Cloud API を使用してワークシートをエクスポート – 対応フォーマット、cURL および SDK サンプル"
---

この REST API を使用すると、Excel ファイルからワークシートをさまざまなファイルフォーマットに**エクスポート**できます。

**概要** – **Get Worksheet** エンドポイントを使用して、ワークブックから単一のワークシートを希望のフォーマットでダウンロードします。

以下のフォーマットへエクスポートできます：

| フォーマット | 拡張子 | MIME タイプ                                                         |
| ---------- | ---- | ------------------------------------------------------------------ |
| XLS        | .xls | application/vnd.ms-excel                                          |
| XLSX       | .xlsx | application/vnd.openxmlformats-officedocument.spreadsheetml.sheet |
| XLSB       | .xlsb | application/vnd.ms-excel.sheet.binary.macroEnabled.12             |
| CSV        | .csv | text/csv                                                          |
| TSV        | .tsv | text/tab-separated-values                                         |
| XLSM       | .xlsm | application/vnd.ms-excel.sheet.macroEnabled.12                    |
| ODS        | .ods | application/vnd.oasis.opendocument.spreadsheet                    |
| TXT        | .txt | text/plain                                                        |
| PDF        | .pdf | application/pdf                                                   |
| OTS        | .ots | application/vnd.oasis.opendocument.spreadsheet-template           |
| XPS        | .xps | application/vnd.ms-xpsdocument                                    |
| DIF        | .dif | application/x-dif                                                 |
| PNG        | .png | image/png                                                         |
| JPEG       | .jpeg | image/jpeg                                                        |
| GIF        | .gif | image/gif                                                         |
| BMP        | .bmp | image/bmp                                                         |
| WMF        | .wmf | image/wmf                                                         |
| TIFF       | .tiff | image/tiff                                                        |
| EMF        | .emf | image/emf                                                         |
| NUMBERS    | .numbers | application/vnd.apple.numbers                                     |
| FODS       | .fods | application/vnd.oasis.opendocument.spreadsheet-flat-xml           |

## セキュリティと認証
Aspose.Cells Cloud API は安全であり、[JWT トークンベースの認証](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)を必要とします。

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}
```

### **リクエストパラメーター**

| パラメーター名           | 型      | 位置   | 説明                                                                 |
| ------------------------ | ------- | ------ | ------------------------------------------------------------------- |
| **name**                 | 文字列  | path   | **必須です。** Excel ファイルの名前。                               |
| **sheetName**            | 文字列  | path   | **必須です。** エクスポートするワークシートの名前。                      |
| **format**               | 文字列  | query  | エクスポートされたワークシートの対象ファイルフォーマット（例: `pdf`, `png`）。 |
| **verticalResolution**   | 整数    | query  | 解像度をサポートするフォーマット（例: PNG、JPEG）の画像 DPI。            |
| **horizontalResolution** | 整数    | query  | 解像度をサポートするフォーマットの画像 DPI。                           |
| **area**                 | 文字列  | query  | エクスポートするセル範囲（例: `A1:D10`）。                              |
| **pageIndex**            | 整数    | query  | ワークシートがページ分割されている場合にエクスポートするページのインデックス。        |
| **folder**               | 文字列  | query  | ソースファイルが配置されているストレージ内のフォルダーのパス。            |
| **storageName**          | 文字列  | query  | Aspose Cloud ストレージの名前。                                   |

<a href="https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheet" target="_blank" rel="noopener noreferrer">OpenAPI Specification</a> は、パブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST 相互作用を実行できるようにします。

cURL コマンドラインツールを使用すると、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例では、cURL を使ってクラウド API を呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1?format=gif" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt_token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```http
HTTP/1.1 200 OK
Content-Type: image/gif
Content-Disposition: attachment; filename="Sheet1.gif"

<バイナリデータ>
```

{{< /tab >}}

{{< /tabs >}}

## エラーハンドリング

API は標準的な HTTP ステータスコードを返します。主なレスポンスは以下の通りです：

| ステータスコード | 意味                                                         | 例 JSON ボディ                             |
| -------------- | ------------------------------------------------------------ | ----------------------------------------- |
| **200**        | 成功 – ワークシートのストリームが返されます。                 | `{ "stream": "..." }`                      |
| **400**        | 不正リクエスト – パラメーターが不足している、または無効です。                | `{ "error": "Invalid format parameter." }` |
| **401**        | 認証されていません – JWT トークンが無効または不足しています。                | `{ "error": "Authentication failed." }`    |
| **404**        | 見つかりません – 指定されたファイルまたはワークシートが存在しません。 | `{ "error": "Worksheet not found." }`      |
| **500**        | サーバー内部エラー – サーバー上で予期しない状態が発生しました。 | `{ "error": "Unexpected error." }`         |

これらのレスポンスをクライアントコード内で適切に処理し、ユーザーに適切なフィードバックを提供してください。

## クラウド SDK ファミリー

SDK を使用すると、開発を最速で進めることができます。SDK は低レベルの詳細を処理し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全なリストは <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub リポジトリ</a> をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetWithFormat.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetWithFormat.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetWithFormat.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}