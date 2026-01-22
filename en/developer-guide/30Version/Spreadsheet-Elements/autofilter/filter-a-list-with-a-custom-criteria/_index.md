---
title: "Add a custom criteria in an Excel worksheet"
second_title: "Document"
linktitle: "Add custom filter"
type: docs
url: /autofilter/add-custom-filter/
aliases: [/filter-a-list-with-a-custom-criteria/,/autofilter/add-a-custom-filter/]
keywords: "Excel, custom filter, Aspose.Cells Cloud, REST API, auto filter, worksheet"
description: "Learn how to use the Aspose.Cells Cloud REST API to add a custom filter to an Excel worksheet. Includes request details, cURL example, and SDK code snippets for multiple programming languages."
weight: 65
---

This REST API filters a list using a **custom criteria**.

## REST API

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/custom
```

The request parameters are:

| Parameter Name | Type    | Location                     | Description                                                                 |
|----------------|---------|------------------------------|-----------------------------------------------------------------------------|
| name           | string  | path                         | Name of the Excel file.                                                     |
| sheetName      | string  | path                         | Name of the worksheet that contains the data to be filtered.               |
| range          | string  | query                        | Cell range that the filter will be applied to (e.g., `A1:B1`).             |
| fieldIndex     | integer | query                        | Zero‑based index of the column on which the filter is applied.             |
| operatorType1  | string  | query                        | First comparison operator (e.g., `LessOrEqual`, `Equal`).                  |
| criteria1      | string  | query                        | First filter value or expression.                                          |
| isAnd          | boolean | query                        | If `true`, combines the two criteria with **AND**; otherwise **OR**.       |
| operatorType2  | string  | query                        | Second comparison operator (optional).                                     |
| criteria2      | string  | query                        | Second filter value or expression (optional).                              |
| matchBlanks    | boolean | query                        | When `true`, blanks are included in the filter results.                    |
| refresh        | boolean | query                        | If `true`, forces the worksheet to refresh after applying the filter.      |
| folder         | string  | query                        | Folder path in storage where the file is located.                          |
| storageName    | string  | query                        | Name of the storage service.                                                |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetCustomFilter) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the **cURL** command‑line tool to access Aspose.Cells web services easily. The following example shows how to make a call to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/custom?range=A1:B1&fieldIndex=0&operatorType1=LessOrEqual&criteria1=1" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK Family

Using an SDK is the fastest way to develop. An SDK handles low‑level details so you can focus on your project logic. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetCustomFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetCustomFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetCustomFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetCustomFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetCustomFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetCustomFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetCustomFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetCustomFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}