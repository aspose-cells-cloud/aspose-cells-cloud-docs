---
title: "Update style for pivot table"
second_title: "Aspose.Cells Cloud Document"
linktitle: Format all
type: docs
url: /pivot-tables/format-all/
aliases: [/update-style-for-pivot-table/]
keywords: "Update all cell style for a pivot table."
description: "Aspose.Cells Cloud REST API support updating all cell style for a pivot table. SDK support kinds of development languages. They include Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby, and swift."
weight: 100
---

This REST API indicates `update` style for pivot table
 
## RSET API
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/FormatAll
 
```
The request parameters are: 
 
| Parameter Name | Type | Path/Query String/HTTPBody | Description| 
| :- | :- | :- |:- | 
| name | string | path | Document name. |
| sheetName | string | path | The worksheet name. |
| pivotTableIndex | integer | path | Pivot table index |
| style |  | body | Style dto in request body. |
| needReCalculate | boolean | query | False |
| folder | string | query | Document's folder. |
| storageName | string | query | storage name. |
 
The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/PivotTables/PostPivotTableStyle) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.
 
You can use cURL command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "http://api.aspose.com/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0/FormatAll" \
-X POST \
-d '{"Font":{"Name":"Arial", "Size":10}}'
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
 
 
 
{{< tabs tabTotal="1" tabID="4" tabName1="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "0b2caae7acfa3e947b856c07b6e8633a" >}}

{{< /tab >}}

{{< /tabs >}}
