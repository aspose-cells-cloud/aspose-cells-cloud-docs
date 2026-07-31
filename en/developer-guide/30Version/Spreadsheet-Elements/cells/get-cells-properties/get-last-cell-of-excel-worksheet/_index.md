---
title: "Get Last Cell of Excel Worksheet – Aspose.Cells Cloud API (v4.0)"
type: docs
url: /get-last-cell-of-excel-worksheet/
weight: 30
keywords: "Aspose.Cells, Excel API, get last cell, spreadsheet, cloud"
description: "Retrieve the address of the end cell of an Excel worksheet using Aspose.Cells Cloud REST API v4.0. Includes request details, cURL example, JSON response, and SDK samples."
ArticleTitle: "Get End Cell of an Excel Worksheet – Aspose.Cells Cloud API v4.0"
---

This REST API returns the **endcell** of an Excel worksheet when the `cellOrMethodName` parameter is set to `endcell`.

**Overview**  
The **Get Last Cell** operation returns the address of the last used cell in a specified worksheet. It is useful for determining the effective data range of a sheet without scanning the entire workbook.

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

### Parameters
| Parameter            | Type   | Required | Description |
|----------------------|--------|----------|-------------|
| `fileName`           | string | Yes      | Name of the Excel file stored in the cloud. |
| `worksheetName`      | string | Yes      | Name of the worksheet from which to retrieve the last cell. |
| `cellOrMethodName`   | string | Yes      | Must be set to **`endcell`** to invoke this operation. |
| `folder` *(optional)*| string | No       | Cloud folder path where the workbook is located. |
| `storageName` *(optional)*| string | No   | Name of the storage. If omitted, the default storage is used. |

### Response Codes
| Code | Description |
|------|-------------|
| **200** | Successful request – returns the cell information. |
| **400** | Bad request – missing or invalid parameters. |
| **401** | Unauthorized – authentication token is missing or invalid. |
| **404** | Not found – the specified workbook or worksheet does not exist. |
| **500** | Internal server error – an unexpected condition occurred. |

- **Use Aspose.Cells Cloud SDKs**

Using an SDK is the best way to accelerate development. An SDK handles low‑level details, allowing you to focus on your project tasks. Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

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

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetLastCellWorksheet-1.js" >}}

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

For further operations related to cell navigation, see the **[Get First Cell](/get-first-cell-of-excel-worksheet/)** and **[Get Max Row](/get-max-row-of-worksheet/)** topics.