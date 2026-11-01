---
title: "Advanced Convert Excel File – Aspose.Cells Cloud API Guide"
second_title: "Developer Guide"
linktitle: "Advanced Convert"
type: docs
url: /advanced-convert-excel/
date: 2024-06-15
keywords: "Aspose.Cells, Excel conversion, Cloud API, SDK, convert Excel to PDF, Excel to HTML, page setup Excel"
description: "Convert Excel to PDF, HTML, CSV via PUT /cells/convert with page setup, save options, and print settings control."
weight: 50
ArticleTitle: "Aspose.Cells Cloud Advanced Excel Conversion API – PDF, HTML, CSV with Page Setup & Save Options"
---
The **PutConvertWorkbook** API (`PUT https://api.aspose.cloud/v3.0/cells/convert`) enables developers to convert Excel workbooks into over 30 output formats—including PDF, HTML, CSV, PNG, and others—by uploading the source file and specifying the target format via query parameters, while supporting advanced options such as password protection, page layout control, and custom font handling.

## The Put Convert Workbook Web API

```http
PUT https://api.aspose.cloud/v3.0/cells/convert
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer" target="_blank">JWT token-based authentication</a>.

### **Request Parameters:**

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| File | File | FormData | File to upload |
| format | String | Query | The format to convert(CSV/XLS/HTML/MHTML/ODS/PDF/XML/TXT/TIFF/XLSB/XLSM/XLSX/XLTM/XLTX/XPS/PNG/JPG/JPEG/GIF/EMF/BMP/MD[Markdown]/Numbers). |
| password | String | Query | The password needed to open an Excel file. |
| outPath | String | Query | Path to save the result. If it's a single file, the `outPath` should encompass both the filename and extension. In the case of multiple files, the `outPath` should only include the folder. |
| storageName | String | Query | The storage name where the file is situated. |
| checkExcelRestriction | Boolean | Query | Whether check restriction of excel file when user modify cells related objects. |
| streamFormat | String | Query | The format of the input file stream. |
| region | String | Query | The regional settings for workbook. |
| pageWideFitOnPerSheet | Boolean | Query | The page wide fit on worksheet. |
| pageTallFitOnPerSheet | Boolean | Query | The page tall fit on worksheet. |
| sheetName | String | Query | Convert the specified worksheet. |
| pageIndex | Integer | Query | Convert the specified page  of worksheet, sheetName is required. |
| onePagePerSheet | Boolean | Query | When converting to PDF format, one page per sheet. |
| AutoRowsFit | Boolean | Query | Auto-fits all rows in this workbook. |
| AutoColumnsFit | Boolean | Query | Auto-fits the columns width in this workbook. |
| FontsLocation | String | Query | Use Custom fonts. |

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

**HTTP Status Codes**

| Code | Meaning | Description |
|---|---|---|
| 200 | OK | The request completed successfully. |
| 400 | Bad Request | The request is malformed or one or more parameters are invalid. |
| 401 | Unauthorized | Authentication failed, or the JWT token is missing or expired. |
| 404 | Not Found | The requested workbook, worksheet, or resource was not found. |
| 413 | Payload Too Large | The uploaded file exceeds the allowed size limit. |
| 500 | Internal Server Error | The server encountered an unexpected error while processing the request. |

The Advanced Convert operation enables you to transform an Excel workbook into various output formats (PDF, HTML, CSV, etc.) while giving you fine-grained control over page setup, save options, and print settings.

**Prerequisites / Authentication**  
To use this endpoint you must obtain an access token from Aspose.Cells Cloud and include it in the `Authorization` header as a Bearer token.

**API Reference**

- **Method:** `PUT`
- **Endpoint:** `/cells/convert`
- **Parameters:**
  - `format` (string, required) – Desired output format (e.g., `pdf`, `html`).
  - `outPath` (string, optional) – Path in cloud storage where the converted file will be saved.
  - `options` (object, optional) – JSON object containing advanced conversion options such as `pageSetup`, `saveOptions`, and `printSettings`.
- **Request Body Example:**
  ```json
  {
    "format": "pdf",
    "outPath": "output/converted.pdf",
    "options": {
      "pageSetup": {
        "orientation": "Landscape",
        "paperSize": "A4"
      },
      "saveOptions": {
        "compress": true
      },
      "printSettings": {
        "printHeadings": false
      }
    }
  }
  ```
- **Response:**
  - `200 OK` – Conversion succeeded; response contains the converted file stream or a reference to the saved file.
  - `400 Bad Request` – Invalid parameters or malformed request body.
  - `401 Unauthorized` – Authentication failed or token missing.
  - `500 Internal Server Error` – Server-side error during conversion.


**Notes**

- Some output formats have specific limitations (e.g., HTML conversion strips macros and ActiveX controls). Review the format-specific documentation for details.

### The ability to load spreadsheet files from multiple data sources

### Set Page Setup and Save Options

## Cloud SDK Family

Using an SDK helps accelerate development by handling low-level details, allowing you to focus on your project tasks. Please check out the <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutConvertWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutConvertWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutConvertWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutConvertWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutConvertWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutConvertWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutConvertWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutConvertWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}

<script type="application/ld+json">
{
  "@context":"https://schema.org",
  "@type":"WebAPI",
  "name":"Aspose.Cells Cloud Advanced Convert",
  "description":"Convert an Excel workbook to PDF/HTML/CSV with advanced options.",
  "url":"https://api.aspose.cloud/v3.0/cells/convert",
  "documentation":"https://docs.aspose.cloud/cells/advanced-convert-excel/",
  "endpointDescription":"PUT /cells/convert",
  "featureList": [
    "Convert Excel to PDF",
    "Convert Excel to HTML",
    "Convert Excel to CSV",
    "Set page setup (orientation, paper size)",
    "Configure save options (compression, image quality)",
    "Customize print settings (headings, gridlines)"
  ],
  "provider": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "input":{
    "@type":"PropertyValueSpecification",
    "valueRequired":true,
    "valueName":"format",
    "description":"Desired output format (pdf, html, csv, …)"
  },
  "target":{
    "@type":"EntryPoint",
    "urlTemplate":"https://api.aspose.cloud/v3.0/cells/convert?format={format}",
    "httpMethod":"PUT"
  }
}
</script>
