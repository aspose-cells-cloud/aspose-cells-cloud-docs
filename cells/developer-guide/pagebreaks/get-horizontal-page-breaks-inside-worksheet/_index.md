---
title: "Get Horizontal Page Breaks inside Worksheet"
type: docs
url: /get-horizontal-page-breaks-inside-worksheet/
weight: 10
---

## **Introduction**
This example shows how to get Horizontal Page Breaks inside Worksheet using Aspose.Cells Cloud API. You can use our REST API with any language: .NET, Java, PHP, Ruby, Rails, Python, jQuery and many more.
## **API Information**

|**API**|**Type**|**Description**|**Resource Link**|
| :- | :- | :- | :- |
|/cells/{name}/worksheets/{sheetName}/horizontalpagebreaks|GET|Get horizontal page breaks descripton in worksheet|[GetHorizontalPageBreaks](https://apireference.aspose.cloud/cells/#/PageBreaks/GetHorizontalPageBreaks)|
### **cURL Example**
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X GET "http://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/horizontalpagebreaks" -H "Content-Type: application/json" -H "Accept: application/json"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{

  "HorizontalPageBreaks": {

    "HorizontalPageBreakList": [

      {

        "Row": 6,

        "EndColumn": 16383,

        "StartColumn": 0

      }

    ],

    "link": {

      "Href": "http://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/HorizontalPageBreaks",

      "Rel": "self",

      "Title": null,

      "Type": null

    }

  },

  "Code": 200,

  "Status": "OK"

}

```

{{< /tab >}}

{{< /tabs >}}
## **SDK Source**
The Aspose.Cells Cloud SDKs can be downloaded from the following page: [Available SDKs](/cells/available-sdks/)
### **SDK Examples**
{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="Go" tabName3="Swift" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "036a802d3567e6f9f4600a2ffed6044e" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "0b12bf6e926b544dab3a9f6da53208aa" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "4cba8faa56ffe9e4e73f1b2686c3917b" >}}

{{< /tab >}}

{{< /tabs >}}
