---
title: "Add a top 10 items in an Excel worksheet"
second_title: "Aspose.Cells Cloud Document"
linktitle: "Add top 10 filter"
type: docs
url: /autofilter/add-top-10-filter/ 
aliases: [/filter-the-top-10-items-in-the-list/, /autofilter/add-a-top-10-filter/ ]
keywords: "Adds a top10 filter on an Excel worksheet."
description: "The Aspose.Cells Cloud API supports adding a top10 filter on an Excel worksheet.SDK support kinds of development languages. They include Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby, and swift."
weight: 65
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdown, Add a top 10 items in an Excel worksheet
---

This REST API indicates to filter the `top 10` item in the list

## RSET API

```bash
 
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/filterTop10
 
```

The request parameters are:

| Parameter Name | Type | Path/Query String/HTTPBody | Description|
| :- | :- | :- |:- |
| name | string | path |   |
| sheetName | string | path |   |
| range | string | query |   |
| fieldIndex | integer | query |   |
| isTop | boolean | query |   |
| isPercent | boolean | query |   |
| itemCount | integer | query |   |
| matchBlanks | boolean | query |   |
| refresh | boolean | query |   |
| folder | string | query |   |
| storageName | string | query | storage name. |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetFilterTop10) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use cURL command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```java

curl -v "http://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/filterTop10?range=A1:B1&fieldIndex=0&isTop=true&itemCount=1&isPercent=true&matchBlanks=true" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```java

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

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetFilterTop10.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetFilterTop10.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetFilterTop10.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetFilterTop10.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetFilterTop10.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetFilterTop10.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetFilterTop10.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetFilterTop10.go" >}}

{{< /tab >}}

{{< /tabs >}}
