---
title: "Calculate Cells formula"
type: docs
url: /calculate-cells-formula/
weight: 90
---

This REST API indicates calculate `cells formula` in an Excel file.

## RSET API
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}/calculate
 
```
The request parameters are: 
 
| Parameter Name | Type | Path/Query String/HTTPBody | Description| 
| :- | :- | :- |:- | 
| name | string | path |   |
| sheetName | string | path |   |
| cellName | string | path |   |
| options |  | body |   |
| folder | string | query |   |
| storageName | string | query | storage name. |
 
The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Cells/PostCellCalculate) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.
 
You can use cURL command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL.
 
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}
 
{{< tab tabNum="11" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/cells/A1/calculate" \
-d '{"CalcStackSize": "1"}' \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
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

Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="6" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" tabName4="Node.js" tabName5="Perl" tabName6="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "1e994f29ef29e752b6d02a2c5b63ea9b" "Examples-DotNet-CSharp-Cells-CalculateCellFormula-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "5c1a68c4cea73845b221ff0d3b9ec9df" "Examples-PHP-Cells-PostCalulateCellFormula-.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "" "53fb9eb3d3d0d6e836078d4677a51ab5" "Examples-Ruby-Cells-post_calulate_cell_formula-.rb" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cloud" "04e9dd952c704f334a4eceb3925d479e" "Examples-Node.js-SDK-Cells-CalculateCellFormula-1.js" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cloud" "7effbad588b0c24b5f8ed2d7c7759b72" "Examples-Perl-Cells-CalculateCellFormula-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cloud" "4774754e007cb84169337486da4cc374" >}}

{{< /tab >}}

{{< /tabs >}}
