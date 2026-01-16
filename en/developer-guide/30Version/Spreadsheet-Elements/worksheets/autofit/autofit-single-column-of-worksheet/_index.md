---
title: "Autofit a column on an Excel worksheet"
second_title: "Document"
linktitle: "Column"
type: docs
url: /worksheets/autofit/column/
aliases: [/autofit-single-column-of-worksheet/]
keywords: "Aspose.Cells Cloud, Excel autofit column, REST API, SDK, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go"
description: "The Aspose.Cells Cloud REST API enables you to autofit columns in an Excel worksheet. This guide shows how to invoke the API via HTTP, cURL, and the available SDKs (C#, Java, PHP, Ruby, Node.js, Python, Perl, Go)."
weight: 10
---

This REST API autofits a column (or a range of columns) on an Excel worksheet.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autofitcolumns
```

### Request parameters

| Parameter Name | Type    | Location                     | Description |
|----------------|---------|------------------------------|-------------|
| name           | string  | path                         | The name of the Excel file. |
| sheetName      | string  | path                         | The name of the worksheet. |
| firstColumn    | integer | query                        | Zero‑based index of the first column to autofit. |
| lastColumn     | integer | query                        | Zero‑based index of the last column to autofit. |
| autoFitterOptions | object | body                         | Options that control the autofit behavior (see [AutoFitterOptions](/cells/auto-filter-options)). |
| firstRow       | integer | query                        | Zero‑based index of the first row considered when calculating column width. |
| lastRow        | integer | query                        | Zero‑based index of the last row considered when calculating column width. |
| folder         | string  | query                        | The folder in storage where the file is located. |
| storageName    | string  | query                        | The name of the storage service. |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/PostAutofitWorksheetColumns) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the **cURL** command‑line tool to call Aspose.Cells Cloud services. The example below demonstrates how to invoke the autofit‑column endpoint.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/sampleAutoFit.xlsx/worksheets/Sheet1/autofitcolumns?firstColumn=2&lastColumn=2" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"AutoFitMergedCells": true, "IgnoreHidden": true, "OnlyAuto": true}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK Family

Using an SDK is the fastest way to integrate the API into your application. SDKs handle low‑level details so you can focus on business logic. See the [GitHub repository](https://github.com/aspose-cells-cloud) for the complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call the autofit‑column endpoint with various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}