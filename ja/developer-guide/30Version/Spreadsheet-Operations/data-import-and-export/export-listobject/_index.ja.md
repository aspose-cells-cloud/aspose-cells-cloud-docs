---
title: "リスト オブジェクトのエクスポート"
second_title: "ドキュメント"
linktitle: "リスト オブジェクト"
type: docs
url: /export-excel-listobject-to-different-formats/
aliases: [/export/excel-listobject-to-different-formats/]
keywords: "ListObjectのエクスポート, Excel ListObject, Aspose.Cells Cloud, REST API, PDF, CSV, JSON, XLSX, ODS, PNG, TIFF, SDK"
description: "Aspose.Cells Cloud REST API を使用すると、Excel の ListObject をさまざまなファイル形式にエクスポートできます。SDK は C#、Java、Python、Node.js、Go、PHP、Ruby、Perl、Swift など多くのプログラミング言語で利用可能です。"
weight: 20
---

以下の形式にエクスポート可能です：[XLS](https://docs.fileformat.com/spreadsheet/xls/)、[XLSX](https://docs.fileformat.com/spreadsheet/xlsx/)、[XLSB](https://docs.fileformat.com/spreadsheet/xlsb/)、[CSV](https://docs.fileformat.com/spreadsheet/csv/)、[TSV](https://docs.fileformat.com/spreadsheet/tsv/)、[XLSM](https://docs.fileformat.com/spreadsheet/xlsm/)、[ODS](https://docs.fileformat.com/spreadsheet/ods/)、[TXT](https://docs.fileformat.com/word-processing/txt/)、[PDF](https://docs.fileformat.com/pdf/)、[OTS](https://docs.fileformat.com/spreadsheet/ots/)、[XPS](https://docs.fileformat.com/page-description-language/xps/)、[DIF](https://docs.fileformat.com/spreadsheet/dif/)、[PNG](https://docs.fileformat.com/Image/png/)、[JPEG](https://docs.fileformat.com/image/jpeg/)、[BMP](https://docs.fileformat.com/image/bmp/)、[SVG](https://docs.fileformat.com/page-description-language/svg/)、[TIFF](https://docs.fileformat.com/image/tiff/)、[EMF](https://docs.fileformat.com/image/emf/)、[NUMBERS](https://docs.fileformat.com/spreadsheet/numbers/)、[FODS](https://docs.fileformat.com/spreadsheet/fods/)。

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/export
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメータ

| パラメータ名 | 型 | Path/Query String/HTTP Body | 必須 | 説明 |
|--------------|----|-----------------------------|------|------|
| file | file | formData | True | アップロードするファイル |
| objectType | string | query | True | エクスポートするオブジェクトのタイプ。チャートをエクスポートする場合は `chart` を使用します。その他の可能な値は `worksheet`、`picture` などです。 |
| format | string | query | True | 期望する出力形式。サポートされる値：`png`、`jpeg`、`gif`、`bmp`、`svg`、`tiff`、`emf`、`wmf`、`pdf` |

### レスポンス

```json
{
  "Files": [
    {
      "Filename": "Book1_xlsx_Sheet1_ListObjects_0.tif",
      "FileSize": 390,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet2_ListObjects_0.tif",
      "FileSize": 10040,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet1_ListObjects_0.tif",
      "FileSize": 382,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

**HTTP ステータスコード**

| コード | 意味 | 説明 |
|--------|------|------|
| 200 | OK | フィルターが正常に適用され、レスポンスには操作の詳細が含まれます。 |
| 400 | Bad Request | パラメータが不足または無効（例：サポートされていないファイル形式）です。 |
| 401 | Unauthorized | JWT トークンが無効または不足しています。 |
| 413 | Payload Too Large | アップロードされたファイルがサイズ制限を超えています。 |
| 500 | Internal Server Error | 予期しないサーバーエラーが発生しました。 |

## SDK を使った PostExport API の使用方法

### PostExport API の仕様

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) はパブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST 通信を実行できるようにします。

**cURL** コマンドラインツールを使用して Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例は、cURL を使ってクラウド API にリクエストを行う方法を示しています。

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=listobject&format=tiff" \
-H "accept: multipart/form-data" \
-H "Content-Type: multipart/form-data" \
-H "x-aspose-client: Containerize.Swagger" \
-d '{"File":{}}'
```

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、開発を迅速化できます。SDK が低レベルの詳細を処理するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全な一覧は [GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使って Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportListObject.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportListObject.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportListObject.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportListObject.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportListObject.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportListObject.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportListObject.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportListObject.go" >}}
{{< /tab >}}

{{< /tabs >}}