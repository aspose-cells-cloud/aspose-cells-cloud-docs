---
title: "Unhide columns on an Excel worksheet"
second_title: "Document"
linktitle: "Unhide"
type: docs
url: /columns/unhide/
aliases: [/unhide-columns-in-an-excel-worksheet/,/unhide-columns-in-excel-worksheet/]
keywords: "unhide columns, Excel, Aspose.Cells Cloud, REST API, SDK, worksheet, API"
description: "Learn how to use the Aspose.Cells Cloud REST API to unhide columns in an Excel worksheet. Includes request details, a cURL example, and SDK code samples for several programming languages."
weight: 50
---

This REST API unhides worksheet columns.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/unhide
```

The request parameters are:

| Parameter Name | Type    | Location | Description                                            |
|----------------|---------|----------|--------------------------------------------------------|
| name           | string  | path     | The workbook name.                                     |
| sheetName      | string  | path     | The worksheet name.                                    |
| startColumn    | integer | query    | The index of the first column to be processed.        |
| totalColumns   | integer | query    | The number of columns to be processed.                |
| width          | number  | query    | Desired column width (default = 50.0).                |
| folder         | string  | query    | The folder that contains the document.                |
| storageName    | string  | query    | The name of the storage service.                      |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Cells/PostUnhideWorksheetColumns) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the **cURL** command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/unhide?startColumn=1&totalColumns=1&width=15" -H "accept: application/json"
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

Using an SDK is the best way to speed up development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUnhideWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUnhideWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUnhideWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUnhideWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUnhideWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUnhideWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUnhideWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUnhideWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}