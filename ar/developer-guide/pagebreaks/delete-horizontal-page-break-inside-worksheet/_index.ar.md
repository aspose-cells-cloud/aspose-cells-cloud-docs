---
title: Delete horizontal page brea
second_title: Aspose.Cells Cloud Documen
linktitle: Delete horizontal page brea
type: docs
url: /ar/page-breaks/delete-horizontal-page-break/
aliases: [/delete-horizontal-page-break-inside-worksheet/]
keywords: Delete a page break in an Excel worksheet
description: Aspose.Cells Cloud REST API support deleting a page break in an Excel worksheet. SDK support kinds of development languages. They include Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby, and swift
weight: 50
---
This REST API indicates to delete a `horizontal` page break. 
 
## RSET API
 
```bash
 
DELETE http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/horizontalpagebreaks/{index}
 
```
The request parameters are: 
 
|Parameter Name |Type |Path/Query String/HTTPBody |Description|
|:- |:- |:- |:- |
|name |string |path ||
|sheetName |string |path ||
|index |integer |path ||
|folder |string |query ||
|storageName |string |query |storage name. |
 
The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/PageBreaks/DeleteHorizontalPageBreak) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.
 
You can use cURL command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet1/horizontalpagebreaks/0" \
-X DELETE \
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

{{< gist "aspose-cells-cloud-gists" "16a442c2c2fb97afac8bd89fbbdca563" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "8ec70b4733866d10eae5e5e8c687d3ca" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "0a767f9030525d7f9be51bf9c6342b7d" >}}

{{< /tab >}}

{{< /tabs >}}
