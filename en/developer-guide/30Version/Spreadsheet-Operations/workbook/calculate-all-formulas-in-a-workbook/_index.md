---
title: "Calculate all formulas on an Excel workbook"
second_title: "Document"
linktitle: "Calculate"
type: docs
url: /calculate-all-formulas-on-an-excel-file/
aliases: [/calculate-all-formulas-in-a-workbook/,/workbook/calculate-all-formulas/]
keywords: "calculate formulas, Excel workbook, Aspose.Cells Cloud, REST API, spreadsheet calculation"
description: "Use Aspose.Cells Cloud REST API to calculate all formulas in an Excel workbook. Supports multiple SDKs for languages such as C#, Java, Python, Node.js, and more."
weight: 140
---

This REST API calculates **all formulas** in an Excel workbook.

## REST API

```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/calculateformula
 
```

The request parameters are:

| Parameter Name | Type                | Location | Description                                                                                     |
|----------------|---------------------|----------|-------------------------------------------------------------------------------------------------|
| name           | string              | path     | Name of the workbook file.                                                                      |
| options        | CalculationOptions  | body     | JSON object that specifies calculation settings (e.g., `CalcStackSize`, `IgnoreError`).       |
| ignoreError    | boolean             | query    | When `true`, errors encountered during calculation are ignored.                                |
| folder         | string              | query    | Path to the folder that contains the workbook.                                                  |
| storageName    | string              | query    | Name of the storage service where the workbook is stored.                                      |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbookCalculateFormula) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make a call to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
 
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/calculateformula?ignoreError=true" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"\
-d "{ \"CalcStackSize\": 1, \"IgnoreError\": true, \"PrecisionStrategy\": \"string\", \"Recursive\": true}" 
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

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorkbookCalculateFormula.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorkbookCalculateFormula.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorkbookCalculateFormula.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorkbookCalculateFormula.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorkbookCalculateFormula.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorkbookCalculateFormula.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorkbookCalculateFormula.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorkbookCalculateFormula.go" >}}

{{< /tab >}}

{{< /tabs >}}
