---
title: "Insert Horizontal Page Break inside Worksheet"
type: docs
url: /insert-horizontal-page-break-inside-worksheet/
weight: 30
---

## **Introduction**
This example shows how to insert Horizontal Page Break inside Worksheet using Aspose.Cells Cloud API. You can use our REST API with any language: .NET, Java, PHP, Ruby, Rails, Python, jQuery and many more.
### **API Information**

|**API**|**Type**|**Description**|**Resource Link**|
| :- | :- | :- | :- |
|/cells/{name}/worksheets/{sheetName}/horizontalpagebreaks|PUT|Adds a horizontal page breaks in worksheet|[PutHorizontalPageBreak](https://apireference.aspose.cloud/cells/#/PageBreaks/PutHorizontalPageBreak)|
### **cURL Example**
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X PUT "http://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/horizontalpagebreaks?row=18" -H "Content-Type: application/json"-H "Accept: application/json"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{
  "Code":200,
  "Status":"OK"
}

```

{{< /tab >}}

{{< /tabs >}}
## **SDK Source**
The Aspose.Cells Cloud SDKs can be downloaded from the following page: [Available SDKs](/cells/available-sdks/)
### **SDK Examples**
{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="Go" tabName3="Swift" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "0742361abdbe07508ef0054a3b8a0bb4" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "2462937944298a09a75b64f4c34889b7" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "e82a5628425ae5f59cd211c579b30073" >}}

{{< /tab >}}

{{< /tabs >}}
