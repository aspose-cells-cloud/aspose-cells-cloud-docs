---
title: "Insert Vertical Page Break inside Worksheet"
type: docs
url: /insert-vertical-page-break-inside-worksheet/
weight: 40
---

## **Introduction**
This example shows how to insert Vertical Page Break inside Worksheet using Aspose.Cells Cloud API. You can use our REST API with any language: .NET, Java, PHP, Ruby, Rails, Python, jQuery and many more.
## **API Information**

|**API**|**Type**|**Description**|**Resource Link**|
| :- | :- | :- | :- |
|/cells/{name}/worksheets/{sheetName}/verticalpagebreaks|PUT|Adds a vertical page break in worksheet|[PutVerticalPageBreak](https://apireference.aspose.cloud/cells/#/PageBreaks/PutVerticalPageBreak)|
### **cURL Example**
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X PUT "http://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/verticalpagebreaks?column=9" -H "Content-Type: application/json" -H "Accept: application/json"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{"Code":200,"Status":"OK"}

```

{{< /tab >}}

{{< /tabs >}}
## **SDK Source**
The Aspose.Cells Cloud SDKs can be downloaded from the following page: [Available SDKs](/cells/available-sdks/)
### **SDK Examples**
{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="Go" tabName3="Swift" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "8e0013eccb00b60938aa0c9bc930625b" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "e36b456e3be3e3778f1aa4af7c1bd0d6" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "628d11a1e75ec9e9e28c9ce33bcc775b" >}}

{{< /tab >}}

{{< /tabs >}}
