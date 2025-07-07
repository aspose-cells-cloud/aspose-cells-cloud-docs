---
title: "Batch Split"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /batch/split
keywords: "Batch split Excel file."
description: "Aspose.Cells Cloud API supports batch split file. SDK support kinds of development languages. They include Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby, and swift."
weight: 100
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdown, Batch Split
---

This REST API indicates to `batch split` of eligible file.

## RSET API

```bash
 
POST http://api.aspose.cloud/v3.0/cells/batch/split
 
```

The request parameters are:

| Parameter Name | Type | Path/Query String/HTTPBody | Description|
| :- | :- | :- |:- |
| BatchSplitRequest  |  | body |   |

**BatchSplitRequest  Properties**

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
 SourceFolder | string |  | [optional]
 SourceStorage | string |  | [optional]
 MatchCondition | MatchConditionRequest |  | [optional]
 Format | string |  | [optional]
 FromIndex | integer |  | [optional]
 ToIndex | integer |  | [optional]
 OutFolder | string |  | [optional]
 SaveOptions | SaveOptions |  | [optional]

**MatchConditionRequest Properties**

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
 RegexPattern | string |  | [optional]
 FullMatchConditions | string[] |  | [optional]

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/Batch/PostBatchSplit) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use cURL command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/batch/split" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Format\":\"pdf\"}" 
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```bash
{
"Code": 200,
"Status": "OK"
}
 
```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK Family

Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your split tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js"  tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}
{{< /tab >}}

{{< /tabs >}}
