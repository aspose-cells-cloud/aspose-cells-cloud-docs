---
title: "Convert an Excel file to another format or save it differently."
second_title: "Document"
linktitle: "Conversion and Save As"
type: docs
url: /conversion-and-save-as/
aliases: [/convert-excel/, /convert/]
keywords: "Aspose.Cells, Excel conversion API, convert Excel to PDF, Excel to CSV, Excel to JSON, cloud spreadsheet conversion"
description: "Learn how to convert Excel workbooks to PDF, CSV, JSON, HTML, and over 15 other formats using Aspose.Cells Cloud REST API. Includes endpoint details, sample cURL commands, and SDK snippets for Java, .NET, Python, and more."
weight: 30
ArticleTitle: "Convert Excel Files to PDF, CSV, JSON and More with Aspose.Cells Cloud"
---

If you originally created an Excel file in a certain format—such as [XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), or [CSV](https://docs.fileformat.com/spreadsheet/csv/)—you may find it useful to convert the Excel file to another format to take advantage of special features. For example, converting an Excel file to [PDF](https://docs.fileformat.com/pdf/) protects its contents from unauthorized modifications and makes it easy to read and share.

Document conversion is a complex process. Many factors contribute to the conversion process’s complexity and should be considered during transformation. Providing precise, professional‑quality conversion between Excel formats is a key feature of Aspose.Cells Cloud.

The service works seamlessly for any document format conversion. You can both import and export documents in these formats:

- Import/Export: [XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV](https://docs.fileformat.com/spreadsheet/csv/), [TSV](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [ODS](https://docs.fileformat.com/spreadsheet/ods/), [TXT](https://docs.fileformat.com/word-processing/txt/)
- Export‑only: [PDF](https://docs.fileformat.com/pdf/), [OTS](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [DIF](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [NUMBERS](https://docs.fileformat.com/spreadsheet/numbers/), [FODS](https://docs.fileformat.com/spreadsheet/fods/)

### Conversion APIs

| API                         | Description                                                                             |
| :-------------------------- | :-------------------------------------------------------------------------------------- |
| `GET /cells/{name}`         | Retrieves an Excel workbook from cloud storage and converts it to the requested format. |
| `PUT /cells/convert`        | Converts an Excel workbook supplied in the request body to the specified output format. |
| `POST /cells/{name}/saveAs` | Saves an existing Excel workbook as another format directly to cloud storage.           |

**API details**

- **GET /cells/{name}**  
  - **Path parameters:** `name` – workbook file name (required).  
  - **Query parameters:** `format` – target format (e.g., pdf, csv, json); `storage` – cloud storage name (optional); `folder` – folder path within storage (optional).  
  - **Response:** File stream of the converted workbook; `Content‑Type` matches the target format.  
  - **Status codes:** 200 OK, 400 Bad Request, 401 Unauthorized, 404 Not Found, 500 Internal Server Error.  

- **PUT /cells/convert**  
  - **Request body:** multipart/form‑data containing the source workbook file (`file`) and a required `format` field indicating the desired output.  
  - **Response:** Binary stream of the converted file.  
  - **Status codes:** 200 OK, 400 Bad Request, 401 Unauthorized, 500 Internal Server Error.  

- **POST /cells/{name}/saveAs**  
  - **Path parameters:** `name` – existing workbook name.  
  - **Query parameters:** `format` – target format; `outPath` – destination path in cloud storage (optional); `storage` – storage name (optional).  
  - **Response:** JSON object with operation result and the path of the saved file.  
  - **Status codes:** 200 OK, 400 Bad Request, 401 Unauthorized, 404 Not Found, 500 Internal Server Error.  

**Sample cURL for converting to PDF**

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx?format=pdf" \
  -H "Authorization: Bearer {access_token}" \
  -o MyWorkbook.pdf
```

**Java SDK snippet (GET /cells/{name})**

```java
CellsApi apiInstance = new CellsApi();
String name = "MyWorkbook.xlsx";
String format = "pdf";
File result = apiInstance.cellsGetWorkbook(name, format, null, null);
result.renameTo(new File("MyWorkbook.pdf"));
```

**.NET SDK snippet (PUT /cells/convert)**

```csharp
var api = new CellsApi();
var file = File.ReadAllBytes("MyWorkbook.xlsx");
var format = "pdf";
var result = api.ConvertWorkbook(new MemoryStream(file), format);
File.WriteAllBytes("MyWorkbook.pdf", result);
```

**Python SDK snippet (POST /cells/{name}/saveAs)**

```python
import asposecellscloud
api = asposecellscloud.CellsApi()
api.post_save_as(name="MyWorkbook.xlsx", format="pdf", out_path="Converted/MyWorkbook.pdf")
```

The following articles explain each API in detail and include additional cURL and SDK examples:

- [Convert an Excel file to a different format](/cells/convert-an-excel-file-to-different-formats)
- [Save an Excel file as a different format](/cells/save-an-excel-file-as-other-formats-files)
- [Convert an Excel file to a CSV file](/cells/convert-excel-file-to-csv-file)
- [Convert an Excel file to a DOCX file](/cells/convert-excel-file-to-docx-file)
- [Convert an Excel file to an HTML file](/cells/convert-excel-file-to-html-file)
- [Convert an Excel file to a JSON file](/cells/convert-excel-file-to-json-file)
- [Convert an Excel file to a Markdown file](/cells/convert-excel-file-to-markdown-file)
- [Convert an Excel file to a PDF file](/cells/convert-excel-file-to-pdf-file)
- [Convert an Excel file to a PNG file](/cells/convert-excel-file-to-png-file)
- [Convert an Excel file to a PPTX file](/cells/convert-excel-file-to-pptx-file)
- [Convert an Excel file to a SQL file](/cells/convert-excel-file-to-sql-file)
- [Convert an Excel file to a TIFF file](/cells/convert-excel-file-to-tiff-file)