---
title: "AutoFit Single Row of Worksheet"
type: docs
url: /autofit-single-row-of-worksheet/
weight: 30
---

## **Introduction**
This example shows how to autofit single row of the worksheet using Aspose.Cells Cloud API in your applications. You can use our REST API with any language: .NET, Java, PHP, Ruby, Rails, Python, jQuery and many more.

## **API Information**

|**API**|**Type**|**Description**|**Resource Link**|
| :- | :- | :- | :- |
|/cells/{name}/worksheets/{sheetName}/autofitrow|POST|Autofits row in worksheet|[PostAutofitWorksheetRow](https://apireference.aspose.cloud/cells/#/Worksheets/PostAutofitWorksheetRow)|
### **cURL Example**
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X POST "http://api.aspose.cloud/v3.0/cells/sampleAutoFit.xlsx/worksheets/Sheet1/autofitcolumns?firstRow=2&lastColumn=10&lastRow=2&firstColumn=1" -d '{"AutoFitMergedCells" : true, "IgnoreHidden" : true, "OnlyAuto" : true}' -H "Content-Type: application/json" -H "Accept: application/json"

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
{{< tabs tabTotal="2" tabID="4" tabName1="C#" tabName2="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "5b27cb12deedc47e434c4d0bf70ef00b" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "4df97bb1460dcfa974cb04303e643583" >}}

{{< /tab >}}

{{< /tabs >}}
