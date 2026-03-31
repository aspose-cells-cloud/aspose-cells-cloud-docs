---  
title: "Export a Worksheet with Aspose.Cells Cloud API – Formats, cURL & SDK Samples"  
second_title: "Document"  
linktitle: "Worksheet Export"  
type: docs  
url: /worksheets/get-worksheet/  
keywords: "Aspose.Cells Cloud Get Worksheet, worksheet export, Excel API, REST, CSV, PDF, PNG, JPEG, GIF, BMP, TIFF, EMF, XPS, OTS, XLS, XLSX, XLSB, XLSM, ODS, FODS, Numbers, cloud API"  
description: "Learn how to export a single worksheet from an Excel file using Aspose.Cells Cloud REST API. Includes endpoint, parameters, a corrected cURL example, authentication details, error handling, and SDK snippets for C#, Java, Python, and more."  
weight: 10  
---  

This REST API allows you to **export a worksheet** from an Excel file to many different file formats.

**Summary** – Use the **Get Worksheet** endpoint to download a single worksheet from a workbook in the format of your choice.

You can export to the following formats:

| Format | Extension | MIME Type |
|--------|-----------|-----------|
| XLS | .xls | application/vnd.ms-excel |
| XLSX | .xlsx | application/vnd.openxmlformats-officedocument.spreadsheetml.sheet |
| XLSB | .xlsb | application/vnd.ms-excel.sheet.binary.macroEnabled.12 |
| CSV | .csv | text/csv |
| TSV | .tsv | text/tab-separated-values |
| XLSM | .xlsm | application/vnd.ms-excel.sheet.macroEnabled.12 |
| ODS | .ods | application/vnd.oasis.opendocument.spreadsheet |
| TXT | .txt | text/plain |
| PDF | .pdf | application/pdf |
| OTS | .ots | application/vnd.oasis.opendocument.spreadsheet-template |
| XPS | .xps | application/vnd.ms-xpsdocument |
| DIF | .dif | application/x-dif |
| PNG | .png | image/png |
| JPEG | .jpeg | image/jpeg |
| GIF | .gif | image/gif |
| BMP | .bmp | image/bmp |
| WMF | .wmf | image/wmf |
| TIFF | .tiff | image/tiff |
| EMF | .emf | image/emf |
| NUMBERS | .numbers | application/vnd.apple.numbers |
| FODS | .fods | application/vnd.oasis.opendocument.spreadsheet-flat-xml |

## Authentication  

The API uses **OAuth 2.0 Bearer tokens**. Obtain a JWT token from the `/connect/token` endpoint and include it in the request header:

```http
Authorization: Bearer <your_jwt_token>
```

Tokens are valid for a limited period (default 20 minutes). Refresh the token before it expires.

## REST API  

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}
```

The request parameters are:

| Parameter Name        | Type    | Location | Description                                                                 |
|-----------------------|---------|----------|-----------------------------------------------------------------------------|
| **name**              | string  | path     | **Required.** Name of the Excel file.                                       |
| **sheetName**         | string  | path     | **Required.** Name of the worksheet to export.                              |
| **format**            | string  | query    | Target file format for the exported worksheet (e.g., `pdf`, `png`).        |
| **verticalResolution**| integer | query    | Image DPI for formats that support resolution (e.g., PNG, JPEG).           |
| **horizontalResolution**| integer| query  | Image DPI for formats that support resolution.                              |
| **area**              | string  | query    | Cell range to export (e.g., `A1:D10`).                                      |
| **pageIndex**         | integer | query    | Index of the page to export when the worksheet is paginated.               |
| **folder**            | string  | query    | Folder path in storage where the source file is located.                    |
| **storageName**       | string  | query    | Name of the Aspose Cloud storage.                                           |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheet) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to call the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

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

```json
{
  "stream"
}
```

{{< /tab >}}

{{< /tabs >}}

## Error Handling  

The API returns standard HTTP status codes. Common responses include:

| Status Code | Meaning                              | Example JSON Body |
|-------------|--------------------------------------|-------------------|
| **200**     | Success – the worksheet stream is returned. | `{ "stream": "..." }` |
| **400**     | Bad request – missing or invalid parameters. | `{ "error": "Invalid format parameter." }` |
| **401**     | Unauthorized – invalid or missing JWT token. | `{ "error": "Authentication failed." }` |
| **404**     | Not found – the specified file or worksheet does not exist. | `{ "error": "Worksheet not found." }` |
| **500**     | Internal server error – unexpected condition on the server. | `{ "error": "Unexpected error." }` |

Handle these responses in your client code to provide appropriate feedback to users.

## Cloud SDK Family  

Using an SDK is the best way to speed up development. An SDK takes care of low‑level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

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

---  

### Frequently Asked Questions  

<details>  
<summary>How do I export a specific worksheet to PDF using Aspose.Cells Cloud?</summary>  
Send a **GET** request to  

```
https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}?format=pdf
```  

including a valid **Bearer** token. Optional `folder` and `storageName` parameters can be added if the file resides outside the root folder.  
</details>  

<details>  
<summary>What authentication method is required for the Get Worksheet API?</summary>  
The API uses **OAuth 2.0**. Obtain a JWT via the `/connect/token` endpoint and pass it in the `Authorization: Bearer <token>` header for every request.  
</details>  

<details>  
<summary>Which query parameters control image resolution when exporting a worksheet as PNG?</summary>  
Use `horizontalResolution` and `verticalResolution` (integer DPI values). Example:  

```
.../worksheets/Sheet1?format=png&horizontalResolution=300&verticalResolution=300
```  
</details>  