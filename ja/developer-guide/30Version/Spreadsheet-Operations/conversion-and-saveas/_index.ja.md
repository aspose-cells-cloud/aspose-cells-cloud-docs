---
title: "Excel ファイルを別の形式に変換する、または別の方法で保存する"
second_title: "Document"
linktype: "Conversion and Save As"
type: docs
url: /ja/conversion-and-save-as/
aliases: [  /ja/convert-excel/ , /ja/convert/ ]
keywords: "Aspose.Cells, Excel 変換 API, Excel を PDF に変換, Excel を CSV に変換, Excel を JSON に変換, クラウド表計算変換"
description: "Aspose.Cells Cloud REST API を使用して、Excel ワークブックを PDF、CSV、JSON、HTML、およびその他の 15 種類以上の形式に変換する方法を学びます。エンドポイントの詳細、cURL コマンドのサンプル、Java、.NET、Python などの SDK スニペットが含まれています。"
weight: 30
ArticleTitle: "Aspose.Cells Cloud を使用して Excel ファイルを PDF、CSV、JSON などに変換する"
---

元々 [XLS](https://docs.fileformat.com/spreadsheet/xls/)、[XLSX](https://docs.fileformat.com/spreadsheet/xlsx/)、[XLSB](https://docs.fileformat.com/spreadsheet/xlsb/)、[CSV](https://docs.fileformat.com/spreadsheet/csv/) などの特定の形式で Excel ファイルを作成した場合、そのファイルを別の形式に変換して特殊な機能を活用したいと考えることがあります。たとえば、Excel ファイルを [PDF](https://docs.fileformat.com/pdf/) に変換すると、コンテンツが不正な変更から保護され、読み取りやすくなり、共有もしやすくなります。

**前提条件**  
変換 API を呼び出す前に、Aspose Cloud から OAuth 2.0 アクセストークンを取得し、ワークブックが Aspose Cloud ストレージに保存されていること（または PUT 変換エンドポイントのリクエスト本文に含まれていること）を確認してください。

ドキュメント変換は、非常に複雑なプロセスです。変換処理の複雑さに影響を与える多くの要因があり、変換の際にはそれらすべてを考慮する必要があります。Excel 形式間で正確でプロフェッショナルな品質の変換を提供することは、Aspose.Cells Cloud の主要な機能の一つです。

このサービスは、あらゆるドキュメント形式の変換にシームレスに機能します。以下の形式でドキュメントのインポートおよびエクスポートが可能です。

**サポートされている形式**  
- インポート／エクスポート: [XLS](https://docs.fileformat.com/spreadsheet/xls/)、[XLSX](https://docs.fileformat.com/spreadsheet/xlsx/)、[XLSB](https://docs.fileformat.com/spreadsheet/xlsb/)、[CSV](https://docs.fileformat.com/spreadsheet/csv/)、[TSV](https://docs.fileformat.com/spreadsheet/tsv/)、[XLSM](https://docs.fileformat.com/spreadsheet/xlsm/)、[ODS](https://docs.fileformat.com/spreadsheet/ods/)、[TXT](https://docs.fileformat.com/word-processing/txt/)
- エクスポートのみ: [PDF](https://docs.fileformat.com/pdf/)、[OTS](https://docs.fileformat.com/spreadsheet/ots/)、[XPS](https://docs.fileformat.com/page-description-language/xps/)、[DIF](https://docs.fileformat.com/spreadsheet/dif/)、[PNG](https://docs.fileformat.com/Image/png/)、[JPEG](https://docs.fileformat.com/image/jpeg/)、[BMP](https://docs.fileformat.com/image/bmp/)、[SVG](https://docs.fileformat.com/page-description-language/svg/)、[TIFF](https://docs.fileformat.com/image/tiff/)、[EMF](https://docs.fileformat.com/image/emf/)、[NUMBERS](https://docs.fileformat.com/spreadsheet/numbers/)、[FODS](https://docs.fileformat.com/spreadsheet/fods/)

### 変換 API

| API                         | 説明                                                                 |
| :-------------------------- | :------------------------------------------------------------------- |
| `GET /cells/{name}`         | クラウドストレージから Excel ワークブックを取得し、要求された形式に変換します。 |
| `PUT /cells/convert`        | リクエスト本文に含まれる Excel ワークブックを指定された出力形式に変換します。    |
| `POST /cells/{name}/saveAs` | 既存の Excel ワークブックを別の形式でクラウドストレージに直接保存します。         |

**API の詳細**

- **GET /cells/{name}**  
  - **パスパラメータ:** `name` – ワークブックのファイル名（必須）  
  - **クエリパラメータ:** `format` – 変換先の形式（例: pdf、csv、json）；`storage` – クラウドストレージ名（オプション）；`folder` – ストレージ内のフォルダーパス（オプション）  
  - **レスポンス:** 変換されたワークブックのファイルストリーム；`Content‑Type` は変換先の形式と一致します。  
  - **ステータスコード:** 200 OK、400 Bad Request、401 Unauthorized、404 Not Found、500 Internal Server Error  

- **PUT /cells/convert**  
  - **リクエスト本文:** 変換元ワークブックファイル（`file`）と、希望する出力形式を指定する必須フィールド `format` を含む multipart/form‑data  
  - **レスポンス:** 変換されたファイルのバイナリストリーム  
  - **ステータスコード:** 200 OK、400 Bad Request、401 Unauthorized、500 Internal Server Error  

- **POST /cells/{name}/saveAs**  
  - **パスパラメータ:** `name` – 既存のワークブック名  
  - **クエリパラメータ:** `format` – 変換先の形式；`outPath` – クラウドストレージ内の保存先パス（オプション）；`storage` – ストレージ名（オプション）  
  - **レスポンス:** 処理結果と保存されたファイルのパスを含む JSON オブジェクト。レスポンス例:  

    ```json
    {
      "status": "OK",
      "code": 200,
      "message": "File saved successfully.",
      "path": "Converted/MyWorkbook.pdf"
    }
    ```  

  - **ステータスコード:** 200 OK、400 Bad Request、401 Unauthorized、404 Not Found、500 Internal Server Error  

**PDF に変換するための cURL サンプル**

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx?format=pdf" \
  -H "Authorization: Bearer {access_token}" \
  -o MyWorkbook.pdf
```

**Java SDK スニペット（GET /cells/{name}）**

```java
CellsApi apiInstance = new CellsApi();
String name = "MyWorkbook.xlsx";
String format = "pdf";
File result = apiInstance.cellsGetWorkbook(name, format, null, null);
result.renameTo(new File("MyWorkbook.pdf"));
```

**.NET SDK スニペット（PUT /cells/convert）**

```csharp
var api = new CellsApi();
var file = File.ReadAllBytes("MyWorkbook.xlsx");
var format = "pdf";
var result = api.ConvertWorkbook(new MemoryStream(file), format);
File.WriteAllBytes("MyWorkbook.pdf", result);
```

**Python SDK スニペット（POST /cells/{name}/saveAs）**

```python
import asposecellscloud
api = asposecellscloud.CellsApi()
api.post_save_as(name="MyWorkbook.xlsx", format="pdf", out_path="Converted/MyWorkbook.pdf")
```

以下の記事では、各 API を詳しく説明し、追加の cURL および SDK の使用例を紹介しています。

- [Excel ファイルを別の形式に変換する](/ja/cells/convert-an-excel-file-to-different-formats)
- [Excel ファイルを別の形式で保存する](/ja/cells/save-an-excel-file-as-other-formats-files)
- [Excel ファイルを CSV ファイルに変換する](/ja/cells/convert-excel-file-to-csv-file)
- [Excel ファイルを DOCX ファイルに変換する](/ja/cells/convert-excel-file-to-docx-file)
- [Excel ファイルを HTML ファイルに変換する](/ja/cells/convert-excel-file-to-html-file)
- [Excel ファイルを JSON ファイルに変換する](/ja/cells/convert-excel-file-to-json-file)
- [Excel ファイルを Markdown ファイルに変換する](/ja/cells/convert-excel-file-to-markdown-file)
- [Excel ファイルを PDF ファイルに変換する](/ja/cells/convert-excel-file-to-pdf-file)
- [Excel ファイルを PNG ファイルに変換する](/ja/cells/convert-excel-file-to-png-file)
- [Excel ファイルを PPTX ファイルに変換する](/ja/cells/convert-excel-file-to-pptx-file)
- [Excel ファイルを SQL ファイルに変換する](/ja/cells/convert-excel-file-to-sql-file)
- [Excel ファイルを TIFF ファイルに変換する](/ja/cells/convert-excel-file-to-tiff-file)
---