---
title: "Merge Cells in Excel Worksheet"
type: docs
url: /merge-cells-in-excel-worksheet/
weight: 110
---

This REST API indicates `merge` cells in an Excel file.

```bash

POST  http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/merge

```

- **Path Parameter**


|Parameter Name|Type|Description|
| :- | :- | :- |
| name | string |  The workbook name. |
| sheetName | string |  The worksheet name. |


- **Query Parameter**

|Parameter Name|Type|Description|
| :- | :- | :- |
|startRow| int | |
|startColumn| int | |
|totalRows| int | |
|totalColumns| int | |
|folder|string|Original workbook folder.|
|storageName|string|Storage name.|



- **Response**


```bash
{
    "Code": 200,
    "Status": "OK"
}

```


- **Api Reference**   

 [PostWorksheetMerge](https://apireference.aspose.cloud/cells/#/Cells/PostWorksheetMerge)

- **Cloud SDK Family**

Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:



{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" tabName4="Python" tabName5="Node.js" tabName6="Android" tabName7="Objective C" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "1e994f29ef29e752b6d02a2c5b63ea9b" "Examples-DotNET-CSharp-Cells-MergeCellsWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "5c1a68c4cea73845b221ff0d3b9ec9df" "Examples-PHP-Cells-PostWorksheetMerge-.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "3c5c9f9fff9898bb8251aa7ee9191641" "Examples-Ruby-Worksheet-merge_cells-.rb" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cloud" "5161752550311c9baf73ffa0a811ea0b" "MergeCellsInExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "04e9dd952c704f334a4eceb3925d479e" "Examples-Node.js-SDK-Cells-MergeCellsWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cloud" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-MergeCellsWorksheet-merge-cells-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cloud" "7effbad588b0c24b5f8ed2d7c7759b72" "Examples-Perl-Cells-MergeCellsWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cloud" "43d141d338376958100f323ea790f350" >}}

{{< /tab >}}

{{< /tabs >}}
