---
title: "Autofit columns on an Excel file"
second_title: "Document"
linktitle: "Columns"
type: docs
url: /autofit-columns-on-an-excel-file/
aliases: [/auto-fit-columns-in-excel-workbooks,/autofit-columns-in-excel-workbooks/,/columns/autofit/,/workbook/autofit/columns/]
keywords: "Autofit columns, Excel, Aspose.Cells Cloud, REST API, SDK"
description: "Learn how to use Aspose.Cells Cloud REST API to autofit columns in an Excel workbook. Includes request details, cURL example, and SDK code samples for multiple languages."
weight: 90
---

This REST API supports autofitting columns in an Excel workbook.

## REST API

```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/autofitcolumns
 
```

The request parameters are:

| Parameter Name          | Type   | Location                     | Description                              |
|-------------------------|--------|------------------------------|------------------------------------------|
| **name**                | string | path                         | The name of the workbook file.           |
| **autoFitterOptions**   | object | body                         | Options that control the autofit behavior. |
| **startColumn**         | integer| query                        | Zero‑based index of the first column to autofit. |
| **endColumn**           | integer| query                        | Zero‑based index of the last column to autofit. |
| **folder**              | string | query                        | The folder that contains the workbook.   |
| **storageName**         | string | query                        | The name of the storage service.         |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Workbook/PostAutofitWorkbookColumns) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to easily access Aspose.Cells web services. The following example shows how to call the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "http://api.aspose.com/v3.0/cells/myWorkbook.xlsx/autofitcolumns" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-d '{"AutoFitMergedCells":true, "IgnoreHidden":true}'
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

Using an SDK is the most efficient way to accelerate development. An SDK handles low‑level details so you can focus on your project logic. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorkbookColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorkbookColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorkbookColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorkbookColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorkbookColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorkbookColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorkbookColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorkbookColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}
