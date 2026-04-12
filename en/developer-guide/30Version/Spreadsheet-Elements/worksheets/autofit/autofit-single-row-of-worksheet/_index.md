---
title: "Autofit a row on an Excel worksheet"
second_title: "Document"
linktitle: "Row"
type: docs
url: /worksheets/autofit/row/
aliases: [/autofit-single-row-of-worksheet/]
description: "Learn how to use Aspose.Cells Cloud REST API to autofit a row in an Excel worksheet. Includes endpoint, parameters, authentication, error handling, cURL request, and SDK examples."
keywords: "autofit row, Aspose.Cells Cloud, Excel API, REST, worksheet, SDK"
weight: 30
---

This REST API **autofits a row** on an Excel worksheet.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autofitrow
```

### **Request parameters**

| Parameter Name    | Type    | Location | Description                                                                                                                                                                                                  |
| ----------------- | ------- | -------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| name              | string  | path     | The name of the Excel file.                                                                                                                                                                                  |
| sheetName         | string  | path     | The name of the worksheet.                                                                                                                                                                                   |
| rowIndex          | integer | query    | Zero‑based index of the row to autofit.                                                                                                                                                                      |
| firstColumn       | integer | query    | Index of the first column included in the operation.                                                                                                                                                         |
| lastColumn        | integer | query    | Index of the last column included in the operation.                                                                                                                                                          |
| autoFitterOptions | object  | body     | Object that controls the autofit behavior (e.g., whether to consider merged cells, wrap text, etc.). See [AutoFitterOptions](/cells/auto-fitter-options){:rel="noopener" title="Controls autofit behavior"}. |
| folder            | string  | query    | Folder where the file is stored.                                                                                                                                                                             |
| storageName       | string  | query    | Name of the storage.                                                                                                                                                                                         |

### Entity Definitions

| Entity              | Description                                                                              |
| ------------------- | ---------------------------------------------------------------------------------------- |
| `rowIndex`          | Zero‑based index of the target row.                                                      |
| `firstColumn`       | Starting column for the autofit operation.                                               |
| `lastColumn`        | Ending column for the autofit operation.                                                 |
| `autoFitterOptions` | Optional settings that influence how the row is autofit (merged cells, wrap text, etc.). |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/PostAutofitWorksheetRow) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The example below demonstrates how to call the API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleAutoFit.xlsx/worksheets/Sheet1/autofitrow?rowIndex=2&firstColumn=1&lastColumn=10" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

| Field  | Description                                |
| ------ | ------------------------------------------ |
| Code   | `200` – request succeeded.                 |
| Status | `"OK"` – the row was autofit successfully. |

{{< /tab >}}

{{< /tabs >}}

## Error Handling

The API returns standard HTTP status codes. Common error responses for this endpoint are:

| HTTP Code | Example Payload                                           | Meaning                                                                           |
| --------- | --------------------------------------------------------- | --------------------------------------------------------------------------------- |
| 400       | `{ "Code": 400, "Message": "Row index out of range." }`   | The supplied `rowIndex` does not exist in the worksheet.                          |
| 401       | `{ "Code": 401, "Message": "Invalid or expired token." }` | Authentication failed – check the JWT token and ensure the request is over HTTPS. |
| 404       | `{ "Code": 404, "Message": "File not found." }`           | The specified Excel file or worksheet cannot be located.                          |
| 500       | `{ "Code": 500, "Message": "Internal server error." }`    | An unexpected server‑side problem occurred.                                       |

## Cloud SDK Family

Using an SDK is the fastest way to develop. An SDK abstracts low‑level details, allowing you to focus on your business logic. See the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorksheetRow.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorksheetRow.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorksheetRow.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorksheetRow.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2c4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorksheetRow.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorksheetRow.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorksheetRow.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorksheetRow.go" >}}
{{< /tab >}}

{{< /tabs >}}
