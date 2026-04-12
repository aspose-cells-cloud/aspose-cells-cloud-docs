---
title: "Get Last Cell of Excel Worksheet – Aspose.Cells Cloud API (v4.0)"
type: docs
url: /get-last-cell-of-excel-worksheet/
weight: 30
keywords: "Aspose.Cells, Cloud API, Excel last cell, endcell, REST"
description: "Retrieve the address of the last used cell in an Excel worksheet with Aspose.Cells Cloud REST API (v4.0). Includes cURL request, JSON response, and SDK samples."
---

This REST API returns the **endcell** of an Excel worksheet when the `cellOrMethodName` parameter is set to `endcell`.

- **cURL Example.**

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/endcell" \
     -H "Authorization: Bearer <your_access_token>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Cell": {
    "Name": "F341",
    "Row": 340,
    "Column": 5,
    "Value": "<More Info>",
    "Type": "IsString",
    "Formula": "=HYPERLINK(SUBSTITUTE(HelpURLTemplate,\"xxxxxxxxxx\",[Help Topic]),\"<More Info>\")",
    "IsFormula": false,
    "IsMerged": false,
    "IsArrayHeader": false,
    "IsInArray": false,
    "IsErrorValue": false,
    "IsInTable": false,
    "IsStyleSet": false,
    "HtmlString": "<Font Style=\"TEXT-DECORATION: underline;FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\">&lt;More Info&gt;</Font>",
    "Style": {
      "link": {
        "Href": "/style",
        "Rel": "self"
      }
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

- **Response Fields Overview**

| Field           | Type    | Description                                           |
| --------------- | ------- | ----------------------------------------------------- |
| `Name`          | string  | Address of the cell (e.g., `F341`).                   |
| `Row`           | integer | Zero‑based row index.                                 |
| `Column`        | integer | Zero‑based column index.                              |
| `Value`         | string  | The cell’s displayed value.                           |
| `Type`          | string  | Data type of the cell (e.g., `IsString`).             |
| `Formula`       | string  | Formula text if the cell contains a formula.          |
| `IsFormula`     | bool    | Indicates whether the cell contains a formula.        |
| `IsMerged`      | bool    | Indicates whether the cell is part of a merged range. |
| `IsArrayHeader` | bool    | Indicates whether the cell is an array header.        |
| `IsInArray`     | bool    | Indicates whether the cell belongs to an array.       |
| `IsErrorValue`  | bool    | Indicates whether the cell contains an error value.   |
| `IsInTable`     | bool    | Indicates whether the cell is inside a table.         |
| `IsStyleSet`    | bool    | Indicates whether a style is applied to the cell.     |
| `HtmlString`    | string  | HTML‑encoded representation of the cell’s value.      |
| `Style.link`    | object  | Hyperlink to the style resource.                      |

- **Cloud SDK Family**

Using an SDK is the best way to accelerate development. An SDK handles low‑level details, allowing you to focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetLastCellWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetEndCellWorksheet-get-last-cell-excel-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetLastCell.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_last_cell.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetLastCellOfExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetLastCellWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetEndCellWorksheet-get-last-cell-excel-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

_Coming soon._

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetLastCellWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "3cf3e145c223fd6f6f3d9f6377092db5" >}}

{{< /tab >}}

{{< /tabs >}}
