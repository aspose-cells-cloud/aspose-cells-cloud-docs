---
title: "Aspose.Cells Cloud API – Merge Cells Range"
second_title: "Document"
linktitle: "Merge"
type: docs
url: /ranges/merge/
aliases: [/combines-a-range-of-cells-into-a-single-cell/]
keywords: "Aspose.Cells, merge cells, Excel API, REST, cloud SDK"
description: "Merge a range of cells into a single cell using Aspose.Cells Cloud REST API. Learn request format, parameters, and SDK examples for C#, Java, Python, and more."
weight: 20
---

This REST API merges a range of cells into a single cell on an Excel worksheet.

**Overview** – Merging a range combines the selected cells into one cell, preserving the value of the upper‑left cell and discarding the rest. Use this operation when you need to create a header that spans multiple columns or rows, or when you want to simplify the layout of a worksheet.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/merge
```

### **Request parameters**

| Parameter Name  | Type   | Location | Description                                         |
| --------------- | ------ | -------- | --------------------------------------------------- |
| **name**        | string | path     | Workbook name.                                      |
| **sheetName**   | string | path     | Worksheet name.                                     |
| **range**       | object | body     | Range object that specifies the cells to be merged. |
| **folder**      | string | query    | Folder where the workbook is stored.                |
| **storageName** | string | query    | Name of the storage.                                |

#### Request Body Schema

The **Range** object must contain the following fields (all others are optional):

| Property        | Type    | Required | Description                                            |
| --------------- | ------- | -------- | ------------------------------------------------------ |
| **FirstRow**    | integer | Yes      | Zero‑based index of the first row in the range.        |
| **FirstColumn** | integer | Yes      | Zero‑based index of the first column in the range.     |
| **RowCount**    | integer | Yes      | Number of rows to include in the range.                |
| **ColumnCount** | integer | Yes      | Number of columns to include in the range.             |
| **Name**        | string  | No       | Optional name for the range.                           |
| **RefersTo**    | string  | No       | A formula that the range refers to.                    |
| **Worksheet**   | string  | No       | Worksheet name (if different from the path parameter). |
| **RowHeight**   | number  | No       | Height of rows in the range (pixels).                  |
| **ColumnWidth** | number  | No       | Width of columns in the range (pixels).                |

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make a call to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/merge" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "FirstRow": 9,
        "FirstColumn": 0,
        "RowCount": 1,
        "ColumnCount": 7
      }'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

#### Response Details

| HTTP Status                   | Description                                             | Sample JSON                                            |
| ----------------------------- | ------------------------------------------------------- | ------------------------------------------------------ |
| **200 OK**                    | The range was merged successfully.                      | `{ "Code": 200, "Status": "OK" }`                      |
| **400 Bad Request**           | Invalid range parameters (e.g., out‑of‑bounds indices). | `{ "Code": 400, "Message": "Invalid range." }`         |
| **401 Unauthorized**          | Missing or invalid JWT token.                           | `{ "Code": 401, "Message": "Authentication failed." }` |
| **404 Not Found**             | Workbook or worksheet not found.                        | `{ "Code": 404, "Message": "Resource not found." }`    |
| **500 Internal Server Error** | Unexpected server error.                                | `{ "Code": 500, "Message": "Internal server error." }` |

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeMerge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeMerge.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeMerge.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeMerge.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeMerge.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeMerge.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeMerge.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeMerge.go" >}}

{{< /tab >}}

{{< /tabs >}}
