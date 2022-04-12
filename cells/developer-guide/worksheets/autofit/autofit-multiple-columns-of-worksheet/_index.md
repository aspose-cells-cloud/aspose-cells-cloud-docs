---
title: "Autofit multiple columns on an Excel worksheet"
second_title: "Aspose.Cells Cloud Document"
linktitle: "Columns"
type: docs
url: /worksheets/autofit/columns/
aliases: [/autofit-multiple-columns-of-worksheet/]
keywords: "Autofit columns on an Excel workbook"
description: "Aspose.Cells Cloud REST API support autofitting columns on an Excel workbook. SDK support kinds of development languages. They include Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby, and swift."
weight: 20
---

This REST API indicates to autofit `multiple columns` on an Excel worksheet. 
 
## RSET API
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autofitcolumns
 
```
The request parameters are: 
 
| Parameter Name | Type | Path/Query String/HTTPBody | Description| 
| :- | :- | :- |:- | 
| name | string | path |   |
| sheetName | string | path |   |
| firstColumn | integer | query |   |
| lastColumn | integer | query |   |
| autoFitterOptions |  | body |   |
| firstRow | integer | query |   |
| lastRow | integer | query |   |
| folder | string | query |   |
| storageName | string | query | storage name. |
 
The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/PostAutofitWorksheetColumns) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.
 
You can use cURL command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/sampleAutoFit.xlsx/worksheets/Sheet1/autofitcolumns?lastColumn=5&firstColumn=0" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-d '{"AutoFitMergedCells" : true, "IgnoreHidden" : true, "OnlyAuto" : true}' 
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
 

{{< tabs tabTotal="2" tabID="4" tabName1="C#" tabName2="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "52437300ed7949d3375da7504b40c4dc" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "ca139ec2081abc8cfe870a4788b57e09" >}}

{{< /tab >}}

{{< /tabs >}}
