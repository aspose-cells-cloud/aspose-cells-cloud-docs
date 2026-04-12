---
title: "Delete a Column on an Excel Worksheet"
second_title: "Document"
linktitle: "Delete"
type: docs
url: /columns/delete/
aliases:
  [/delete-column-from-an-excel-worksheet/, /delete-column-from-a-worksheet/]
keywords: "Delete a Column, Aspose.Cells Cloud, Excel API, REST, Spreadsheet"
description: "Learn how to delete one or more columns from an Excel worksheet using the Aspose.Cells Cloud REST API. Includes request syntax, required parameters, authentication, error handling, and sample code in multiple SDKs."
weight: 80
---

This REST API deletes **one or more columns** in an Excel worksheet.

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/{columnIndex}
```

### Request parameters

| Parameter Name      | Type    | Location | Required | Description                                                                                      |
| ------------------- | ------- | -------- | -------- | ------------------------------------------------------------------------------------------------ |
| **name**            | string  | path     | Yes      | The workbook file name.                                                                          |
| **sheetName**       | string  | path     | Yes      | The worksheet name.                                                                              |
| **columnIndex**     | integer | path     | Yes      | Zero‑based index of the first column to delete.                                                  |
| **startColumn**     | integer | query    | No       | Zero‑based index of the column where the deletion starts (defaults to `columnIndex`).            |
| **totalColumns**    | integer | query    | No       | Number of columns to delete. If omitted, only the column identified by `columnIndex` is removed. |
| **updateReference** | boolean | query    | No       | When `true`, cell references (including formulas) are updated automatically after the deletion.  |
| **folder**          | string  | query    | No       | Path to the folder that contains the workbook.                                                   |
| **storageName**     | string  | query    | No       | Name of the Aspose Cloud storage service.                                                        |

### Example request

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/1?startColumn=1&totalColumns=1&updateReference=true" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>"
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

### Responses

| HTTP Code | Description                                                 | Example                                                       |
| --------- | ----------------------------------------------------------- | ------------------------------------------------------------- |
| **200**   | Success – the column(s) were deleted.                       | `{ "Code": 200, "Status": "OK" }`                             |
| **400**   | Bad request – missing or invalid parameters.                | `{ "Code": 400, "Message": "Invalid totalColumns value." }`   |
| **401**   | Unauthorized – missing or invalid access token.             | `{ "Code": 401, "Message": "Authentication failed." }`        |
| **404**   | Not found – workbook or worksheet does not exist.           | `{ "Code": 404, "Message": "Worksheet 'Sheet1' not found." }` |
| **500**   | Internal server error – unexpected condition on the server. | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Cells/DeleteWorksheetColumns) defines the full programming interface and lets you perform REST interactions directly from a web browser.

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}
