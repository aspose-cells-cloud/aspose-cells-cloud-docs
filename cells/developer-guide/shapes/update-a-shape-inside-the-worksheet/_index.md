---
title: "Update a Shape inside the Worksheet"
type: docs
url: /update-a-shape-inside-the-worksheet/
weight: 31
---

## **Introduction**
This example shows how to update a shape inside the worksheet, using Aspose.Cells Cloud API in your applications. You can use our REST API with any language: .NET, Java, PHP, Ruby, Rails, Python, jQuery and many more.
## **API Information**

|**API**|**Type**|**Description**|**Resource Link**|
| :- | :- | :- | :- |
|/cells​/{name}​/worksheets​/{sheetName}​/shapes​/{shapeindex}|POST|Updates a shape in worksheet|[PostWorksheetShape](https://apireference.aspose.cloud/cells/#/Shapes/PostWorksheetShape)|
### **cURL Example**
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X POST "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes/0?folder=Temp" -H "accept: application/json" -H "Content-Type: application/json" -H "x-aspose-client: Containerize.Swagger" -d "{ \"link\": { \"Href\": \"string\", \"Rel\": \"string\", \"Title\": \"string\", \"Type\": \"string\" }, \"Name\": \"string\", \"MsoDrawingType\": \"string\", \"AutoShapeType\": \"string\", \"Placement\": \"string\", \"UpperLeftRow\": 0, \"Top\": 0, \"UpperLeftColumn\": 0, \"Left\": 0, \"LowerRightRow\": 0, \"Bottom\": 0, \"LowerRightColumn\": 10, \"Right\": 0, \"Width\": 0, \"Height\": 0, \"X\": 0, \"Y\": 0, \"RotationAngle\": 0, \"HtmlText\": \"string\", \"Text\": \"string\", \"AlternativeText\": \"string\", \"TextHorizontalAlignment\": \"string\", \"TextHorizontalOverflow\": \"string\", \"TextOrientationType\": \"string\", \"TextVerticalAlignment\": \"string\", \"TextVerticalOverflow\": \"string\", \"IsGroup\": true, \"IsHidden\": true, \"IsLockAspectRatio\": true, \"IsLocked\": true, \"IsPrintable\": true, \"IsTextWrapped\": true, \"IsWordArt\": true, \"LinkedCell\": \"string\", \"ZOrderPosition\": 0, \"Font\": { \"Color\": { \"A\": 0, \"R\": 0, \"G\": 0, \"B\": 0 }, \"DoubleSize\": 0, \"IsBold\": true, \"IsItalic\": true, \"IsStrikeout\": true, \"IsSubscript\": true, \"IsSuperscript\": true, \"Name\": \"string\", \"Size\": 0, \"Underline\": \"string\" }, \"Hyperlink\": \"string\"}"

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
{{< tabs tabTotal="5" tabID="4" tabName1="C#" tabName2="Java" tabName3="Perl" tabName4="Go" tabName5="Swift" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "1e994f29ef29e752b6d02a2c5b63ea9b" "Example-PostWorksheetShape.cs">}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "af3fea45644d431483f6df52cf3bfe26" "Example-PostWorksheetShape.java">}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "7effbad588b0c24b5f8ed2d7c7759b72" "Example-PostWorksheetShape.pl">}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cloud" "f97be54c9a1c7fd47eb5d294c66476fb" "Example-PostWorksheetShape.go">}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "f342d1e6f85982e0429fcd9bed8b11a8" "Example-PostWorksheetShape.swift">}}

{{< /tab >}}

{{< /tabs >}}
