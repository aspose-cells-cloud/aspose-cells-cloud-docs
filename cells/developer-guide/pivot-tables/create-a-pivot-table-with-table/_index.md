---
title: "Create a pivot table with table"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /pivottables/create-with-table/
aliases: [/create-a-pivottable-with-table/,/create-new-pivot-table-with-list-object-as-source-data/]
keywords: "REST API, pivot table, spreadsheets, excel"
description: "Cells.Cloud API for Excel operate: create pivot table with table."
weight: 30
---

This REST API create a `pivottable` with list object.


**Query Parameter**

|Parameter Name|Type|Description|
| :- | :- | :- |
|destsheetName|string|  |
|folder|string|Original workbook folder.|
|storageName|string|Storage name.|

**Request Body Parameter**

|Parameter Name|Type|Description|
| :- | :- | :- |
|CreatePivotTableRequest|Object | |


**CreatePivotTableRequest**

| Parameter Name|Type|Description|
| :- | :- | :- |
| Name | string |  |
| SourceData | string |  |
| DestCellName | string |  |
| UseSameSource | string | true/false.  |
| PivotFieldRows | int[] | |
| PivotFieldColumns | int[] | |
| PivotFieldData |  int[] | |


## REST API

|**API**|**Type**|**Description**|**Resource Link**|
| :- | :- | :- | :- |
|/cells/{name}/worksheets/{sheetName}/{listObjectIndex}/SummarizeWithPivotTable|POST|Creates a pivot table with list object.|[PostWorksheetListObjectSummarizeWithPivotTable](https://apireference.aspose.cloud/cells/#/ListObjects/PostWorksheetListObjectSummarizeWithPivotTable)|


The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/ListObjects/PostWorksheetListObjectSummarizeWithPivotTable) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use **cURL** command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL.


{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash

curl -v "https://api-qa.aspose.cloud/v3.0/cells/TestCase.xlsx/worksheets/Sheet2/listobjects/0/SummarizeWithPivotTable?folder=CellsTests&destsheetName=Sheet4" \
-X POST \
-d '{"Name":"TestPivot","DestCellName":"C1","PivotFieldRows":[0,1],"PivotFieldColumns":[2],"PivotFieldData":[3,4]}' \
-H "Content-Type: application/json" \
-H "Accept: application/json"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```bash

{  
  "Code": "200",
  "Status": "OK"
}

```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK Family

Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:
