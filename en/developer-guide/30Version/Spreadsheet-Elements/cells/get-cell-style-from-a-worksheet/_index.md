---
title: "Get Cell Style from a Worksheet – Aspose.Cells Cloud API"
type: docs
url: /get-cell-style-from-a-worksheet/
weight: 10
date: 2024-03-15
keywords: "Aspose.Cells, Excel, REST API, cell style, spreadsheet, cloud SDK, API documentation"
description: "Learn how to retrieve the style of a specific cell in an Excel worksheet using Aspose.Cells Cloud REST API v3. Includes cURL, response schema, status codes, and SDK snippets for 8+ languages."
tags:
  - excel
  - cell-style
  - rest-api
  - cloud-sdk
categories:
  - cells
  - api-reference
---

Use this REST API to retrieve the **style** of a cell in an Excel worksheet.

## GetWorksheetCellStyle API

{{% alert color="primary" %}}
This endpoint is part of **Aspose.Cells Cloud API v3.0** and returns detailed style information—including font properties, borders, alignment, and fill patterns—for a specified cell in a worksheet.
{{% /alert %}}

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}/style
```

### Security and Authentication

The Aspose.Cells Cloud APIs are secure and require [JWT token-based authentication](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### Request Parameters

| Parameter Name | Type   | Location | Description                                      | Required |
|----------------|--------|----------|--------------------------------------------------|----------|
| `name`         | string | path     | The name of the Excel document.                  | Yes      |
| `sheetName`    | string | path     | The name of the worksheet.                       | Yes      |
| `cellName`     | string | path     | The address of the cell (e.g., `A1`, `$B$2`).    | Yes      |
| `folder`       | string | query    | The folder that contains the file.               | No       |
| `storageName`  | string | query    | The name of the storage to use.                  | No       |

> **Note**: Omit `folder` or `storageName` if using the default storage/folder configured in your Aspose.Cloud account.

### Response

A successful request returns the full style object for the specified cell in the `Style` property of the response.

```json
{
  "Style": {
    "Font": {
      "Color": { "A": 255, "R": 5, "G": 99, "B": 193 },
      "DoubleSize": 11,
      "IsBold": false,
      "IsItalic": false,
      "IsStrikeout": false,
      "IsSubscript": false,
      "IsSuperscript": false,
      "Name": "Calibri",
      "Size": 11,
      "Underline": "Single"
    },
    "Name": null,
    "CultureCustom": "General",
    "Custom": "",
    "BackgroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
    "ForegroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
    "IsFormulaHidden": false,
    "IsDateTime": false,
    "IsTextWrapped": false,
    "IsGradient": false,
    "IsLocked": true,
    "IsPercent": false,
    "ShrinkToFit": false,
    "IndentLevel": 0,
    "Number": 0,
    "RotationAngle": 0,
    "Pattern": "None",
    "TextDirection": "Context",
    "VerticalAlignment": "Bottom",
    "HorizontalAlignment": "General",
    "BorderCollection": [
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "BottomBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "DiagonalDown"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "DiagonalUp"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "Horizontal"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "LeftBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "RightBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "TopBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "Vertical"
      }
    ],
    "BackgroundThemeColor": null,
    "ForegroundThemeColor": null,
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet1/cells/a1/style",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

#### Response Schema

| Field                    | Type    | Description                                                               |
| ------------------------ | ------- | ------------------------------------------------------------------------- |
| `Style`                  | object  | Container for all style-related properties of the cell.                   |
| `Style.Font`             | object  | Font settings (name, size, color, style flags).                           |
| `Style.Font.Color`       | object  | RGBA color values for the font.                                           |
| `Style.Font.IsBold`      | boolean | `true` if the font is bold.                                               |
| `Style.Font.IsItalic`    | boolean | `true` if the font is italic.                                             |
| `Style.Font.IsStrikeout` | boolean | `true` if the font has a strike-through.                                  |
| `Style.Font.IsSubscript` | boolean | `true` if the font is subscript.                                          |
| `Style.Font.IsSuperscript`| boolean| `true` if the font is superscript.                                        |
| `Style.Font.Name`        | string  | Font family name (e.g., **Calibri**).                                     |
| `Style.Font.Size`        | number  | Font size in points.                                                      |
| `Style.Font.Underline`   | string  | Underline style (e.g., **Single**, **Double**, **None**).                 |
| `Style.IsLocked`         | boolean | Indicates whether the cell is protected from editing.                     |
| `Style.IsTextWrapped`    | boolean | `true` if text wrapping is enabled.                                       |
| `Style.IsGradient`       | boolean | `true` if a gradient fill is applied.                                     |
| `Style.Pattern`          | string  | Fill pattern name (e.g., **None**, **Gray75**, **LightVertical**).        |
| `Style.BorderCollection` | array   | List of border objects defining line style, color, and border type.       |
| `Style.BackgroundColor`  | object  | RGBA values for the cell background.                                      |
| `Style.ForegroundColor`  | object  | RGBA values for the cell foreground.                                      |

> **Tip**: All optional fields (e.g., `Name`, `Custom`, `BackgroundThemeColor`) may be `null` if not explicitly set.

### HTTP Status Codes

| Code | Meaning                     | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Style retrieved successfully; response contains the `Style` object. |
| 400  | Bad Request                 | Missing or invalid parameters (e.g., invalid `cellName` format, unsupported file type). |
| 401  | Unauthorized                | Invalid or missing JWT token. |
| 404  | Not Found                   | File, worksheet, or cell not found in the document. |
| 413  | Payload Too Large           | Requested resource exceeds size limit.          |
| 500  | Internal Server Error       | Unexpected server error.                        |

#### Error Responses

Typical error payloads follow the standard Aspose.Cells format:

**400 Bad Request**
```json
{
  "Code": 400,
  "Message": "Invalid parameter 'cellName'.",
  "Description": "The cell name provided is not in a valid A1 format."
}
```

**401 Unauthorized**
```json
{
  "Code": 401,
  "Message": "Authentication failed.",
  "Description": "The JWT token is missing or invalid."
}
```

**404 Not Found**
```json
{
  "Code": 404,
  "Message": "Worksheet 'Sheet2' not found.",
  "Description": "The specified worksheet does not exist in the document."
}
```

## How to Use the GetWorksheetCellStyle API

### Using cURL

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/a1/style" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your_jwt_token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Style": {
    "Font": {
      "Color": { "A": 255, "R": 5, "G": 99, "B": 193 },
      "DoubleSize": 11,
      "IsBold": false,
      "IsItalic": false,
      "IsStrikeout": false,
      "IsSubscript": false,
      "IsSuperscript": false,
      "Name": "Calibri",
      "Size": 11,
      "Underline": "Single"
    },
    "Name": null,
    "CultureCustom": "General",
    "Custom": "",
    "BackgroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
    "ForegroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
    "IsFormulaHidden": false,
    "IsDateTime": false,
    "IsTextWrapped": false,
    "IsGradient": false,
    "IsLocked": true,
    "IsPercent": false,
    "ShrinkToFit": false,
    "IndentLevel": 0,
    "Number": 0,
    "RotationAngle": 0,
    "Pattern": "None",
    "TextDirection": "Context",
    "VerticalAlignment": "Bottom",
    "HorizontalAlignment": "General",
    "BorderCollection": [
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "BottomBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "DiagonalDown"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "DiagonalUp"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "Horizontal"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "LeftBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "RightBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "TopBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "Vertical"
      }
    ],
    "BackgroundThemeColor": null,
    "ForegroundThemeColor": null,
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet1/cells/a1/style",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Using Aspose.Cells Cloud SDKs

Using an SDK is the best way to speed up development. An SDK handles low-level details (e.g., authentication, serialization) so you can focus on your project tasks. All SDKs are open-source and maintained on [GitHub](https://github.com/aspose-cells-cloud).

> **Note**: All SDK examples below use the latest stable release (v23.12+). See the [SDK Changelog](/sdk-changelog/) for version-specific updates.

{{< tabs tabTotal="8" tabID="4" tabName1="C# (v23.12)" tabName2="Java (v23.12)" tabName3="PHP (v23.12)" tabName4="Ruby (v23.12)" tabName5="Node.js (v23.12)" tabName6="Python (v23.12)" tabName7="Perl (v23.12)" tabName8="Go (v23.12)" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCellStyle.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCellStyle.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCellStyle.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCellStyle.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCellStyle.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCellStyle.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCellStyle.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetCellStyle.go" >}}

{{< /tab >}}

{{< /tabs >}}

### Interactive API Reference

You can explore and test this endpoint directly in your browser using the [Interactive OpenAPI (Swagger) reference](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetCellStyle).

## See Also

- [Set Cell Style](/set-cell-style/)
- [Get Cell Value](/get-cell-value/)
- [Apply Cell Formatting](/apply-cell-formatting/)
- [Cell Style Best Practices](/cell-style-guidelines/)  
- [Working with Excel Files in the Cloud](/excel-cloud-overview/)