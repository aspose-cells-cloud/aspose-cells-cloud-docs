---
title: "Auto Fit Rows in Excel Workbooks"
type: docs
url: /auto-fit-rows-in-excel-workbooks/
keywords: "REST API, auto-fit rows, auto-fit height, auto-fit width, spreadsheets, excel "
description: "Auto-fit the height and the width of the rows using Aspose.Cells Cloud REST API in Python, Perl, .Net, Java and many more."
weight: 90
---

## **Introduction**
The Aspose.Cells Cloud API provides a straightforward approach to auto-fit the height and the width of rows in a worksheet, by just giving the row index. Our REST API can be used with any language: . NET, Java, PHP, Ruby, Rails, Python, jQuery and many more. Following example shows how to auto-fit the rows using Aspose.Cells Cloud API.
## **API Information**

|**API**|**Type**|**Description**|**Resource Link**|
| :- | :- | :- | :- |
|/cells/{name}/worksheets/{sheetName}/autofitrows|POST|Autofits rows in worksheet|[PostAutofitWorksheetRows](https://apireference.aspose.cloud/cells/#/Worksheets/PostAutofitWorksheetRows)|
### **cURL Example**
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X POST "http://api.aspose.com/v3.0/cells/myWorkbook.xlsx/autofitrows" -d '{"AutoFitMergedCells":true, "IgnoreHidden":true}' -H "Content-Type: application/json" -H "Accept: application/json"

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

{{< gist "aspose-cloud" "1e994f29ef29e752b6d02a2c5b63ea9b" "Examples-DotNET-CSharp-Rows-AutoFitRowsInWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "af3fea45644d431483f6df52cf3bfe26" "Examples-Java-rows-AutoFitRowsInWorksheet-autofit-rows-in-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "5c1a68c4cea73845b221ff0d3b9ec9df" "Examples-PHP-Rows-PostAutofitWorkbookRows-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cloud" "3c5c9f9fff9898bb8251aa7ee9191641" "Examples-Ruby-Workbook-autofit_workbook_rows-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "5161752550311c9baf73ffa0a811ea0b" "AutoFitRowsInExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cloud" "04e9dd952c704f334a4eceb3925d479e" "Examples-Node.js-SDK-Rows-AutoFitRowsInWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cloud" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-rows-AutoFitRowsInWorksheet-autofit-rows-in-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cloud" "7effbad588b0c24b5f8ed2d7c7759b72" "Examples-Perl-Rows-AutoFitRowsInWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cloud" "47291f603a163aa155e675f846e27ea2" >}}

{{< /tab >}}

{{< /tabs >}}
