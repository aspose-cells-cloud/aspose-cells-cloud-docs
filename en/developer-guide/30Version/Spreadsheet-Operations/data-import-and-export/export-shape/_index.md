---
title: "Export Shapes"
second_title: "Developer Guide"
linktitle: "Shape"
type: docs
url: /export-excel-shape-to-different-formats/
aliases: [/export/excel-shape-to-different-formats/]
keywords: "Export Shapes, Aspose.Cells Cloud, Excel shape export, Image formats, REST API, SDK"
description: "Export Excel shapes to PNG, GIF, JPEG, BMP, SVG, TIFF, EMF, and WMF using Aspose.Cells Cloud REST API and SDKs."
weight: 100
ArticleTitle: "Export Shapes – Aspose.Cells Cloud"
---
The **PostExport** API (`POST https://api.aspose.cloud/v3.0/cells/export`) enables exporting Excel internal elements—such as shapes, charts, or entire workbooks—to diverse formats like PDF, PNG, HTML, or CSV. Using Aspose.Cells Cloud, developers can programmatically convert specific sheet components without manual intervention, supporting 30+ output formats and including optional parameters for password protection, regional settings, and font customization. To use the API, upload the source Excel file via the required `File` form-data field and specify the target `objectType` (e.g., `shape`) and `format` in the query string.

You can export shapes to the following formats: **PNG**, **GIF**, **JPEG**, **BMP**, **SVG**, **TIFF**, **EMF**, **WMF**.

## The Post Export Web API

```http
POST https://api.aspose.cloud/v3.0/cells/export
```

### Security and Authentication

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| File | File | FormData | File to upload |
| objectType | String | Query | Exported object type:workbook/worksheet/chart/comment/picture/shape/listobject/oleobject. |
| format | String | Query | The conversion format(CSV/XLS/HTML/MHTML/ODS/PDF/XML/TXT/TIFF/XLSB/XLSM/XLSX/XLTM/XLTX/XPS/PNG/JPG/JPEG/GIF/EMF/BMP/MD[Markdown]/Numbers). |
| password | String | Query | The password needed to open an Excel file. |
| checkExcelRestriction | Boolean | Query | Whether check restriction of excel file when user modify cells related objects. |
| region | String | Query | The regional settings for workbook. |
| FontsLocation | String | Query | Use Custom fonts. |

### Response

```json
[
  {
    "Name": "FilesResult",
    "DataType": {
      "Identifier": "Class",
      "Reference": "FilesResult"
    }
  }
]
```

**Sample response headers**

```http
HTTP/1.1 200 OK
Content-Type: application/json
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

_Typical Base64‑encoded file payloads range from a few hundred bytes to several megabytes, depending on image dimensions and format._

### **Request Example**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=shape&format=tiff" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "Authorization: Bearer <your_access_token>" \
     -H "x-aspose-client: Containerize.Swagger" \
     -d '{"File":{}}'
```

## How to Use the Post Export API with SDKs?

### Post Export API Specification

The <a href="https://reference.aspose.cloud/cells/#/DataProcessing/PostExport" rel="noopener noreferrer">Post Export API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

You can use the **cURL** command‑line tool to access Aspose.Cells web services easily. The following example shows how to call the Cloud API using cURL.

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=shape&format=tiff" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "Authorization: Bearer <your_access_token>" \
     -H "x-aspose-client: Containerize.Swagger" \
     -d '{"File":{}}'
```

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExport.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExport.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExport.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExport.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExport.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExport.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExport.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExport.go" >}}
{{</tab>}}
{{< /tabs >}}
