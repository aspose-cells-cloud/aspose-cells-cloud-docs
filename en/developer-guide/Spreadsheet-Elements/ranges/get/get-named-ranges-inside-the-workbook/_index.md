---
title: "Get Named Ranges on an Excel workbook"
second_title: "Aspose.Cells Cloud Document"
linktitle: "Name"
type: docs
url: /ranges/get/name/
aliases: [/get-named-ranges-inside-the-workbook/]
keywords: "Get cells data based on named range on an Excel worksheet."
description: "Aspose.Cells Cloud REST API support getting cells data based on named range on an Excel worksheet. SDK support kinds of development languages. They include Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby, and swift."
weight: 10
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdown, Get Named Ranges on an Excel workbook
---
This REST API indicates Read worksheets ranges info.
 
## RSET API
 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/ranges
 
```
The request parameters are: 
 
| Parameter Name | Type | Path/Query String/HTTPBody | Description| 
| :- | :- | :- |:- | 
| name | string | path | Document name. |
| folder | string | query | Document folder. |
| storageName | string | query | storage name. |
 
The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/GetNamedRanges) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.
 
You can use cURL command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/ranges" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}}
 
{{< tab tabNum="2" >}}
 
```bash
{

  "Ranges": {

    "RangeList": [

      {

        "ColumnCount": 7,

        "ColumnWidth": 8.428571428571429,

        "FirstColumn": 1,

        "FirstRow": 9,

        "Name": "data",

        "RefersTo": "=Sheet1!$B$10:$H$10",

        "RowCount": 1,

        "RowHeight": 15,

        "Worksheet": "Sheet1"

      }

    ]

  },

  "Code": 200,

  "Status": "OK"

}
 
```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## Cloud SDK Family
 
Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.
 
The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:
 
 
{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="Ruby" tabName3="Go" >}}

{{< tab tabNum="1" >}}



{{< /tab >}}

{{< tab tabNum="2" >}}



{{< /tab >}}

{{< tab tabNum="3" >}}



{{< gist "aspose-cells-cloud-gists" "c75da9aa06645e27e899a9fb6cdc134c" >}}

{{< /tab >}}

{{< /tabs >}}
