---
title: "Update cell style for pivot table"
second_title: "Document"
linktitle: Format
type: docs
url: /pivot-tables/format/
aliases: [/update-cell-style-for-pivot-table/]
keywords: "Aspose.Cells Cloud, REST API, pivot table, update cell style, Excel, spreadsheet"
description: "Learn how to use Aspose.Cells Cloud REST API to update the style of a cell in a pivot table. Includes request details, cURL example, and SDK code snippets for multiple programming languages."
weight: 90
---

This REST API updates the **style** of a cell in a pivot table.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/Format
```

The request parameters are:

| Parameter Name   | Type    | Location                     | Description                                                                 |
|------------------|---------|------------------------------|-----------------------------------------------------------------------------|
| name             | string  | path                         | Document name.                                                              |
| sheetName        | string  | path                         | Worksheet name.                                                             |
| pivotTableIndex  | integer | path                         | Index of the pivot table.                                                   |
| column           | integer | query                        | Zero‑based column index of the cell to format.                              |
| row              | integer | query                        | Zero‑based row index of the cell to format.                                 |
| style            | object  | body                         | Style DTO (data‑transfer object) that defines the new cell style.          |
| needReCalculate  | boolean | query                        | Indicates whether the pivot table should be recalculated after styling. Default is **false**. |
| folder           | string  | query                        | Folder where the document is stored.                                        |
| storageName      | string  | query                        | Name of the storage.                                                        |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/PivotTables/PostPivotTableCellStyle) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the **cURL** command‑line tool to access Aspose.Cells web services easily. The following example shows how to make a call to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "http://api.aspose.com/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0/Format?column=1&row=1" \
-X POST \
-d '{"Font":{"Name":"Arial","Size":10}}' \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
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

## Cloud SDK Family

Using an SDK is the fastest way to develop. An SDK abstracts low‑level details, allowing you to focus on your business logic. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code example demonstrates how to call Aspose.Cells web services using the **Go** SDK:

{{< tabs tabTotal="1" tabID="4" tabName1="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "3236805d26482f06f4656b14f2d00d79" >}}

{{< /tab >}}

{{< /tabs >}}