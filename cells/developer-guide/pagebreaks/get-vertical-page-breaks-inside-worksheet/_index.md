---
title: "Get Vertical Page Breaks inside Worksheet"
type: docs
url: /get-vertical-page-breaks-inside-worksheet/
weight: 20
---

## **Introduction**
This example shows how to get Vertical Page Breaks inside Worksheet using Aspose.Cells Cloud API. You can use our REST API with any language: .NET, Java, PHP, Ruby, Rails, Python, jQuery and many more.
## **API Information**

|**API**|**Type**|**Description**|**Resource Link**|
| :- | :- | :- | :- |
|/cells/{name}/worksheets/{sheetName}/verticalpagebreaks|GET|Get vertical page breaks description in worksheet|[GetVerticalPageBreaks](https://apireference.aspose.cloud/cells/#/PageBreaks/GetVerticalPageBreaks)|
### **cURL Example**
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X GET "http://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/verticalpagebreaks" -H "Content-Type: application/json" -H "Accept: application/json"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{

  "VerticalPageBreaks": {

    "VerticalPageBreakList": [

      {

        "Column": 3,

        "EndRow": 1048575,

        "StartRow": 0

      }

    ],

    "link": {

      "Href": "http://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/VerticalPageBreaks",

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

{{< gist "aspose-cloud" "537a7b794adab07f9ca929cf2c6f131a" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "34317a3fb628d9c3cd433f78b42bddc3" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "399b8d96afaffb51a07730c498e6eaf2" >}}

{{< /tab >}}

{{< /tabs >}}
