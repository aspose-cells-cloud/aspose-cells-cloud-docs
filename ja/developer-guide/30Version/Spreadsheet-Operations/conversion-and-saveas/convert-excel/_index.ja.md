---
title: "Excel ファイルを異なる形式に変換する"
ArticleTitle: "Excel ファイルを異なる形式に変換する"
second_title: "Document"
linktype: "Convert Excel"
type: docs
url: /ja/convert-an-excel-file-to-different-formats/
aliases:
  [
    /convert-excel-workbook-to-different-file-formats/,
    /convert/excel-to-different-formats/,
  ]
keywords: "Aspose.Cells Cloud, Excel 変換, ファイル形式変換, REST API, SDK, CSV, PDF, HTML, JSON, Markdown"
description: "Aspose.Cells Cloud REST API を使用して、Excel ワークブックを CSV、PDF、HTML、JSON、Markdown などの形式に変換します。"
weight: 10
---

このエンドポイントを呼び出す前に、有効な JWT トークンを取得し、ソースワークブックがサポートされているストレージ場所（例：Aspose Cloud ストレージ）に保存されていることを確認してください。トークンは `Authorization` ヘッダーに含め、必要に応じて `storageName` クエリパラメーターを指定してください。

この REST API は、Excel ファイルをさまざまな出力形式に変換します。

## PutConvertWorkBook API

```http
PUT https://api.aspose.cloud/v3.0/cells/convert
```

このリクエストは、HTTP の **PUT** で、マルチパート形式のコンテンツです（参照：[RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) または [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)）。  
マルチパートボディの最初のパートには **データファイル** が含まれ、2 番目のパートには **保存オプション** が含まれます。

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>を要求します。

### クエリパラメーター

| パラメーター名          | 型     | 説明                                                                                                                |
| ----------------------- | ------ | -------------------------------------------------------------------------------------------------------------------------- |
| `format`                | 文字列 | 変換先のファイル形式（例：CSV、XLS、HTML、PDF、XML、TXT、TIFF、PNG、JPG、GIF、EMF、BMP、MD、Numbers、WMF、SVG など）。      |
| `password`              | 文字列 | ソース Excel ファイルを開くために必要なパスワード。                                                                           |
| `outPath`               | 文字列 | 単一の出力ファイルの完全なパス（ファイル名と拡張子を含む）、または複数のファイルを生成する場合のフォルダーパス。 |
| `storageName`           | 文字列 | ソースファイルが存在するストレージの名前。                                                                         |
| `checkExcelRestriction` | 真偽値 | **true** の場合、セルや関連オブジェクトを変更する前に Excel の制限を検証します。                                     |
| `streamFormat`          | 文字列 | 入力ファイルストリームの形式。                                                                                           |
| `region`                | 文字列 | ワークブックに適用される地域設定。                                                                                 |
| `pageWideFitOnPerSheet` | 真偽値 | PDF に変換する際に、各ワークシートの幅に合わせてページ幅を調整します。                                                           |
| `pageTallFitOnPerSheet` | 真偽値 | PDF に変換する際に、各ワークシートの高さに合わせてページ高さを調整します。                                                          |
| `sheetName`             | 文字列 | 変換するワークシートの名前。                                                                                          |
| `pageIndex`             | 文字列 | 変換するページのインデックス（`sheetName` の指定が必要）。                                                                       |
| `onePagePerSheet`       | 真偽値 | **true** の場合、ワークシートごとに 1 つの PDF ページを生成します。                                                                       |
| `AutoRowsFit`           | 真偽値 | ワークブック内のすべての行を自動的に調整します。                                                                                        |
| `AutoColumnsFit`        | 真偽値 | ワークブック内の列幅を自動的に調整します。                                                                                   |

### リクエストボディパラメーター

| パラメーター名 | 型         | 説明                                                    |
| -------------- | ---------- | -------------------------------------------------------------- |
| `datafile`     | データファイル | マルチパートボディの最初のパートに配置された Excel ファイル。 |
| `SaveOptions`  | オブジェクト   | マルチパートボディの 2 番目のパートに配置された保存オプション。  |

### **レスポンス**

```json
{
    "Name": "ResponseFile",
    "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
    }
}
```

**HTTP ステータスコード**

| コード | 意味                         | 説明                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | フィルターが正常に適用され、レスポンスに操作の詳細が含まれます。 |
| 400  | Bad Request                 | パラメーターが不足している、または無効です（例：サポートされていないファイル形式）。 |
| 401  | Unauthorized                | JWT トークンが無効または不足しています。 |
| 413  | Payload Too Large           | アップロードされたファイルがサイズ制限を超えています。 |
| 500  | Internal Server Error       | 予期しないサーバーエラーが発生しました。 |
## SDK を使用した PutConvertWorkBook API の使用方法

### PutConvertWorkBook API の仕様

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) は、Web ブラウザから直接 REST 通信を可能にする公開可能なインターフェースを定義しています。

### cURL の例

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/convert?format=html" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: Containerize.Swagger" \
     -d '{"File":{}}'
```

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、低レベルの詳細を処理できるため、開発が加速し、ビジネスロジックに集中できます。Aspose.Cells Cloud SDK の完全なリストは [GitHub リポジトリ](https://github.com/aspose-cells-cloud) を参照してください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutConvertWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutConvertWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "ExamplePutConvertWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "ExamplePutConvertWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "ExamplePutConvertWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "ExamplePutConvertWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "ExamplePutConvertWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "ExamplePutConvertWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}
---