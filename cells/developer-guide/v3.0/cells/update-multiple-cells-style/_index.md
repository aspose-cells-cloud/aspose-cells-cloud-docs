---
title: "Update Multiple Cells Style"
type: docs
url: /update-multiple-cells-style/
weight: 20
---

This REST API indicates set `cells style` to a cell in an Excel file.

```bash

POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/style

```

- **Path Parameter**


|Parameter Name|Type|Description|
| :- | :- | :- |
| name | string |  The workbook name. |
| sheetName | string |  The worksheet name. |


- **Query Parameter**

|Parameter Name|Type|Description|
| :- | :- | :- |
| range | string |  range name. |
|folder|string|Original workbook folder.|
|storageName|string|Storage name.|


- **Request Body Parameter**

|Parameter Name|Type|Description|
| :- | :- | :- |
|Style |object | cell style |


- **Response**


```bash
{
    "Code": 200,
    "Status": "OK"
}

```


- **Api Reference**   

 [PostUpdateWorksheetRangeStyle](https://apireference.aspose.cloud/cells/#/Cells/PostUpdateWorksheetRangeStyle)

- **Cloud SDK Family**

Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:



{{< tabs tabTotal="3" tabID="4" tabName1="PHP" tabName2="Ruby" tabName3="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "5c1a68c4cea73845b221ff0d3b9ec9df" "Examples-PHP-Cells-PostUpdateWorksheetCellStyle-.php" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "3c5c9f9fff9898bb8251aa7ee9191641" "Examples-Ruby-Cells-post_update_worksheet_cell_style-.rb" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "59dae0a6697e3c68ade244ed28b27d10" >}}

{{< /tab >}}

{{< /tabs >}}
