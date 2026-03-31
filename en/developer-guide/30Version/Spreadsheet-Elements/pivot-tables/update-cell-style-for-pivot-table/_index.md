---  
title: "Update Cell Style for Pivot Table"  
second_title: "Document"  
linktitle: Format  
type: docs  
url: /pivot-tables/format/  
aliases: [/update-cell-style-for-pivot-table/]  
keywords: "Aspose.Cells Cloud, pivot table style, update cell style API, REST API, Excel API, spreadsheet formatting, cloud SDK"  
description: "Learn how to update the style of a specific cell in an Aspose.Cells Cloud pivot table via the REST API. Includes endpoint, parameters, authentication, cURL example, and Go SDK code snippet."  
weight: 90  
---  

This REST API updates the **style** of a cell in a pivot table.

**Authentication** – All calls must include a valid JWT token in the `Authorization` header (`Bearer <jwt token>`).  
Obtain the token from the Aspose.Cells Cloud authentication service and ensure the token contains the required scopes for spreadsheet operations.

## REST API  

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/Format
```  

The request parameters are:

| Parameter Name   | Type    | Location | Description                                                                                         |
|------------------|---------|----------|-----------------------------------------------------------------------------------------------------|
| name             | string  | path     | Document name (required).                                                                           |
| sheetName        | string  | path     | Worksheet name (required).                                                                          |
| pivotTableIndex  | integer | path     | Index of the pivot table (required).                                                                |
| column           | integer | query    | Zero‑based column index of the cell to format (required).                                          |
| row              | integer | query    | Zero‑based row index of the cell to format (required).                                             |
| style            | object  | body     | Style DTO (data‑transfer object) that defines the new cell style.                                   |
| needReCalculate  | boolean | query    | Indicates whether the pivot table should be recalculated after styling. The default value is **false**. |
| folder           | string  | query    | Folder where the document is stored (optional).                                                     |
| storageName      | string  | query    | Name of the storage (optional).                                                                     |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/PivotTables/PostPivotTableCellStyle) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the **cURL** command‑line tool to access Aspose.Cells web services easily. The following example shows how to make a call to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0/Format?column=1&row=1" \
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