---
title: "Clear Contents and Styles of Cells in Excel Worksheet"
type: docs
url: /clear-contents-and-styles-of-cells-in-excel-worksheet/
weight: 50
---

This REST API indicates `clear` cells `content` in an Excel file.

```bash

POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/clearcontents

```

- **Path Parameter**


|Parameter Name|Type|Description|
| :- | :- | :- |
| name | string |  The workbook name. |
| sheetName | string |  The worksheet name. |


- **Query Parameter**

|Parameter Name|Type|Description|
| :- | :- | :- |
|folder|string|Original workbook folder.|
|storageName|string|Storage name.|
|range|string|Represents the range to which the specified cells applies.|
|startRow| int | |
|startColumn| int | |
|endRow| int | |
|endColumn| int | |


- **Response**


```bash
{
    "Code": 200,
    "Status": "OK"
}

```


- **Api Reference**   

 [PostClearContents](https://apireference.aspose.cloud/cells/#/Cells/PostClearContents)

- **Cloud SDK Family**

Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:


{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "1e994f29ef29e752b6d02a2c5b63ea9b" "Examples-DotNET-CSharp-Cells-ClearCellContentStyleWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "af3fea45644d431483f6df52cf3bfe26" "Examples-Java-cells-ClearCellContentStyleWorksheet-clear-cell-content-style.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "5c1a68c4cea73845b221ff0d3b9ec9df" "Examples-PHP-Cells-PostClearContents-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cloud" "3c5c9f9fff9898bb8251aa7ee9191641" "Examples-Ruby-Cells-clear_cells_contents-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "5161752550311c9baf73ffa0a811ea0b" "ClearContentsFromExcelWorkSheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cloud" "04e9dd952c704f334a4eceb3925d479e" "Examples-Node.js-SDK-Cells-ClearCellContentStyleWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cloud" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-ClearCellContentStyleWorksheet-clear-cell-content-style.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cloud" "7effbad588b0c24b5f8ed2d7c7759b72" "Examples-Perl-Cells-ClearCellContentStyleWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cloud" "bd4048e2d1e2d751b75c962b42162dc5" >}}

{{< /tab >}}

{{< /tabs >}}
