---
title: "AutoFit Single Column of Worksheet"
type: docs
url: /autofit-single-column-of-worksheet/
weight: 10
---

## **Introduction**
This example shows how to autofit single column of the worksheet using Aspose.Cells Cloud API in your applications. You can use our REST API with any language: .NET, Java, PHP, Ruby, Rails, Python, jQuery and many more.
## **API Information**

|**API**|**Type**|**Description**|**Resource Link**|
| :- | :- | :- | :- |
|/cells/{name}/worksheets/{sheetName}/autofitcolumns|POST|Autofit columns in worksheet|[PostAutofitWorksheetColumns](https://apireference.aspose.cloud/cells/#/Worksheets/PostAutofitWorksheetColumns)|
### **cURL Example**
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X POST "http://api.aspose.cloud/v3.0/cells/sampleAutoFit.xlsx/worksheets/Sheet1/autofitcolumns?lastColumn=2&firstColumn=2" -d '{"AutoFitMergedCells" : true, "IgnoreHidden" : true, "OnlyAuto" : true}' -H "Content-Type: application/json" -H "Accept: application/json"

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

{{< gist "aspose-cloud" "9b4ccf2e3ba7d0f1d2a625d6cd40d2fd" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "3f17376a8d99f16f703fdb52c08a05ff" >}}

{{< /tab >}}

{{< /tabs >}}




