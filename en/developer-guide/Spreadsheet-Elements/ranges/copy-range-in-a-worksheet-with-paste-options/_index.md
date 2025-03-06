---
title: "Copy Range in a Worksheet with Paste Options"
second_title: "Aspose.Cells Cloud Document"
linktitle: "Copy"
type: docs
url: /ranges/copy/
aliases: [/copy-range-in-a-worksheet-with-paste-options/]
keywords: "Copy a range in an Excel worksheet with paste options."
description: "Aspose.Cells Cloud REST API support copying a range in an Excel worksheet with paste options. SDK support kinds of development languages. They include Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby, and swift."
weight: 20
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdwon, Copy Range in a Worksheet with Paste Options
---

This REST API indicates to copy range in the worksheet on an Excel worksheet.
 
## RSET API
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges
 
```
The request parameters are: 
 
| Parameter Name | Type | Path/Query String/HTTPBody | Description| 
| :- | :- | :- |:- | 
| name | string | path | workbook name |
| sheetName | string | path | worksheet name |
| rangeOperate |  | body | copydata,copystyle,copyto,copyvalue |
| folder | string | query | Workbook folder. |
| storageName | string | query | storage name. |
 
The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRanges) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.
 
You can use cURL command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/ranges" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
-d "{ \"Operate\": \"string\", \"Source\": { \"ColumnCount\": 0, \"ColumnWidth\": 0, \"FirstColumn\": 0, \"FirstRow\": 0, \"Name\": \"string\", \"RefersTo\": \"string\", \"RowCount\": 0, \"RowHeight\": 0, \"Worksheet\": \"string\" }, \"Target\": { \"ColumnCount\": 0, \"ColumnWidth\": 0, \"FirstColumn\": 0, \"FirstRow\": 0, \"Name\": \"string\", \"RefersTo\": \"string\", \"RowCount\": 0, \"RowHeight\": 0, \"Worksheet\": \"string\" }, \"PasteOptions\": { \"OnlyVisibleCells\": true, \"PasteType\": \"string\", \"SkipBlanks\": true, \"Transpose\": true }}"

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

```csharp

string Client_Id = "Use your Client_Id";

string Client_Secret = "Use your Client_Secret";

//Copy Range in a Worksheet with Paste Options - URL

string url = "http://api.aspose.cloud/v3.0/cells/sampleRangeCopyTo.xlsx/worksheets/Sheet1/ranges";

//JSON - Part of Request Body

string strJson = "{ \"Operate\": \"copyto\", \"Source\": { \"ColumnCount\": 5, \"ColumnWidth\": 8.43, \"FirstColumn\": 1, \"FirstRow\": 0, \"RowCount\": 7, \"RowHeight\": 15, }, \"Target\": { \"ColumnCount\": 5, \"ColumnWidth\": 8.43, \"FirstColumn\": 10, \"FirstRow\": 20, \"RowCount\": 7, \"RowHeight\": 15, } , \"PasteOptions\": { \"OnlyVisibleCells\": true, \"PasteType\": \"All\", \"SkipBlanks\": true, \"Transpose\": false } }";

//Sign the URL

string surl = Sign(url, Client_Id, Client_Secret);

//Process Command - Post Signed URL with JSON body

using (Stream stream = ProcessCommand(surl, "Post", strJson, "json"))

{

	//Your code

}

```

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "4b9529b9d4238c301f3ee4855843874b" >}}

{{< /tab >}}

{{< /tabs >}}




