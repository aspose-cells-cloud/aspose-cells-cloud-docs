---
title: "AutoFit Multiple Rows of Worksheet"
type: docs
url: /autofit-multiple-rows-of-worksheet/
weight: 40
---

## **Introduction**
This example shows how to autofit multiple rows of the worksheet using Aspose.Cells Cloud API in your applications. You can use our REST API with any language: .NET, Java, PHP, Ruby, Rails, Python, jQuery and many more.
## **API Information**

|**API**|**Type**|**Description**|**Resource Link**|
| :- | :- | :- | :- |
|/cells/{name}/worksheets/{sheetName}/autofitrows|POST|Autofits rows in worksheet|[PostAutofitWorksheetRows](https://apireference.aspose.cloud/cells/#/Worksheets/PostAutofitWorksheetRows)|
### **cURL Example**
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X POST "http://api.aspose.cloud/v3.0/cells/sampleAutoFit.xlsx/worksheets/Sheet1/autofitcolumns?firstRow=1&lastColumn=10&lastRow=7&firstColumn=1" -d '{"AutoFitMergedCells" : true, "IgnoreHidden" : true, "OnlyAuto" : false}' -H "Content-Type: application/json" -H "Accept: application/json"

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

{{< gist "aspose-cloud" "094d1d9d2596d2bc485a9b1a056d901f" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "47291f603a163aa155e675f846e27ea2" >}}

{{< /tab >}}

{{< /tabs >}}




