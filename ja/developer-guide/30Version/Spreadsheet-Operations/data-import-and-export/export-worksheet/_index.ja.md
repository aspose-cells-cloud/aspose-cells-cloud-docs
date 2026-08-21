---
title: "ワークシートのエクスポート – Aspose.Cells Cloud"
second_title: "ドキュメント"
linktitle: "ワークシート"
type: docs
url: /export-excel-worksheet-to-different-formats/
aliases: [/export/excel-worksheet-to-different-formats/]
keywords: "Aspose.Cells, ワークシートのエクスポート, Excel API, PDF, CSV, TIFF, ODS, 画像形式"
description: "Aspose.Cells Cloud REST API を使用して、Excel ワークシートを PDF、CSV、TIFF などの形式にエクスポートする方法を学びます。cURL の使用例、必要な認証、パラメータの詳細、応答処理を含みます。"
weight: 20
ArticleTitle: "Excel ワークシートをさまざまな形式にエクスポート – Aspose.Cells Cloud"
---

以下の形式にワークシートをエクスポートできます：

- **XLS** – [XLS 形式の詳細](https://docs.fileformat.com/spreadsheet/xls/)
- **XLSX** – [XLSX 形式の詳細](https://docs.fileformat.com/spreadsheet/xlsx/)
- **XLSB** – [XLSB 形式の詳細](https://docs.fileformat.com/spreadsheet/xlsb/)
- **CSV** – [CSV 形式の詳細](https://docs.fileformat.com/spreadsheet/csv/)
- **TSV** – [TSV 形式の詳細](https://docs.fileformat.com/spreadsheet/tsv/)
- **XLSM** – [XLSM 形式の詳細](https://docs.fileformat.com/spreadsheet/xlsm/)
- **ODS** – [ODS 形式の詳細](https://docs.fileformat.com/spreadsheet/ods/)
- **TXT** – [TXT 形式の詳細](https://docs.fileformat.com/word-processing/txt/)
- **PDF** – [PDF 形式の詳細](https://docs.fileformat.com/pdf/)
- **OTS** – [OTS 形式の詳細](https://docs.fileformat.com/spreadsheet/ots/)
- **XPS** – [XPS 形式の詳細](https://docs.fileformat.com/page-description-language/xps/)
- **DIF** – [DIF 形式の詳細](https://docs.fileformat.com/spreadsheet/dif/)
- **PNG** – [PNG 形式の詳細](https://docs.fileformat.com/Image/png/)
- **JPEG** – [JPEG 形式の詳細](https://docs.fileformat.com/image/jpeg/)
- **BMP** – [BMP 形式の詳細](https://docs.fileformat.com/image/bmp/)
- **SVG** – [SVG 形式の詳細](https://docs.fileformat.com/page-description-language/svg/)
- **TIFF** – [TIFF 形式の詳細](https://docs.fileformat.com/image/tiff/)
- **EMF** – [EMF 形式の詳細](https://docs.fileformat.com/image/emf/)
- **NUMBERS** – [Numbers 形式の詳細](https://docs.fileformat.com/spreadsheet/numbers/)
- **FODS** – [FODS 形式の詳細](https://docs.fileformat.com/spreadsheet/fods/)

[ワークブック全体やチャートのエクスポートなど、関連するエクスポート操作を確認する。](https://docs.aspose.cloud/cells/export-excel-workbook-to-different-formats/)

## PostExport API

```http
POST https://api.aspose.cloud/v3.0/cells/export
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメータ

| パラメータ名 | 型     | パス／クエリ文字列／HTTP ボディ | 必須 | 説明 |
|-------------|--------|--------------------------------|------|------|
| file        | file   | formData                       | True | アップロードするファイル |
| objectType  | string | query                          | True | エクスポートするオブジェクトの種類。チャートをエクスポートする場合は `chart` を指定します。その他の指定可能な値には `worksheet`、`picture` などがあります。 |
| format      | string | query                          | True | 出力形式の指定。サポートされる値: `png`, `jpeg`, `gif`, `bmp`, `svg`, `tiff`, `emf`, `wmf`, `pdf` |

### 応答

```json
{
  "Files": [
    {
      "Filename": "Book1_xlsx_Sheet1.tif",
      "FileSize": 390,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet2.tif",
      "FileSize": 10040,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet3.tif",
      "FileSize": 2824,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet4.tif",
      "FileSize": 1350,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet5.tif",
      "FileSize": 12978,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet6.tif",
      "FileSize": 7002,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet7.tif",
      "FileSize": 11532,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet1.tif",
      "FileSize": 382,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet2.tif",
      "FileSize": 382,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet3.tif",
      "FileSize": 130084,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet4.tif",
      "FileSize": 120062,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

### **エラー処理**

リクエストが失敗した場合、API は `Code` や `Message` などのフィールドを含む JSON エラーオブジェクトを返します。典型的な HTTP ステータスコードには、**401 Unauthorized**（トークンが欠落している、または無効）および **400 Bad Request**（無効なパラメータ）があります。

**HTTP ステータスコード**

| コード | 意味             | 説明 |
|-------|------------------|------|
| 200   | OK               | フィルターが正常に適用され、応答に操作の詳細が含まれます。 |
| 400   | Bad Request      | パラメータが欠落または無効（例：サポートされていないファイル形式） |
| 401   | Unauthorized     | JWT トークンが無効または欠落しています。 |
| 413   | Payload Too Large| アップロードされたファイルがサイズ制限を超えています。 |
| 500   | Internal Server Error | 予期しないサーバーエラーが発生しました。 |

**注意事項**

- アップロード可能なファイルの最大サイズは 50 MB です。  
- API は単一のリクエストで複数のワークシートをエクスポートできます。各ワークシートは `Files` 配列内に個別のファイルとして返されます。  
- 大きなワークブックに対しては非同期処理が利用可能です。`202 Accepted` 応答を使用して操作のステータスをポーリングします。

## SDK を使用した PostExport API の利用方法

### 前提条件

API を呼び出す前に、Aspose.Cells Cloud の認証フローを使用して有効な JWT アクセストークンを取得し、各リクエストの `Authorization` ヘッダーにトークンを含めてください。SDK は、クライアント認証情報を設定すると、トークンの取得を自動的に処理します。

### PostExport API 仕様

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) はパブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST 操作を実行できるようにします。

**cURL** コマンドラインツールを使用して、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例は、cURL を使用してクラウド API を呼び出す方法を示しています。

```bash
# ワークシートを TIFF 形式にエクスポート
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=worksheet&format=tiff" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: Containerize.Swagger" \
     -F "File=@MyWorkbook.xlsx"
```

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、Aspose.Cells Cloud に対する開発が最も迅速に行えます。SDK は低レベルの詳細を抽象化し、ビジネスロジックの開発に集中できるようにします。サポートされている SDK の完全な一覧については、[GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご覧ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportWorksheet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportWorksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportWorksheet.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportWorksheet.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportWorksheet.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportWorksheet.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportWorksheet.go" >}}

{{< /tab >}}

{{< /tabs >}}