---
title: "Export a Worksheet Area to PNG, PDF, CSV – Aspose.Cells Cloud API"
second_title: "Developer Guide"
linktitle: "Area"
type: docs
url: /worksheets/area-to-different-formats/
aliases: [/get-worksheet-for-area/]
keywords: "Aspose.Cells, export worksheet area, PNG, PDF, CSV, Excel conversion, REST API, SDK"
description: "Export a specific Excel worksheet range to PNG, PDF, CSV, and 20+ formats using Aspose.Cells Cloud REST API or SDKs."
weight: 230
ArticleTitle: "Export Worksheet Area to PNG, PDF, CSV with Aspose.Cells Cloud API – Complete Guide"
---
The **GetWorksheetWithFormat** API (`GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}`) enables developers to retrieve a specified worksheet from a workbook in various formats—including XLS, XLSX, PDF, PNG, JPEG, and others—by leveraging Aspose.Cells Cloud. The operation supports exporting a specific cell range (via the `area` query parameter) and allows customization such as image resolution, print settings, and page layout options, making it ideal for programmatic document conversion and reporting workflows.

This guide shows how to export a **specific cell range** from an Excel worksheet to PNG, PDF, CSV, and more than 20 additional formats using the Aspose.Cells Cloud API. For related operations such as exporting an entire worksheet or converting a workbook, see the **[Export Entire Worksheet](https://docs.aspose.cloud/cells/worksheets/worksheet-to-different-formats/)** and **[Convert Workbook to PDF](https://docs.aspose.cloud/cells/workbook/convert-to-pdf/)** pages.

## The Get Worksheet with Format Web API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer" target="_blank">JWT token-based authentication</a>.

### Request parameters

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

### Successful response

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

- **200 OK** – Returns the requested file in binary format (PNG, PDF, CSV, etc.).

### Error responses

| Status Code | Description                                                 |
| ----------- | ----------------------------------------------------------- |
| 400         | Bad request – missing or invalid parameters.                |
| 401         | Unauthorized – authentication token is missing or invalid.  |
| 404         | Not found – specified workbook or worksheet does not exist. |
| 500         | Internal server error – unexpected condition on the server. |

**Example error payload**

```json
{
  "error": {
    "code": "InvalidParameter",
    "message": "The 'area' parameter is malformed. Expected format: B3:K8."
  }
}
```

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make a call to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1?format=png&verticalResolution=100&horizontalResolution=90&area=B3%3AK8&folder=DotnetFiles" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

Converted image (binary PNG)

{{< /tab >}}

{{< /tabs >}}

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetWithFormat) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

## Cloud SDK Family

Using an SDK is the fastest way to develop. An SDK abstracts low‑level details, allowing you to focus on your project logic. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCellAreaWithFormat.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCellAreaWithFormat.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCellAreaWithFormat.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCellAreaWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCellAreaWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCellAreaWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCellAreaWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetCellAreaWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}
