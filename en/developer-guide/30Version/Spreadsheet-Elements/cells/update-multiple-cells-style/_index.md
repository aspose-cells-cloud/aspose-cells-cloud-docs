---
title: "Update Multiple Cells Style – Aspose.Cells Cloud API Reference (v3.0)"
type: docs
url: /update-multiple-cells-style/
weight: 20
keywords: ["Aspose.Cells", "update multiple cells style", "Excel cell style API", "cloud SDK", "REST API", "cURL example", "JSON request", "JWT authentication"]
description: "Learn how to update the style of a range of cells in an Excel workbook using the Aspose.Cells Cloud REST API v3.0. Includes endpoint, HTTP method, parameters, cURL and SDK examples, authentication, error handling, and version information."
ArticleTitle: "Update Multiple Cells Style – Aspose.Cells Cloud API Reference (v3.0)"
---

## REST API

This REST API sets the **style** for a range of cells in an Excel workbook.

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/style
```

## Security and Authentication

The Aspose.Cells Cloud APIs are secure and require [JWT token-based authentication](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).


### Request parameters

| Parameter Name | Type   | Location | Description |
|----------------|--------|----------|-------------|
| **name**       | string | path     | Workbook name. |
| **sheetName**  | string | path     | Worksheet name. |
| **range**      | string | query    | The cell range (e.g., `A1:A10`). |
| **style**      | object | body     | JSON object that defines the style to apply. |
| **folder**     | string | query    | Folder that contains the workbook. |
| **storageName**| string | query    | Name of the storage. |

#### Style object
The `style` JSON object represents cell formatting. It may contain any of the following optional properties:

- **Font** – Font settings (`Name`, `Size`, `IsBold`, `IsItalic`, `Color`, etc.).  
- **BackgroundColor** – Background color in ARGB format.  
- **ForegroundColor** – Foreground color in ARGB format.  
- **Name**, **CultureCustom**, **Custom** – Additional style metadata.

## **Response**

Return CellCloudResponse.

- **Response Fields Overview**

| Field           | Type    | Description                                           |
| --------------- | ------- | ----------------------------------------------------- |
| `Status`          | string  |                    |
| `Code`           | integer | 200,400,401,500,...                                 |


```json
{
  "Status":"OK",
  "Code":200
}
```

**Http Status Codes**

| Code | Meaning                     | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Compression succeeded; response contains compressed file details. |
| 400  | Bad Request                 | Missing or invalid parameters (e.g., unsupported file type). |
| 401  | Unauthorized                | Invalid or missing JWT token. |
| 413  | Payload Too Large           | Uploaded file exceeds size limit. |
| 500  | Internal Server Error       | Unexpected server error. |

## How to Use the PostUpdateWorksheetRangeStyle API with SDKs

### PostUpdateWorksheetRangeStyle API Specification

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Cells/PostUpdateWorksheetRangeStyle) provides the full schema.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
cURL -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/style?range=a1%3Aa10" \
  -X POST \
  -d '{
        "Font": {
          "Color": { "A":255, "R":255, "G":255, "B":0 },
          "Size": 22,
          "IsBold": true,
          "IsItalic": true,
          "IsStrikeout": true,
          "IsSubscript": true,
          "IsSuperscript": true,
          "Name": "Arial"
        },
        "Name": "string",
        "CultureCustom": "string",
        "Custom": "string",
        "BackgroundColor": { "A":10, "R":10, "G":10, "B":10 },
        "ForegroundColor": { "A":255, "R":255, "G":255, "B":0 }
      }' \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}


### Use Aspose.Cells Cloud SDKs

Using an SDK is the best way to speed up development. An SDK handles low‑level details, allowing you to focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeStyle.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeStyle.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeStyle.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeStyle.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeStyle.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeStyle.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeStyle.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeStyle.go" >}}

{{< /tab >}}

{{< /tabs >}}