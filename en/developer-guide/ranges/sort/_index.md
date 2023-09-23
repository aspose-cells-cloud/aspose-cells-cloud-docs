---
title: Range Sort 
second_title: "Aspose.Cells Cloud Document"
linktitle: "Sort"
type: docs
keywords: "Range Sort."
url: /ranges/sort/
description: Sets outline border around a range of cells. 
weight: 20
---

This REST API indicates range sort. 

## RSET API


```bash

POST http://api.aspose.cloud/v3.0//cells/{name}/worksheets/{sheetName}/ranges/sort

```

The request parameters are: 

| Parameter Name | Type | Path/Query String/HTTPBody | Description | 
| :- | :- | :- |:- | 
|name|String|Path|The workbook name.|
|sheetName|String|Path|The worksheet name.|
|rangeOperate|Class|Body|Range Sort Request |
|folder|String|Query|Original workbook folder.|
|storageName|String|Query|Storage name.|



The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/RangesController/PostWorksheetCellsRangeSort) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use cURL command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
{{< tab tabNum="1" >}}
```powershell
curl -v "http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/sort" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
```
{{< /tab >}}
{{< tab tabNum="2" >}}
```powershell

```
{{< /tab >}}

{{< /tabs >}}

## Cloud SDK Family

Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the GitHub repository for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

