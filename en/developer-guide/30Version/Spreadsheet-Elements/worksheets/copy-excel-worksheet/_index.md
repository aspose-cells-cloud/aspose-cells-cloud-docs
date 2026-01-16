---
title: "Copies contents and formats from another worksheet."
second_title: "Document"
linktitle: "Copy"
type: docs
url: /worksheets/copy/
aliases: [/copy-excel-worksheet/]
keywords: "copy worksheet, Aspose.Cells, Excel, REST API, spreadsheet, cloud SDK"
description: "Use Aspose.Cells Cloud REST API to copy a worksheet and its formats to a new sheet within the same workbook. Supports multiple SDKs (C#, Java, PHP, Ruby, Node.js, Python, Perl, Go)."
weight: 20
---

This REST API copies a worksheet and its formats to a new sheet within the same workbook.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/copy
```

The request parameters are:

| Parameter Name   | Type   | Location                     | Description                                                                 |
|------------------|--------|------------------------------|-----------------------------------------------------------------------------|
| `name`           | string | path                         | The name of the workbook file.                                              |
| `sheetName`      | string | path                         | The name of the destination worksheet (the new sheet).                     |
| `sourceSheet`    | string | query                        | The name of the worksheet to be copied.                                     |
| `options`        | object | body                         | JSON object containing copy options (e.g., column width, formulas).       |
| `sourceWorkbook` | string | query                        | The name of the source workbook if it differs from the current workbook.   |
| `sourceFolder`   | string | query                        | The folder path where the source workbook is stored.                        |
| `folder`         | string | query                        | The folder path where the destination workbook will be saved.               |
| `storageName`    | string | query                        | The name of the storage service to use.                                     |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/PostCopyWorksheet) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/NewSheet/copy?sourceSheet=Sheet3X" \
-X POST \
-d '{ "ColumnCharacterWidth": true, "CopyInvalidFormulasAsValues": true, "CopyNames": true, "ExtendToAdjacentRange": true, "ReferToDestinationSheet": true, "ReferToSheetWithSameName": true}' \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
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

Using an SDK is the best way to speed up development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCopyWorksheet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCopyWorksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCopyWorksheet.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCopyWorksheet.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCopyWorksheet.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCopyWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCopyWorksheet.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCopyWorksheet.go" >}}

{{< /tab >}}

{{< /tabs >}}