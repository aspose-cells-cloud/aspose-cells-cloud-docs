---
title: "Get Cell Style from a Worksheet – Aspose.Cells Cloud API"
type: docs
url: /get-cell-style-from-a-worksheet/
weight: 10
keywords: "Aspose.Cells, get cell style, Excel API, REST, cloud SDK, spreadsheet styling"
description: "Learn how to retrieve the style of a specific cell in an Excel worksheet using Aspose.Cells Cloud REST API (v3.0). Includes cURL example, response schema, and SDK snippets."
---

Use this REST API to retrieve the **style** of a cell in an Excel worksheet.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}/style
```

The request parameters are:

| Parameter Name | Type   | Location | Description                         |
| -------------- | ------ | -------- | ----------------------------------- |
| name           | string | path     | The name of the Excel document.     |
| sheetName      | string | path     | The name of the worksheet.          |
| cellName       | string | path     | The address of the cell (e.g., A1). |
| folder         | string | query    | The folder that contains the file.  |
| storageName    | string | query    | The name of the storage to use.     |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetCellStyle) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make a call to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/a1/style" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
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

## Response Schema

| Field                    | Type    | Description                                                               |
| ------------------------ | ------- | ------------------------------------------------------------------------- |
| **Style**                | object  | Container for all style‑related properties of the cell.                   |
| Style.Font               | object  | Font settings (name, size, color, style flags).                           |
| Style.Font.Color         | object  | RGBA color values for the font.                                           |
| Style.Font.IsBold        | boolean | `true` if the font is bold.                                               |
| Style.Font.IsItalic      | boolean | `true` if the font is italic.                                             |
| Style.Font.IsStrikeout   | boolean | `true` if the font has a strike‑through.                                  |
| Style.Font.IsSubscript   | boolean | `true` if the font is subscript.                                          |
| Style.Font.IsSuperscript | boolean | `true` if the font is superscript.                                        |
| Style.Font.Name          | string  | Font family name (e.g., **Calibri**).                                     |
| Style.Font.Size          | number  | Font size in points.                                                      |
| Style.Font.Underline     | string  | Underline style (e.g., **Single**).                                       |
| Style.IsLocked           | boolean | Indicates whether the cell is protected from editing.                     |
| Style.IsTextWrapped      | boolean | `true` if text wrapping is enabled.                                       |
| Style.IsGradient         | boolean | `true` if a gradient fill is applied.                                     |
| Style.Pattern            | string  | Fill pattern name (e.g., **None**).                                       |
| Style.BorderCollection   | array   | List of border objects defining line style, color, and border type.       |
| Style.BackgroundColor    | object  | RGBA values for the cell background.                                      |
| Style.ForegroundColor    | object  | RGBA values for the cell foreground.                                      |
| …                        | …       | _(Other fields follow the same pattern as defined in the API reference.)_ |

## Related Operations

- **Update Multiple Cells Style** – Modify the style of several cells in a single request.
- **Set Value of a Cell** – Write data to a specific cell.

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

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
