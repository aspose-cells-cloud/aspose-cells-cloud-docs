---
title: "Convert an Excel File to Different Formats"
ArticleTitle: "Convert an Excel File to Different Formats"
second_title: "Developer Guide"
linktitle: "Convert Excel"
type: docs
url: /convert-an-excel-file-to-different-formats/
aliases:
  [
    /convert-excel-workbook-to-different-file-formats/,
    /convert/excel-to-different-formats/,
  ]
keywords: "Aspose.Cells Cloud, Excel conversion, file format conversion, REST API, SDK, CSV, PDF, HTML, JSON, Markdown"
description: "Convert Excel to CSV, PDF, HTML, JSON, Markdown via Aspose.Cells Cloud PutConvertWorkBook API"
weight: 100
---
The **PutConvertWorkbook** API (`PUT https://api.aspose.cloud/v3.0/cells/convert`) enables conversion of Excel workbooks to 30+ formats—including PDF, CSV, HTML, PNG, and others—by uploading the source file in the request body and specifying the target format via the `format` query parameter, with optional support for password-protected files and custom output paths.

This REST API converts an Excel file to various output formats.

## The Put Convert Workbook Web API

```http
PUT https://api.aspose.cloud/v3.0/cells/convert
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Query Parameters

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

The request is an HTTP **PUT** with multipart content (see [RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) or [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)).  
The first part of the multipart body contains the **data file**, and the second part contains the **save options**.

### Request Body Parameters

| Parameter Name | Type      | Description                                                    |
| -------------- | --------- | -------------------------------------------------------------- |
| `datafile`     | data file | The Excel file placed in the first part of the multipart body. |
| `SaveOptions`  | object    | Save options placed in the second part of the multipart body.  |

## How to Use the PutConvertWorkBook API with SDKs

### PutConvertWorkBook API Specification

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) defines a publicly accessible interface that enables direct REST interactions from a web browser.

### cURL Example

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/convert?format=html" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: Containerize.Swagger" \
     -d '{"File":{}}'
```

### Use Aspose.Cells Cloud SDKs

Using an SDK accelerates development by handling low‑level details, allowing you to focus on business logic. See the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services with various SDKs:

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
