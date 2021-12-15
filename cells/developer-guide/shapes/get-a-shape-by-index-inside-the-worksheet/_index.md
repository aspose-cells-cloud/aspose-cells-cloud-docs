---
title: "Get a Shape by Index inside the Worksheet"
type: docs
url: /get-a-shape-by-index-inside-the-worksheet/
weight: 20
---

## **Introduction**
This example shows how to get a shape by index inside the worksheet, using Aspose.Cells Cloud API in your applications. You can use our REST API with any language: .NET, Java, PHP, Ruby, Rails, Python, jQuery and many more.
## **API Information**

|**API**|**Type**|**Description**|**Resource Link**|
| :- | :- | :- | :- |
|/cells/{name}/worksheets/{sheetName}/shapes/{shapeindex}|GET|Get a shape description in worksheet|[GetWorksheetShape](https://apireference.aspose.cloud/cells/#/Shapes/GetWorksheetShape)|
### **cURL Example**
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X GET "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes/0" -H "accept: application/json" 
-H "x-aspose-client: Containerize.Swagger"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{

  "Status": "string",

  "Shape": {

    "link": {

      "Href": "string",

      "Rel": "string",

      "Title": "string",

      "Type": "string"

    },

    "Name": "string",

    "MsoDrawingType": "string",

    "AutoShapeType": "string",

    "Placement": "string",

    "UpperLeftRow": 0,

    "Top": 0,

    "UpperLeftColumn": 0,

    "Left": 0,

    "LowerRightRow": 0,

    "Bottom": 0,

    "LowerRightColumn": 0,

    "Right": 0,

    "Width": 0,

    "Height": 0,

    "X": 0,

    "Y": 0,

    "RotationAngle": 0,

    "HtmlText": "string",

    "Text": "string",

    "AlternativeText": "string",

    "TextHorizontalAlignment": "string",

    "TextHorizontalOverflow": "string",

    "TextOrientationType": "string",

    "TextVerticalAlignment": "string",

    "TextVerticalOverflow": "string",

    "IsGroup": true,

    "IsHidden": true,

    "IsLockAspectRatio": true,

    "IsLocked": true,

    "IsPrintable": true,

    "IsTextWrapped": true,

    "IsWordArt": true,

    "LinkedCell": "string",

    "ZOrderPosition": 0

  }

}

```

{{< /tab >}}

{{< /tabs >}}
## **SDK Source**
The Aspose.Cells Cloud SDKs can be downloaded from the following page: [Available SDKs](/cells/available-sdks/)
### **SDK Examples**
{{< tabs tabTotal="5" tabID="4" tabName1="C#" tabName2="Java" tabName3="Perl" tabName4="Go" tabName5="Swift" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-GetWorksheetShape.cs">}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example-GetWorksheetShape.java">}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example-GetWorksheetShape.pl">}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "dd6d8ac9aacd9be6085356c07dbbadd0" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "f342d1e6f85982e0429fcd9bed8b11a8" "Example-GetWorksheetShape.swift">}}

{{< /tab >}}

{{< /tabs >}}

