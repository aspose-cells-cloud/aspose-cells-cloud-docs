---
title: "Import Data in Excel Worksheet without using Storage"
type: docs
url: /import-data-in-excel-worksheet-without-using-storage/
weight: 40
---

## **Introduction**
This example shows you how to import data from a text file into the worksheet. Both text file and import options are sent in API request body. You can use our REST API with any language: .NET, Java, PHP, Ruby, Rails, Python, jQuery and many more.
## **API Information**

|**API**|**Type**|**Description**|**Resource Link**|
| :- | :- | :- | :- |
|/cells/{name}/importdata|POST|Imports data into workbook|[PostImportData](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData)|
### **cURL Example**
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X POST "http://api.aspose.cloud/v3.0/cells/Book1.xlsx/importdata" -F 'json={"BatchData":null,"DestinationWorksheet":"Sheet1","IsInsert":false,"ImportDataType":"BatchData","Source":{"FileSourceType":1,"FilePath":"Batch_data_json.txt"}};type=application/json' -F "Batch_data_json.txt=@Batch_data_json.txt;type=text/json" -H "Content-Type: multipart/form-data" -H "Accept: application/json"

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
{{< tabs tabTotal="6" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" tabName4="Node.js" tabName5="Perl" tabName6="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "1e994f29ef29e752b6d02a2c5b63ea9b" "Examples-DotNet-CSharp-ImportData-postImportDataMultipartContent-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "5c1a68c4cea73845b221ff0d3b9ec9df" "Examples-PHP-Workbook-PostImportDataMultipartContent-.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "" "53fb9eb3d3d0d6e836078d4677a51ab5" "Examples-Ruby-Workbook-post_import_data_without_using_storage-.rb" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cloud" "04e9dd952c704f334a4eceb3925d479e" "Examples-Node.js-SDK-ImportData-postImportDataMultipartContent-1.js" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "7effbad588b0c24b5f8ed2d7c7759b72" "Examples-Perl-ImportData-postImportDataMultipartContent-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cloud" "0eff0430a2804c79c04ef7e8d75d1535" >}}

{{< /tab >}}

{{< /tabs >}}
