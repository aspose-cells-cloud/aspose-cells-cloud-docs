---
title: "Copy Rows in Excel Worksheet"
type: docs
url: /copy-rows-in-excel-worksheet/
weight: 30
---

## **Introduction**
This example shows how to copy rows within a Excel Worksheet using Aspose.Cells Cloud API in your applications. You can use our REST API with any language: .NET, Java, PHP, Ruby, Rails, Python, jQuery and many more.

## **API Information**

|**API**|**Type**|**Description**|**Resource Link**|
| :- | :- | :- | :- |
|` `/cells/{name}/worksheets/{sheetName}/cells/rows/copy|` `POST|` `Copy|` `[PostCopyWorksheetRows](https://apireference.aspose.cloud/cells/#/Cells/PostCopyWorksheetRows)|
### **cURL Example**
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/copy?sourceRowIndex=1&destinationRowIndex=12&rowNumber=10" -H "accept: application/json" 

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
## **SDK Source**
The Aspose.Cells Cloud SDKs can be downloaded from the following page: [Available SDKs](/cells/available-sdks/)
### **SDK Examples**
{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "1e994f29ef29e752b6d02a2c5b63ea9b" "Examples-DotNET-CSharp-Rows-CopyRowsInWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "af3fea45644d431483f6df52cf3bfe26" "Examples-Java-rows-CopyRowsInWorksheet-copy-rows-in-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "5c1a68c4cea73845b221ff0d3b9ec9df" "Examples-PHP-Rows-PostCopyWorksheetRows-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cloud" "3c5c9f9fff9898bb8251aa7ee9191641" "Examples-Ruby-Rows-copy_worksheet_rows-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "5161752550311c9baf73ffa0a811ea0b" "CopyRowsInExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cloud" "04e9dd952c704f334a4eceb3925d479e" "Examples-Node.js-SDK-Rows-CopyRowsInWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cloud" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-rows-CopyRowsInWorksheet-copy-rows-in-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cloud" "7effbad588b0c24b5f8ed2d7c7759b72" "Examples-Perl-Rows-CopyRowsInWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cloud" "dec38026e75ab416ae85afd684c924d6" >}}

{{< /tab >}}

{{< /tabs >}}
