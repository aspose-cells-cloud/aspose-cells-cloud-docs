---
title: "Update style for pivot table"
second_title: "Document"
linktitle: "Format all"
type: docs
url: /pivot-tables/format-all/
aliases: [/update-style-for-pivot-table/]
keywords: "pivot table, update style, Aspose.Cells Cloud, REST API, Excel, spreadsheet, API"
description: "Learn how to update the style of an entire pivot table using the Aspose.Cells Cloud REST API. Includes request details, cURL example, and SDK snippets for multiple programming languages."
weight: 100
---

This REST API updates the style for a pivot table.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/FormatAll
```

The request parameters are:

| Parameter Name   | Type   | Location                     | Description                                          |
|------------------|--------|------------------------------|------------------------------------------------------|
| name             | string | path                         | The name of the workbook file.                       |
| sheetName        | string | path                         | The worksheet that contains the pivot table.         |
| pivotTableIndex  | integer| path                         | Zero‑based index of the pivot table to be formatted. |
| style            | object | body                         | A style DTO that defines the formatting to apply.   |
| needReCalculate  | boolean| query                        | Set to **true** to recalculate the pivot table after formatting; default is **false**. |
| folder           | string | query                        | The folder where the workbook is stored.             |
| storageName      | string | query                        | The name of the storage service.                     |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/PivotTables/PostPivotTableStyle) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make a call to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "http://api.aspose.com/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0/FormatAll" \
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

Using an SDK is the fastest way to develop against the API. The SDK abstracts low‑level details so you can focus on your business logic. See the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code example demonstrates how to call the API using the Go SDK:

{{< tabs tabTotal="1" tabID="4" tabName1="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "0b2caae7acfa3e947b856c07b6e8633a" >}}

{{< /tab >}}

{{< /tabs >}}