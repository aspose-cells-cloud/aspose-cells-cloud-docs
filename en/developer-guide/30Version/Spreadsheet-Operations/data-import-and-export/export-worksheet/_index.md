---
title: "Export Worksheet – Aspose.Cells Cloud"
second_title: "Document"
linktitle: "Worksheet"
type: docs
url: /export-excel-worksheet-to-different-formats/
aliases: [ /export/excel-worksheet-to-different-formats/]
keywords: "Aspose.Cells Cloud, export worksheet, REST API, PDF, CSV, TIFF, XLSX, ODS, image formats"
description: "Learn how to export an Excel worksheet to PDF, CSV, TIFF, and other formats using the Aspose.Cells Cloud REST API. Includes cURL example, required authentication, parameter details, and response handling."
weight: 20
---

You can export a worksheet to the following formats:

- **XLS** – [Link](https://docs.fileformat.com/spreadsheet/xls/)
- **XLSX** – [Link](https://docs.fileformat.com/spreadsheet/xlsx/)
- **XLSB** – [Link](https://docs.fileformat.com/spreadsheet/xlsb/)
- **CSV** – [Link](https://docs.fileformat.com/spreadsheet/csv/)
- **TSV** – [Link](https://docs.fileformat.com/spreadsheet/tsv/)
- **XLSM** – [Link](https://docs.fileformat.com/spreadsheet/xlsm/)
- **ODS** – [Link](https://docs.fileformat.com/spreadsheet/ods/)
- **TXT** – [Link](https://docs.fileformat.com/word-processing/txt/)
- **PDF** – [Link](https://docs.fileformat.com/pdf/)
- **OTS** – [Link](https://docs.fileformat.com/spreadsheet/ots/)
- **XPS** – [Link](https://docs.fileformat.com/page-description-language/xps/)
- **DIF** – [Link](https://docs.fileformat.com/spreadsheet/dif/)
- **PNG** – [Link](https://docs.fileformat.com/Image/png/)
- **JPEG** – [Link](https://docs.fileformat.com/image/jpeg/)
- **BMP** – [Link](https://docs.fileformat.com/image/bmp/)
- **SVG** – [Link](https://docs.fileformat.com/page-description-language/svg/)
- **TIFF** – [Link](https://docs.fileformat.com/image/tiff/)
- **EMF** – [Link](https://docs.fileformat.com/image/emf/)
- **NUMBERS** – [Link](https://docs.fileformat.com/spreadsheet/numbers/)
- **FODS** – [Link](https://docs.fileformat.com/spreadsheet/fods/)

### REST API

| **API** | **Type** | **Description** | **Swagger Link** |
| ------- | -------- | --------------- | ---------------- |
| /cells/export | POST | Export an Excel worksheet from the request body to a specified format | [PostExport](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

**Authentication**  
The Aspose.Cells Cloud API uses OAuth 2.0. Obtain an access token from the `/connect/token` endpoint and include it in the request header as `Authorization: Bearer <access_token>`.

**Parameters**  
- `objectType` – The type of Excel object to export (e.g., `worksheet`).  
- `format` – The desired output format (e.g., `tiff`). Both parameters are required and are passed as query strings.

You can use the **cURL** command‑line tool to access Aspose.Cells web services easily. The following example shows how to call the Cloud API with cURL.

#### Request

```bash
# Export a worksheet to TIFF format
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=worksheet&format=tiff" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: Containerize.Swagger" \
     -F "File=@MyWorkbook.xlsx"
```

#### Response

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

**Error handling**  
If the request fails, the API returns a JSON error object containing fields such as `Code` and `Message`. Typical HTTP status codes include **401 Unauthorized** (missing or invalid token) and **400 Bad Request** (invalid parameters).

### Cloud SDK Family

Using an SDK is the fastest way to develop against Aspose.Cells Cloud. An SDK abstracts low‑level details, allowing you to focus on your business logic. For a complete list of supported SDKs, please visit the [GitHub repository](https://github.com/aspose-cells-cloud).

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

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