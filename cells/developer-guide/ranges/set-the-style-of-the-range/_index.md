---
title: "Set the Style of the Range"
type: docs
url: /set-the-style-of-the-range/
weight: 70
---

## **Introduction**
This example allows you to set the style of the range, using Aspose.Cells Cloud API in your applications. You can use our REST API with any language: .NET, Java, PHP, Ruby, Rails, Python, jQuery and many more.
## **API Information**

|**API**|**Type**|**Description**|**Resource Link**|
| :- | :- | :- | :- |
|/cells/{name}/worksheets/{sheetName}/ranges/style|POST|Set the cell style of a named range|[PostWorksheetCellsRangeStyle](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeStyle)|
### **cURL Example**
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/style" -H "accept: application/json" -H "Content-Type: application/json" -d "{ \"Range\": { \"ColumnCount\": 2, \"ColumnWidth\": 0, \"FirstColumn\": 1, \"FirstRow\": 1, \"Name\": \"string\", \"RefersTo\": \"string\", \"RowCount\": 2, \"RowHeight\": 0, \"Worksheet\": \"Sheet1\" }, \"Style\": { \"Font\": { \"DoubleSize\": 1, \"IsBold\": true, \"IsItalic\": true, \"IsStrikeout\": true, \"IsSubscript\": true, \"IsSuperscript\": true } }}"

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
{{< tabs tabTotal="4" tabID="4" tabName1="PHP" tabName2="Ruby" tabName3="Objective C" tabName4="Go" >}}

{{< tab tabNum="1" >}}



{{< /tab >}}

{{< tab tabNum="2" >}}



{{< /tab >}}

{{< tab tabNum="3" >}}



{{< /tab >}}

{{< tab tabNum="4" >}}



{{< gist "aspose-cloud" "81d7e60eaf43ae7192df00993997afde" >}}

{{< /tab >}}

{{< /tabs >}}
