---
title: "Batch Lock"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /batch/lock
keywords: "Batch lock of multiple Excel files."
description: "Aspose.Cells Cloud API supports batch lock of multiple excel files. SDK support kinds of development languages. They include Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby, and swift."
weight: 100
---

This REST API indicates to `batch lock` of eligible files.
 
## RSET API
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/batch/lock
 
```
The request parameters are: 
 
| Parameter Name | Type | Path/Query String/HTTPBody | Description| 
| :- | :- | :- |:- | 
| BatchLockRequest  |  | body |   |

**BatchLockRequest  Properties**
 
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
 SourceFolder | string |  | [optional] 
 MatchCondition | MatchConditionRequest |  | [optional] 
 Password | string |  | [optional] 
 OutFolder | string |  | [optional] 

**MatchConditionRequest Properties**
 
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
 RegexPattern | string |  | [optional] 
 FullMatchConditions | string[] |  | [optional] 

 
The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/Batch/PostBatchLock) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.
 
You can use cURL command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL.
 
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}
 
{{< tab tabNum="11" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/batch/lock" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Password\":\"123456\"}" 
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
 
Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your lock tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.
 
The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:
 
 
  
{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

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

{{< tab tabNum="10" >}}


{{< /tab >}}

{{< /tabs >}}

