---
title: "Convert Worksheet to PDF, PNG, JPEG, SVG, TIFF & More – Aspose.Cells Cloud API"
description: "Convert Excel worksheet to image or text formats using Aspose.Cells Cloud REST API with cURL and SDK examples"
keywords: "worksheet conversion, Excel to image, Aspose.Cells Cloud API, convert worksheet to PNG, Excel to PDF, REST API export, SDK examples"
date: 2024-06-15
type: docs
url: /convert-worksheet/
aliases:
  - /cells/convert-worksheet-to-image/
  - /worksheets/conversion/
weight: 130
linktitle: "Convert Worksheet to Image"
ArticleTitle: "Convert Excel Worksheet to PDF, PNG, JPEG, SVG & More with Aspose.Cells Cloud API"
---

The **GetWorksheetWithFormat** API (`GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}`) enables developers to extract and convert a specific worksheet from an Excel workbook (such as XLSX, XLS, CSV, etc.) into over 15 formats—including high-fidelity images like PNG, JPEG, SVG, and TIFF—by specifying the desired output format via the `format` query parameter.

## Overview

Aspose.Cells Cloud’s `GetWorksheetWithFormat` API enables you to convert a single worksheet from an Excel workbook (XLS, XLSX, XLSB, CSV, etc.) into over 15 output formats — including high-fidelity images (PNG, JPEG, SVG, TIFF, BMP, EMF), PDF, and document formats (CSV, TXT, XPS, OTS, NUMBERS, FODS).

This API is ideal for:

- Generating report snapshots (e.g., dashboards → PNG for web embedding)
- Archiving specific sheets as PDF for compliance
- Converting financial data to CSV for downstream processing
- Exporting charts or tables as scalable vector graphics (SVG) for responsive UIs

---

## Supported Formats

| Category           | Formats                                                                     |
| ------------------ | --------------------------------------------------------------------------- |
| **Input (Read)**   | XLS, XLSX, XLSB, CSV, TSV, XLSM, ODS, TXT                                   |
| **Output (Write)** | PDF, OTS, XPS, DIF, PNG, JPEG, BMP, SVG, TIFF, EMF, NUMBERS, FODS, CSV, TXT |

> 💡 **Note**:
>
> - For image formats (PNG, JPEG, SVG, etc.), resolution can be controlled via `verticalResolution`/`horizontalResolution`.
> - SVG is an _image_ format (vector), **not** a page description language.

---

## The Get Worksheet with Format Web API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}
```

### Security and Authentication

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer" target="_blank">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name       | Type    | Path/Query String/HTTPBody | Description                                                                                                                        |
| -------------------- | ------- | -------------------------- | ---------------------------------------------------------------------------------------------------------------------------------- |
| name                 | String  | Path                       | The file name.                                                                                                                     |
| sheetName            | String  | Path                       | The worksheet name.                                                                                                                |
| format               | String  | Query                      | Export format(CSV/XLS/HTML/MHTML/ODS/PDF/XML/TXT/TIFF/XLSB/XLSM/XLSX/XLTM/XLTX/XPS/PNG/JPG/JPEG/GIF/EMF/BMP/MD[Markdown]/Numbers). |
| verticalResolution   | Integer | Query                      | Image vertical resolution.                                                                                                         |
| horizontalResolution | Integer | Query                      | Image horizontal resolution.                                                                                                       |
| area                 | String  | Query                      | Represents the range to be printed.                                                                                                |
| pageIndex            | Integer | Query                      | Represents the page to be printed                                                                                                  |
| onePagePerSheet      | Boolean | Query                      | -                                                                                                                                  |
| printHeadings        | Boolean | Query                      | -                                                                                                                                  |
| folder               | String  | Query                      | The folder where the file is situated.                                                                                             |
| storageName          | String  | Query                      | The storage name where the file is situated.                                                                                       |

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
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="result"
```

**HTTP Status Codes**

| Code | Meaning               | Description                                                              |
| ---- | --------------------- | ------------------------------------------------------------------------ |
| 200  | OK                    | The request completed successfully.                                      |
| 400  | Bad Request           | The request is malformed or one or more parameters are invalid.          |
| 401  | Unauthorized          | Authentication failed, or the JWT token is missing or expired.           |
| 404  | Not Found             | The requested workbook, worksheet, or resource was not found.            |
| 500  | Internal Server Error | The server encountered an unexpected error while processing the request. |

## How to Use the Get Worksheet with Format API with SDKs?

### Get Worksheet with Format API Specification

The <a href="https://reference.aspose.cloud/cells/#/Worksheets/GetWorksheetWithFormat" rel="noopener noreferrer">Get Worksheet with Format API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

**cURL Example**

```bash
curl -v "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1?format=png&verticalResolution=150&horizontalResolution=150" \
  -X GET \
  -H "Authorization: Bearer <your_jwt_token>" \
  -H "Accept: application/octet-stream" \
  -o "converted_sheet.png"
```

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetWithFormat.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetWithFormat.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetWithFormat.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetWithFormat.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetWithFormat.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetWithFormat.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetWithFormat.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetWithFormat.go" >}}
{{</tab>}}
{{< /tabs >}}
