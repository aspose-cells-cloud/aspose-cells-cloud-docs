---
title: "Delete a Shape by Index inside the Worksheet"
type: docs
url: /delete-a-shape-by-index-inside-the-worksheet/
weight: 50
---

## **Introduction**
This example shows how to delete a shape by index inside the worksheet, using Aspose.Cells Cloud API in your applications. You can use our REST API with any language: .NET, Java, PHP, Ruby, Rails, Python, jQuery and many more.
## **API Information**

|**API**|**Type**|**Description**|**Resource Link**|
| :- | :- | :- | :- |
|/cells/{name}/worksheets/{sheetName}/shapes/{shapeindex}|DELETE|Delete a shape in worksheet|[DeleteWorksheetShape](https://apireference.aspose.cloud/cells/#/Shapes/DeleteWorksheetShape)|
### **cURL Example**
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X DELETE "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes/1" -H "accept: application/json" 
-H "x-aspose-client: Containerize.Swagger"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{

  "Code" : 200,

  "Status" : "OK"

}

```

{{< /tab >}}

{{< /tabs >}}
## **SDK Source**
The Aspose.Cells Cloud SDKs can be downloaded from the following page: [Available SDKs](/cells/available-sdks/)
### **SDK Examples**
{{< tabs tabTotal="5" tabID="4" tabName1="C#" tabName2="Java" tabName3="Perl" tabName4="Go" tabName5="Swift" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "1e994f29ef29e752b6d02a2c5b63ea9b" "Example-DeleteWorksheetShape.cs">}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "af3fea45644d431483f6df52cf3bfe26" "Example-DeleteWorksheetShape.java">}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "7effbad588b0c24b5f8ed2d7c7759b72" "Example-DeleteWorksheetShape.pl">}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cloud" "146761753dfc29a19e41a7de616c9d2c" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "f342d1e6f85982e0429fcd9bed8b11a8" "Example-DeleteWorksheetShape.swift">}}

{{< /tab >}}

{{< /tabs >}}
