---
title: "Export a Worksheet with Aspose.Cells Cloud API – Formats, cURL & SDK Samples"
second_title: "Developer Guide"
linktitle: "Worksheet Export"
type: docs
url: /worksheets/get-worksheet/
keywords: "Aspose.Cells Cloud Get Worksheet, worksheet export, Excel API, REST, CSV, PDF, PNG, JPEG, GIF, BMP, TIFF, EMF, XPS, OTS, XLS, XLSX, XLSB, XLSM, ODS, FODS, Numbers, cloud API"
description: "Retrieve a worksheet from an Excel file using Aspose.Cells Cloud REST API with cURL or SDKs"
weight: 100
ArticleTitle: "Export a Worksheet with Aspose.Cells Cloud API – Formats, cURL & SDK Samples"
---
The **GetWorksheetWithFormat** API (`GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}`) enables developers to retrieve a specific worksheet from an Excel workbook and export it directly in a requested format—such as PDF, PNG, HTML, or CSV—by specifying the workbook file name and worksheet name as path parameters, with optional query parameters to control resolution, print area, and output settings.

**Summary** – Use the **Get Worksheet** endpoint to download a single worksheet from a workbook in the format of your choice.

You can export to the following formats:

| Format  | Extension | MIME Type                                                         |
| ------- | --------- | ----------------------------------------------------------------- |
| XLS     | .xls      | application/vnd.ms-excel                                          |
| XLSX    | .xlsx     | application/vnd.openxmlformats-officedocument.spreadsheetml.sheet |
| XLSB    | .xlsb     | application/vnd.ms-excel.sheet.binary.macroEnabled.12             |
| CSV     | .csv      | text/csv                                                          |
| TSV     | .tsv      | text/tab-separated-values                                         |
| XLSM    | .xlsm     | application/vnd.ms-excel.sheet.macroEnabled.12                    |
| ODS     | .ods      | application/vnd.oasis.opendocument.spreadsheet                    |
| TXT     | .txt      | text/plain                                                        |
| PDF     | .pdf      | application/pdf                                                   |
| OTS     | .ots      | application/vnd.oasis.opendocument.spreadsheet-template           |
| XPS     | .xps      | application/vnd.ms-xpsdocument                                    |
| DIF     | .dif      | application/x-dif                                                 |
| PNG     | .png      | image/png                                                         |
| JPEG    | .jpeg     | image/jpeg                                                        |
| GIF     | .gif      | image/gif                                                         |
| BMP     | .bmp      | image/bmp                                                         |
| WMF     | .wmf      | image/wmf                                                         |
| TIFF    | .tiff     | image/tiff                                                        |
| EMF     | .emf      | image/emf                                                         |
| NUMBERS | .numbers  | application/vnd.apple.numbers                                     |
| FODS    | .fods     | application/vnd.oasis.opendocument.spreadsheet-flat-xml           |

## Security and Authentication

The Aspose.Cells Cloud APIs are secure and require [JWT token-based authentication](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## The Get Worksheet with Format Web API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer" target="_blank">JWT token-based authentication</a>.

### **Request parameters**

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| name | String | Path | The file name. |
| sheetName | String | Path | The worksheet name. |
| format | String | Query | Export format(CSV/XLS/HTML/MHTML/ODS/PDF/XML/TXT/TIFF/XLSB/XLSM/XLSX/XLTM/XLTX/XPS/PNG/JPG/JPEG/GIF/EMF/BMP/MD[Markdown]/Numbers). |
| verticalResolution | Integer | Query | Image vertical resolution. |
| horizontalResolution | Integer | Query | Image horizontal resolution. |
| area | String | Query | Represents the range to be printed. |
| pageIndex | Integer | Query | Represents the page to be printed |
| onePagePerSheet | Boolean | Query | - |
| printHeadings | Boolean | Query | - |
| folder | String | Query | The folder where the file is situated. |
| storageName | String | Query | The storage name where the file is situated. |

The <a href="https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheet" target="_blank" rel="noopener noreferrer">OpenAPI Specification</a> defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

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

```http
HTTP/1.1 200 OK
Content-Type: image/gif
Content-Disposition: attachment; filename="Sheet1.gif"

<binary data>
```

{{< /tab >}}

{{< /tabs >}}

### **Response**

```json
[
  {
    "Name": "Stream",
    "DataType": {
      "Identifier": "File"
    }
  }
]
```

**Sample response headers**

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="result"
```

### Error Handling

The API returns standard HTTP status codes. Common responses include:

| Status Code | Meaning                                                     | Example JSON Body                          |
| ----------- | ----------------------------------------------------------- | ------------------------------------------ |
| **200**     | Success – the worksheet stream is returned.                 | `{ "stream": "..." }`                      |
| **400**     | Bad request – missing or invalid parameters.                | `{ "error": "Invalid format parameter." }` |
| **401**     | Unauthorized – invalid or missing JWT token.                | `{ "error": "Authentication failed." }`    |
| **404**     | Not found – the specified file or worksheet does not exist. | `{ "error": "Worksheet not found." }`      |
| **500**     | Internal server error – unexpected condition on the server. | `{ "error": "Unexpected error." }`         |

Handle these responses in your client code to provide appropriate feedback to users.

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK takes care of low‑level details and lets you focus on your project tasks. Please check out the <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

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
