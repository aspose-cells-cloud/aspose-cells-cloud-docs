---
title: "Add vertical page break"
second_title: "Aspose.Cells Cloud Document"
linktitle: "Add vertical page break"
type: docs
url: /page-breaks/add-vertical-page-break/
aliases: [/insert-vertical-page-break-inside-worksheet/]
keywords: "Add a page break in an Excel worksheet."
description: "Aspose.Cells Cloud REST API support adding a page break in an Excel worksheet. SDK support kinds of development languages. They include Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby, and swift."
weight: 40
---

This REST API indicates to insert vertical page break.
 
## RSET API
 
```bash
 
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/verticalpagebreaks
 
```
The request parameters are: 
 
| Parameter Name | Type | Path/Query String/HTTPBody | Description| 
| :- | :- | :- |:- | 
| name | string | path |   |
| sheetName | string | path |   |
| cellname | string | query |   |
| column | integer | query |   |
| row | integer | query |   |
| startRow | integer | query |   |
| endRow | integer | query |   |
| folder | string | query |   |
| storageName | string | query | storage name. |
 
The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/PageBreaks/PutVerticalPageBreak) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.
 
You can use cURL command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/verticalpagebreaks?column=9" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}}
 
{{< tab tabNum="2" >}}
 
```bash
{
"Code": 200,
"Status": "OK"
}
 
```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## Cloud SDK Family
 
Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.
 
The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:
 

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="Go" tabName3="Swift" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8e0013eccb00b60938aa0c9bc930625b" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "e36b456e3be3e3778f1aa4af7c1bd0d6" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "628d11a1e75ec9e9e28c9ce33bcc775b" >}}

{{< /tab >}}

{{< /tabs >}}
