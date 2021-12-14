---
title: "Replace Text in a Worksheet"
type: docs
url: /replace-text-in-a-worksheet/
weight: 60
---

## **Introduction**
This example shows how to replace text in a Microsoft Excel Worksheet using Aspose.Cells Cloud API in your applications. You can use our REST API with any language: .NET, Java, PHP, Ruby, Rails, Python, jQuery and many more.

## **API Information**

|**API**|**Type**|**Description**|**Resource Link**|
| :- | :- | :- | :- |
|/cells/{name}/worksheets/{sheetName}/replaceText|POST|Replace Text in a Excel Worksheet|[PostWorsheetTextReplace](https://apireference.aspose.cloud/cells/#/Worksheets/PostWorsheetTextReplace)|
### **cURL Example**
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/replaceText?oldValue=b&newValue=b11" -H "accept: application/json"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{

  "Matches": 0,

  "Worksheet": {

    "link": {

      "Href": "/test.xlsx/worksheets/Sheet1",

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
{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "1e994f29ef29e752b6d02a2c5b63ea9b" "Examples-DotNET-CSharp-Text-ReplaceTextWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "af3fea45644d431483f6df52cf3bfe26" "Examples-Java-text-ReplaceTextWorksheet-replace-text-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "5c1a68c4cea73845b221ff0d3b9ec9df" "Examples-PHP-Text-PostWorsheetTextReplace-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cloud" "3c5c9f9fff9898bb8251aa7ee9191641" "Examples-Ruby-Worksheet-replace_text-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "5161752550311c9baf73ffa0a811ea0b" "ReplaceTextInWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cloud" "04e9dd952c704f334a4eceb3925d479e" "Examples-Node.js-SDK-Text-ReplaceTextWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cloud" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-text-ReplaceTextWorksheet-replace-text-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cloud" "7effbad588b0c24b5f8ed2d7c7759b72" "Examples-Perl-Text-ReplaceTextWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cloud" "ff17714a94632832ff5ae7d77ba511f6" >}}

{{< /tab >}}

{{< /tabs >}}
