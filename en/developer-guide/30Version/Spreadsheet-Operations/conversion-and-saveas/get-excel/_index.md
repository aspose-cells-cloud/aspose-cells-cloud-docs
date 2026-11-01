---
title: "Aspose.Cells Cloud – Convert Excel Workbook to PDF, CSV, HTML, and More (GET /cells/{name})"
second_title: "Developer Guide"
linktitle: "Convert Excel"
type: docs
url: /get-different-formats-files/
aliases:
  - /export-excel-workbook-to-different-file-formats/
  - /export-different-formats/
keywords: "Aspose.Cells, Excel conversion, convert Excel, PDF, CSV, HTML, ODS, JSON, image formats, spreadsheet export, API, REST"
description: "Convert Excel files to PDF, CSV, HTML, images via Aspose.Cells Cloud API GET /cells/{name} with JWT and SDKs"
weight: 100
ArticleTitle: "Aspose.Cells Cloud – Convert Excel Workbook to PDF, CSV, HTML, and More (GET /cells/{name})"
---
The **GetWorkbook** API (`GET https://api.aspose.cloud/v3.0/cells/{name}`) retrieves an Excel workbook from Aspose.Cells Cloud in various output formats, supporting conversions to PDF, CSV, HTML, XLSX, PNG, JPG, and over 20 other formats via the optional `format` query parameter.

## The Get Workbook Web API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### **Query Parameters**

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| name | String | Path | The file name. |
| format | String | Query | The conversion format(CSV/XLS/HTML/MHTML/ODS/PDF/XML/TXT/TIFF/XLSB/XLSM/XLSX/XLTM/XLTX/XPS/PNG/JPG/JPEG/GIF/EMF/BMP/MD[Markdown]/Numbers). |
| password | String | Query | The password needed to open an Excel file. |
| isAutoFit | Boolean | Query | Specifies whether set workbook rows to be autofit. |
| onlySaveTable | Boolean | Query | Specifies whether only save table data.Only use pdf to excel. |
| folder | String | Query | The folder where the file is situated. |
| outPath | String | Query | Path to save the result. If it's a single file, the `outPath` should encompass both the filename and extension. In the case of multiple files, the `outPath` should only include the folder. |
| storageName | String | Query | The storage name where the file is situated. |
| outStorageName | String | Query | The storage name where the output file is situated. |
| checkExcelRestriction | Boolean | Query | Whether check restriction of excel file when user modify cells related objects. |
| region | String | Query | The regional settings for workbook. |
| pageWideFitOnPerSheet | Boolean | Query | The page wide fit on worksheet. |
| pageTallFitOnPerSheet | Boolean | Query | The page tall fit on worksheet. |
| onePagePerSheet | Boolean | Query | When converting to PDF format, one page per sheet. |
| onlyAutofitTable | Boolean | Query | - |
| FontsLocation | String | Query | Use Custom fonts. |

### Response

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
Content-Type: application/pdf
Content-Disposition: attachment; filename="book1.pdf"
Content-Length: 123456

(binary PDF data)
```

**HTTP Status Codes**

| Code | Meaning | Description |
|---|---|---|
| 200 | OK | The request completed successfully. |
| 400 | Bad Request | The request is malformed or one or more parameters are invalid. |
| 401 | Unauthorized | Authentication failed, or the JWT token is missing or expired. |
| 404 | Not Found | The requested workbook, worksheet, or resource was not found. |
| 500 | Internal Server Error | The server encountered an unexpected error while processing the request. |

**Success (200)**

- The API returns a **[Workbook](/cells/workbook/)** object that contains workbook structure info when the `format` query parameter is omitted.

- The API returns the converted file in the requested format when the `format` query parameter specifies a file type.



> **Notes:**
>
> - Large workbooks may take longer to convert; consider increasing the request timeout.
> - Some formats (e.g., `ODS`) are not supported for certain Excel features such as macros.

## How to Use the GetWorkBook API with SDKs

> **Prerequisites:**
>
> - A valid **JWT access token** obtained via the Aspose.Cells authentication flow.
> - The source workbook must be stored in a supported Aspose storage or supplied directly in the request.
> - Ensure the API version (`v3.0`) matches the latest released version.

### GetWorkBook API Specification

The <a href="https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook" rel="noopener noreferrer">OpenAPI Specification</a> defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

### Example Request

You can use the **cURL** command‑line tool to access Aspose.Cells web services. The following example shows a correct GET request with the required authorization header.

{{< tabs tabTotal="1" tabID="11" tabName11="Request" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/book1.xlsx?format=pdf" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: Containerize.Swagger"
```

{{< /tab >}}

{{< /tabs >}}

### Use Aspose.Cells Cloud SDKs

Using an SDK is the fastest way to develop. An SDK abstracts low‑level details so you can focus on your project tasks. Please check the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}

**See Also**

- <a href="https://apireference.aspose.cloud/cells/#/Workbook/ConvertWorkbook" rel="noopener noreferrer">Convert Workbook (POST)</a>
- <a href="https://apireference.aspose.cloud/cells/#/Workbook/SaveAs" rel="noopener noreferrer">Save As (GET)</a>

---

_Last Updated: 2024-12-01_

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Aspose.Cells Cloud – Convert Excel Workbook to PDF, CSV, HTML, and More (GET /cells/{name})",
  "description": "Documentation for the Aspose.Cells Cloud GET /cells/{name} endpoint that converts Excel workbooks to various formats such as PDF, CSV, HTML, and more.",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "datePublished": "2024-12-01",
  "keywords": "Aspose.Cells, Excel conversion, PDF, CSV, HTML, API, REST, cloud",
  "url": "https://docs.aspose.cloud/cells/get-different-formats-files/",
  "publisher": {
    "@type": "Organization",
    "name": "Aspose"
  }
}
</script>
