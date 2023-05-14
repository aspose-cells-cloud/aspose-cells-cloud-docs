---
title: Add horizontal page brea
second_title: Aspose.Cells Cloud Documen
linktitle: Add horizontal page brea
type: docs
url: /ar/page-breaks/add-horizontal-page-break/
aliases: [/insert-horizontal-page-break-inside-worksheet/]
keywords: Add a page break in an Excel worksheet
description: Aspose.Cells Cloud REST API support adding a page break in an Excel worksheet. SDK support kinds of development languages. They include Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby, and swift
weight: 30
---
This REST API indicates to insert `vertical` page break.
 
## RSET API
 
```bash
 
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/horizontalpagebreaks
 
```
The request parameters are: 
 
|Parameter Name |Type |Path/Query String/HTTPBody |Description|
|:- |:- |:- |:- |
|name |string |path ||
|sheetName |string |path ||
|cellname |string |query ||
|row |integer |query ||
|column |integer |query ||
|startColumn |integer |query ||
|endColumn |integer |query ||
|folder |string |query ||
|storageName |string |query |storage name. |
 
The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/PageBreaks/PutHorizontalPageBreak) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.
 
You can use cURL command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/horizontalpagebreaks?row=18" \
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

{{< gist "aspose-cells-cloud-gists" "0742361abdbe07508ef0054a3b8a0bb4" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "2462937944298a09a75b64f4c34889b7" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "e82a5628425ae5f59cd211c579b30073" >}}

{{< /tab >}}

{{< /tabs >}}
