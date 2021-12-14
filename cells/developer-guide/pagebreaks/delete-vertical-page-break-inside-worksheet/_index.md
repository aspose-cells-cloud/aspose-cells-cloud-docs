---
title: "Delete Vertical Page Break inside Worksheet"
type: docs
url: /delete-vertical-page-break-inside-worksheet/
weight: 60
---

## **Introduction**
This example shows how to delete Vertical Page Break inside Worksheet using Aspose.Cells Cloud API. You can use our REST API with any language: .NET, Java, PHP, Ruby, Rails, Python, jQuery and many more.
## **API Information**

|**API**|**Type**|**Description**|**Resource Link**|
| :- | :- | :- | :- |
|/cells/{name}/worksheets/{sheetName}/verticalpagebreaks|DELETE|Delete vertical page breaks in worksheet|[DeleteVerticalPageBreaks](https://apireference.aspose.cloud/cells/#/PageBreaks/DeleteVerticalPageBreaks)|
### **cURL Example**
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X DELETE "http://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/verticalpagebreaks/0" -H "Content-Type: application/json" -H "Accept: application/json"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{

    Code = 200;

    Status = OK;

}

```

{{< /tab >}}

{{< /tabs >}}
## **SDK Source**
The Aspose.Cells Cloud SDKs can be downloaded from the following page: [Available SDKs](/cells/available-sdks/)
### **SDK Examples**
{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="Go" tabName3="Swift" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "c835cd32432e2cb4bd5951d616436c16" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "a458cdd89dd6d47330fbf1083d7be9b5" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "facec817b056ba33169de10a8a413317" >}}

{{< /tab >}}

{{< /tabs >}}
