---
title: "Ungroup columns in an Excel Worksheet"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /columns/ungroup/
aliases: [/ungroup-columns-in-an-excel-worksheet/, /ungroup-columns-in-excel-worksheet/]
keywords: "REST API, ungroup columns, spreadsheets, excel"
description: "Cells.Cloud API for Excel operate: ungroup columns from an Excel Worksheet."
weight: 70
---

This REST API indicates ungroup worksheet columns.
 
## RSET API
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/ungroup
 
```
The request parameters are: 
 
| Parameter Name | Type | Path/Query String/HTTPBody | Description| 
| :- | :- | :- |:- | 
| name | string | path | The workbook name. |
| sheetName | string | path | The worksheet name. |
| firstIndex | integer | query | The first column index to be operated. |
| lastIndex | integer | query | The last column index to be operated. |
| folder | string | query | The document folder. |
| storageName | string | query | storage name. |


The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Cells/PostUngroupWorksheetColumns) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use **cURL** command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash

curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/Columns/ungroup?firstIndex=1&lastIndex=5" -H "accept: application/json"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```bash

 {

  "Code": 200,

  "Status": "OK"

}

```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK Family

Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "1e994f29ef29e752b6d02a2c5b63ea9b" "Examples-DotNET-CSharp-Columns-UngroupColumnsInWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "af3fea45644d431483f6df52cf3bfe26" "Examples-Java-Columns-UngroupColumnsInWorksheet-ungroup-Columns-in-excel-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "5c1a68c4cea73845b221ff0d3b9ec9df" "Examples-PHP-Columns-PostUngroupWorksheetColumns-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cloud" "3c5c9f9fff9898bb8251aa7ee9191641" "Examples-Ruby-Columns-ungroup_worksheet_Columns-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "5161752550311c9baf73ffa0a811ea0b" "UngroupColumnsInExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cloud" "04e9dd952c704f334a4eceb3925d479e" "Examples-Node.js-SDK-Columns-UngroupColumnsInWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cloud" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-Columns-UngroupColumnsInWorksheet-ungroup-Columns-in-excel-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cloud" "7effbad588b0c24b5f8ed2d7c7759b72" "Examples-Perl-Columns-UngroupColumnsInWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cloud" "b9c6984d8f4f6b863a64da0fd68dbd96" >}}

{{< /tab >}}

{{< /tabs >}}
