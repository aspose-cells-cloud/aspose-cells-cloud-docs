---
title: "Update Multiple Cells Style – Aspose.Cells Cloud API Reference (v3.0)"
date: 2024-05-10
type: docs
url: /update-multiple-cells-style/
weight: 100
keywords:
  [
    "Aspose.Cells",
    "update multiple cells style",
    "Excel cell style API",
    "cloud SDK",
    "REST API",
    "cURL example",
    "JSON request",
    "JWT authentication",
  ]
description: "Update Excel cell range styles (font, color, background) via Aspose.Cells Cloud REST API v3.0 with cURL and SDKs"
linktitle: "Update Cells Style API"
ArticleTitle: "Aspose.Cells Cloud API: Update Multiple Cells Style in Excel"
---
The **PostUpdateWorksheetRangeStyle** API (`POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/style`) enables developers to update the formatting style for a specified cell range in an Excel worksheet via Aspose.Cells Cloud, supporting key parameters including `name`, `sheetName`, `range`, and a `style` object in the request body to apply consistent styling across multiple cells efficiently.

## The Post Update Worksheet Range Style Web API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/style
```

### Security and Authentication

The Aspose.Cells Cloud APIs use [JWT token-based authentication](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/). Include a valid bearer token in the `Authorization` header:

```http
Authorization: Bearer <your_jwt_token>
```

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| name | String | Path | The file name. |
| sheetName | String | Path | The worksheet name. |
| range | String | Query | Represents the range to which the specified cells applies. |
| style | class:style | HTTPBody | Style with update style settings. |
| folder | String | Query | The folder where the file is situated. |
| storageName | String | Query | The storage name where the file is situated. |

#### Style Object

The `style` JSON object supports the following optional properties:

- **Font** – Font settings (e.g., `Name`, `Size`, `IsBold`, `IsItalic`, `Color`, `IsStrikeout`, `IsSubscript`, `IsSuperscript`).
- **BackgroundColor** – Background color in ARGB format: `{ "A":255, "R":0, "G":0, "B":0 }`.
- **ForegroundColor** – Foreground color in ARGB format.
- **Name**, **CultureCustom**, **Custom** – Additional style metadata.

> 📝 **Note**: All color values must be in ARGB format with channel values between `0` and `255`. Invalid values return `400 Bad Request`.

### Response

```json
[
  {
    "Name": "CellsCloudResponse",
    "DataType": {
      "Identifier": "Class",
      "Reference": "CellsCloudResponse"
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

Returns a `CellsCloudResponse` object:


| Field    | Type    | Description                                          |
| -------- | ------- | ---------------------------------------------------- |
| `Status` | string  | Operation result status (`"OK"` on success).         |
| `Code`   | integer | HTTP status code (e.g., `200`, `400`, `401`, `500`). |

#### HTTP Status Codes


---

This REST API updates the **style** for a range of cells in an Excel worksheet.

## How to Use the PostUpdateWorksheetRangeStyle API

### Using cURL

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
        "BackgroundColor": { "A":10, "R":10, "G":10, "B":10 },
        "ForegroundColor": { "A":255, "R":255, "G":255, "B":0 }
      }' \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt_token>"
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

### Using SDKs

Using an SDK is the best way to accelerate development. SDKs handle low-level details like authentication, serialization, and error handling.

See the [Aspose.Cells Cloud SDKs GitHub repository](https://github.com/aspose-cells-cloud){: rel="noopener noreferrer"} for full source and documentation.

Examples for multiple languages:

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

---

## See Also

- [Read cell range style](/read-cell-range-style/)
- [Get worksheet cell styles](/get-worksheet-cell-styles/)

## API Reference

- [OpenAPI Specification: PostUpdateWorksheetRangeStyle](https://apireference.aspose.cloud/cells/#/Cells/PostUpdateWorksheetRangeStyle)
