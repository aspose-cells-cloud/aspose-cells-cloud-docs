---
title: "Add a filter"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /autofilter/add-filter/
aliases: [/add-a-filter-for-a-filter-column/]
keywords: "REST API, autofilter, spreadsheets, excel"
description: "Cells.Cloud API for Excel operate: add autofilter on an Excel file."
weight: 30
---


This REST API add an `AutoFilter` on an Excel Worksheet.

**Query Parameter**

|Parameter Name|Type|Description|
| :- | :- | :- |
|range|string||
|fieldIndex|integer||
|criteria|string| |
|matchBlanks|string|true/false|
|refresh|string|true/false|
|folder|string|Original workbook folder.|
|storageName|string|Storage name.|


## REST API ##

|**API**|**Type**|**Description**|**Resource Link**|
| :- | :- | :- | :- |
|/cells/{name}/worksheets/{sheetName}/autoFilter/filter|PUT|Adds a filter for a filter column in worksheet|[PutWorksheetFilter](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetFilter)|

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetFilter) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use **cURL** command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X PUT "http://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/filter?range=A1:B1&fieldIndex=0&criteria=Year" -H "Content-Type: application/json" -H "Accept: application/json" 

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

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

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "1e994f29ef29e752b6d02a2c5b63ea9b" "Examples-DotNet-CSharp-Worksheet-AddWorksheetFilter-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "af3fea45644d431483f6df52cf3bfe26" "Examples-Java-filters-AddFilterToFilterColumnExample-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "5c1a68c4cea73845b221ff0d3b9ec9df" "Examples-PHP-LiteCells-Assemble.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cloud" "3c5c9f9fff9898bb8251aa7ee9191641" "Examples-Ruby-AutoFilter-put_worksheet_filter-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "04e9dd952c704f334a4eceb3925d479e" "Examples-Node.js-SDK-Worksheet-AddWorksheetFilter-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells" "5e354c1674e561aeb369d1d0f697ddbc" "Examples-Android-filters-AddFilterToFilterColumnExample-1.java" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cloud" "7effbad588b0c24b5f8ed2d7c7759b72" "Examples-Perl-Worksheet-AddWorksheetFilter-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cloud" "a52d6fe194479160b5b85f7d34262795" >}}

{{< /tab >}}

{{< /tabs >}}
