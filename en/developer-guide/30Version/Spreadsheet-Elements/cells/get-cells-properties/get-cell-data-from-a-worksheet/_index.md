---
title: "Get Cell Data from a Worksheet"
type: docs
url: /get-cell-data-from-a-worksheet/
weight: 10
keywords: "Aspose.Cells Cloud, get cell data, Excel API, REST API, cell value, worksheet API, Aspose API example"
description: "Retrieve a single cell’s value, type, and style from an Excel worksheet using Aspose.Cells Cloud REST API (v3.0). Includes cURL, SDK examples, parameters, and error handling."
---

This REST API retrieves a cell from an Excel worksheet when the **`cellOrMethodName`** parameter specifies a cell name (an A1‑style address such as `A3`).

**Request parameters**

| Parameter          | Type   | Required | Description                                                                                                                              |
| ------------------ | ------ | -------- | ---------------------------------------------------------------------------------------------------------------------------------------- |
| `client_id`        | string | Yes      | Your Aspose Cloud client identifier.                                                                                                     |
| `client_secret`    | string | Yes      | Your Aspose Cloud client secret.                                                                                                         |
| `storage`          | string | No       | Name of the cloud storage to use (e.g., `Aspose`). If omitted, the default storage is used.                                              |
| `folder`           | string | No       | Path to the folder containing the workbook in the selected storage.                                                                      |
| `cellOrMethodName` | string | Yes      | The cell address in A1 notation (e.g., `A3`). It can also be a method name for advanced operations (not covered in this simple example). |
| `fileName`         | string | Yes      | Name of the Excel file (e.g., `myWorkbook.xlsx`).                                                                                        |
| `sheetName`        | string | Yes      | Name of the worksheet that contains the target cell (e.g., `Sheet1`).                                                                    |

---

### cURL Example

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/A3?client_id=YOUR_CLIENT_ID&client_secret=YOUR_CLIENT_SECRET" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Cell": {
    "Name": "A3",
    "Row": 2,
    "Column": 0,
    "Value": "Statistical",
    "Type": "IsString",
    "IsFormula": false,
    "IsMerged": false,
    "IsArrayHeader": false,
    "IsInArray": false,
    "IsErrorValue": false,
    "IsInTable": false,
    "IsStyleSet": false,
    "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\">Statistical</Font>",
    "Style": {
      "link": {
        "Href": "/style",
        "Rel": "self"
      }
    },
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/A3",
      "Rel": "self"
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

- **Cloud SDKs**

Using an SDK is the fastest way to develop against the API. An SDK handles low‑level details, allowing you to focus on your project logic. Please check the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of **Aspose.Cells Cloud** SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCell.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCell.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCell.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCell.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCell.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCell.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCell.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetCell.go" >}}

{{< /tab >}}

{{< /tabs >}}
