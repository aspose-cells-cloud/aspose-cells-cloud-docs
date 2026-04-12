---
title: "Calculate Cell Formula"
type: docs
url: /calculate-cells-formula/
weight: 90
keywords: "Aspose.Cells Cloud, calculate cell formula, Excel API, REST, SDK"
description: "Learn how to calculate an Excel cell formula using Aspose.Cells Cloud REST API (v3.0). Includes endpoint, parameters, cURL request, response schema, and SDK examples in C#, Java, Python, and more."
---

This REST API calculates the **cell formula** in an Excel workbook.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}/calculate
```

### Request Parameters

| Parameter Name | Type   | Parameter location (path/query/body) | Description                                                          |
| -------------- | ------ | ------------------------------------ | -------------------------------------------------------------------- |
| name           | string | path                                 | Name of the Excel file (e.g., `Book1.xlsx`).                         |
| sheetName      | string | path                                 | Name of the worksheet that contains the cell.                        |
| cellName       | string | path                                 | Address of the cell to be calculated (e.g., `A1`).                   |
| options        | object | body                                 | JSON object with calculation options (see **Options object** table). |
| folder         | string | query                                | Folder in storage where the file is located.                         |
| storageName    | string | query                                | Name of the Aspose Cloud storage.                                    |

#### Options object

| Field         | Type    | Description                                                                    | Default |
| ------------- | ------- | ------------------------------------------------------------------------------ | ------- |
| CalcStackSize | string  | Maximum calculation stack size.                                                | `"1"`   |
| IgnoreError   | boolean | If `true`, calculation errors are ignored and the cell value is set to `#N/A`. | `false` |
| Recursive     | boolean | Enables recursive calculation of dependent cells.                              | `false` |
| Precision     | string  | Number of decimal places for numeric results.                                  | `"15"`  |
| UseThreading  | boolean | Enables multi‑threaded calculation.                                            | `false` |

### Request example (cURL)

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/cells/A1/calculate" \
  -d '{"CalcStackSize":"1"}' \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Value": 123.45,
  "Formula": "=SUM(B1:B5)",
  "IsError": false
}
```

{{< /tab >}}

{{< /tabs >}}

### Error handling

| HTTP Status | Code | Message                                                            | Example body                                                             |
| ----------- | ---- | ------------------------------------------------------------------ | ------------------------------------------------------------------------ |
| 400         | 4000 | Bad Request – missing or invalid parameters.                       | `{ "Code": 4000, "Message": "The parameter 'name' is required." }`       |
| 401         | 4010 | Unauthorized – invalid or expired JWT token.                       | `{ "Code": 4010, "Message": "Access token is invalid or has expired." }` |
| 404         | 4040 | Not Found – the specified file, worksheet, or cell does not exist. | `{ "Code": 4040, "Message": "File 'Book1.xlsx' not found." }`            |
| 500         | 5000 | Internal Server Error – unexpected server condition.               | `{ "Code": 5000, "Message": "An unexpected error occurred." }`           |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Cells/PostCellCalculate) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK abstracts low‑level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCellCalculate.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCellCalculate.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCellCalculate.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCellCalculate.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCellCalculate.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCellCalculate.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCellCalculate.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCellCalculate.go" >}}

{{< /tab >}}

{{< /tabs >}}
