title: "Convert table to pivot table"
second_title: "Document"
linktitle: Convert
type: docs
url: /pivot-tables/convert-table-to-pivottable/
aliases: [/create-a-pivottable-with-table/,/create-new-pivot-table-with-list-object-as-source-data/]
keywords: "pivot table, list object, Aspose.Cells Cloud, REST API, convert table to pivot table"
description: "Learn how to create a pivot table from a list object using Aspose.Cells Cloud REST API. Includes request details, cURL example, and SDK references."
weight: 60
---

This REST API creates a **pivot table** from a list object.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/SummarizeWithPivotTable
```

The request parameters are:

| Parameter Name   | Type    | Location                     | Description                                 |
|------------------|---------|------------------------------|---------------------------------------------|
| name             | string  | path                         | Workbook file name.                         |
| sheetName        | string  | path                         | Worksheet that contains the list object.    |
| listObjectIndex  | integer | path                         | Index of the list object in the worksheet.  |
| destsheetName    | string  | query                        | Name of the destination worksheet.          |
| request          | object  | body                         | JSON payload that defines the pivot table. |
| folder           | string  | query                        | Folder path where the workbook resides.     |
| storageName      | string  | query                        | Name of the storage.                        |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/ListObjects/PostWorksheetListObjectSummarizeWithPivotTable) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the **cURL** command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api-qa.aspose.cloud/v3.0/cells/TestCase.xlsx/worksheets/Sheet2/listobjects/0/SummarizeWithPivotTable?folder=CellsTests&destsheetName=Sheet4" \
-X POST \
-d '{"Name":"TestPivot","DestCellName":"C1","PivotFieldRows":[0,1],"PivotFieldColumns":[2],"PivotFieldData":[3,4]}' \
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

Using an SDK is the best way to speed up development. An SDK handles low‑level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

