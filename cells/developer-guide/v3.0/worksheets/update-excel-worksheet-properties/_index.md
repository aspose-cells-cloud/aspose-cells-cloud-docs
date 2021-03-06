---
title: "Update Excel Worksheet Properties"
type: docs
url: /update-excel-worksheet-properties/
weight: 170
---

## **Introduction**
This example shows how to update properties of a worksheet using Aspose.Cells Cloud API in your applications. You can use our REST API with any language: .NET, Java, PHP, Ruby, Rails, Python, jQuery and many more.
## **API Information**

|**API**|**Type**|**Description**|**Resource Link**|
| :- | :- | :- | :- |
|/cells/{name}/worksheets/{sheetName}|POST|Update worksheet properties|[PostUpdateWorksheetProperty](https://apireference.aspose.cloud/cells/#/Worksheets/PostUpdateWorksheetProperty)|
### **cURL Example**
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X POST "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1" -H "accept: application/json" -H "Content-Type: application/json" -H "x-aspose-client: Containerize.Swagger" -d "{ \"Links\": [ { \"Href\": \"string\", \"Rel\": \"string\", \"Title\": \"string\", \"Type\": \"string\" } ], \"DisplayRightToLeft\": true, \"DisplayZeros\": true, \"FirstVisibleColumn\": 1, \"FirstVisibleRow\": 0, \"Name\": \"string\", \"Index\": 0, \"IsGridlinesVisible\": true, \"IsOutlineShown\": true, \"IsPageBreakPreview\": true, \"IsVisible\": true, \"IsProtected\": true, \"IsRowColumnHeadersVisible\": true, \"IsRulerVisible\": true, \"IsSelected\": true, \"TabColor\": { \"A\": 0, \"R\": 0, \"G\": 0, \"B\": 0 }, \"TransitionEntry\": true, \"TransitionEvaluation\": true, \"Type\": \"string\", \"ViewType\": \"string\", \"VisibilityType\": \"string\", \"Zoom\": 0, \"Cells\": { \"link\": { \"Href\": \"string\", \"Rel\": \"string\", \"Title\": \"string\", \"Type\": \"string\" } }, \"Charts\": { \"link\": { \"Href\": \"string\", \"Rel\": \"string\", \"Title\": \"string\", \"Type\": \"string\" } }, \"AutoShapes\": { \"link\": { \"Href\": \"string\", \"Rel\": \"string\", \"Title\": \"string\", \"Type\": \"string\" } }, \"OleObjects\": { \"link\": { \"Href\": \"string\", \"Rel\": \"string\", \"Title\": \"string\", \"Type\": \"string\" } }, \"Comments\": { \"link\": { \"Href\": \"string\", \"Rel\": \"string\", \"Title\": \"string\", \"Type\": \"string\" } }, \"Pictures\": { \"link\": { \"Href\": \"string\", \"Rel\": \"string\", \"Title\": \"string\", \"Type\": \"string\" } }, \"MergedCells\": { \"link\": { \"Href\": \"string\", \"Rel\": \"string\", \"Title\": \"string\", \"Type\": \"string\" } }, \"Validations\": { \"link\": { \"Href\": \"string\", \"Rel\": \"string\", \"Title\": \"string\", \"Type\": \"string\" } }, \"ConditionalFormattings\": { \"link\": { \"Href\": \"string\", \"Rel\": \"string\", \"Title\": \"string\", \"Type\": \"string\" } }, \"Hyperlinks\": { \"link\": { \"Href\": \"string\", \"Rel\": \"string\", \"Title\": \"string\", \"Type\": \"string\" } }}"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{
  "Status": "string",
  "Worksheet": {
    "Links": [
      {
        "Href": "string",
        "Rel": "string",
        "Title": "string",
        "Type": "string"
      }
    ],
    "DisplayRightToLeft": true,
    "DisplayZeros": true,
    "FirstVisibleColumn": 0,
    "FirstVisibleRow": 0,
    "Name": "string",
    "Index": 0,
    "IsGridlinesVisible": true,
    "IsOutlineShown": true,
    "IsPageBreakPreview": true,
    "IsVisible": true,
    "IsProtected": true,
    "IsRowColumnHeadersVisible": true,
    "IsRulerVisible": true,
    "IsSelected": true,
    "TabColor": {
      "A": 0,
      "R": 0,
      "G": 0,
      "B": 0
    },
    "TransitionEntry": true,
    "TransitionEvaluation": true,
    "Type": "string",
    "ViewType": "string",
    "VisibilityType": "string",
    "Zoom": 0,
    "Cells": {
      "link": {
        "Href": "string",
        "Rel": "string",
        "Title": "string",
        "Type": "string"
      }
    },
    "Charts": {
      "link": {
        "Href": "string",
        "Rel": "string",
        "Title": "string",
        "Type": "string"
      }
    },
    "AutoShapes": {
      "link": {
        "Href": "string",
        "Rel": "string",
        "Title": "string",
        "Type": "string"
      }
    },
    "OleObjects": {
      "link": {
        "Href": "string",
        "Rel": "string",
        "Title": "string",
        "Type": "string"
      }
    },
    "Comments": {
      "link": {
        "Href": "string",
        "Rel": "string",
        "Title": "string",
        "Type": "string"
      }
    },
    "Pictures": {
      "link": {
        "Href": "string",
        "Rel": "string",
        "Title": "string",
        "Type": "string"
      }
    },
    "MergedCells": {
      "link": {
        "Href": "string",
        "Rel": "string",
        "Title": "string",
        "Type": "string"
      }
    },
    "Validations": {
      "link": {
        "Href": "string",
        "Rel": "string",
        "Title": "string",
        "Type": "string"
      }
    },
    "ConditionalFormattings": {
      "link": {
        "Href": "string",
        "Rel": "string",
        "Title": "string",
        "Type": "string"
      }
    },
    "Hyperlinks": {
      "link": {
        "Href": "string",
        "Rel": "string",
        "Title": "string",
        "Type": "string"
      }
    }
  }
}
```

{{< /tab >}}

{{< /tabs >}}
## **SDK Source**
The Aspose.Cells Cloud SDKs can be downloaded from the following page: [Available SDKs](/cells/available-sdks/)
### **SDK Examples**
{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Objective C" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "" "f21c488545888fe78bbd97e47790246b" "Examples-.NET-CellsWorksheetsPostUpdateWorksheetProperty.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "af3fea45644d431483f6df52cf3bfe26" "Examples-Java-worksheet-UpdateWorksheetProperties-update-worksheet-properties.java" >}}


{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "5c1a68c4cea73845b221ff0d3b9ec9df" "Examples-PHP-Worksheet-PostUpdateWorksheetProperty-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cloud" "3c5c9f9fff9898bb8251aa7ee9191641" "Examples-Ruby-Worksheet-update_worksheet_property-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "04e9dd952c704f334a4eceb3925d479e" "Examples-Node.js-SDK-Worksheet-UpdateWorksheetProperties-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cloud" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-UpdateWorksheetProperties-update-worksheet-properties.java" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cloud" "7effbad588b0c24b5f8ed2d7c7759b72" "Examples-Perl-Worksheet-UpdateWorksheetProperties-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cloud" "ce38cb4feb118132fada7801c7f5cd43" >}}

{{< /tab >}}

{{< /tabs >}}
