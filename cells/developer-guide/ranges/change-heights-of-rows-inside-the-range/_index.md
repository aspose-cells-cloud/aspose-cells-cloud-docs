---
title: "Change Heights of Rows inside the Range"
type: docs
url: /change-heights-of-rows-inside-the-range/
weight: 30
---

## **Introduction**
This example shows how to change the height of a rows within a named range within a workbook, using Aspose.Cells Cloud API in your applications. You can use our REST API with any language: .NET, Java, PHP, Ruby, Rails, Python, jQuery and many more.
## **API Information**

|**API**|**Type**|**Description**|**Resource Link**|
| :- | :- | :- | :- |
|/cells/{name}/worksheets/{sheetName}/ranges/rowHeight|POST|Change the row height of a named range|[PostWorksheetCellsRangeRowHeight](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeRowHeight)|
### **cURL Example**
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/rowHeight?value=15" -H "accept: application/json" -H "Content-Type: application/json" -d "{ \"ColumnCount\": 7, \"ColumnWidth\": 19, \"FirstColumn\": 0, \"FirstRow\": 9, \"Name\": \"string\", \"RefersTo\": \"string\", \"RowCount\": 1, \"RowHeight\": 15, \"Worksheet\": \"Sheet1\"}"

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
{{< tabs tabTotal="1" tabID="4" tabName1="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "18574f2f44071ac9d80be95568c193ff" >}}

{{< /tab >}}

{{< /tabs >}}
