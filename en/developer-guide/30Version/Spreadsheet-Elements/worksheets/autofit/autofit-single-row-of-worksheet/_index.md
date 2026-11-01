---
title: "Autofit a row on an Excel worksheet"
second_title: "Developer Guide"
linktitle: "Row"
type: docs
url: /worksheets/autofit/row/
aliases: [/autofit-single-row-of-worksheet/]
description: "Learn how to use Aspose.Cells Cloud REST API to autofit a row in an Excel worksheet. Includes endpoint, parameters, authentication, error handling, cURL request, and SDK examples."
keywords: "autofit row, Aspose.Cells Cloud, Excel API, REST, worksheet, SDK, spreadsheet, cloud API"
weight: 30
ArticleTitle: "Autofit Row in Excel Worksheet using Aspose.Cells Cloud API"
---
The **PostAutofitWorksheetRow** API (`POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autofitrow`) in Aspose.Cells Cloud enables autofitting a single row in a worksheet by dynamically adjusting its height to accommodate the tallest content in the specified row, with optional parameters to limit the operation to a specific column range (`firstColumn`, `lastColumn`) and support for custom folder and storage locations; the operation requires the file name, worksheet name, and row index as mandatory path and query parameters.

## Security and Authentication

The Aspose.Cells Cloud APIs are secure and require [JWT token-based authentication](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## The Post Autofit Worksheet Row Web API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autofitrow
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer" target="_blank">JWT token-based authentication</a>.

### **Request parameters**

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| name | String | Path | The file name. |
| sheetName | String | Path | The worksheet name. |
| rowIndex | Integer | Query | The row index. |
| firstColumn | Integer | Query | The first column index. |
| lastColumn | Integer | Query | The last column index. |
| folder | String | Query | The folder where the file is situated. |
| storageName | String | Query | The storage name where the file is situated. |
| rowCount | Integer | Query | - |

**Sample `autoFitterOptions` JSON body**

```json
{
  "IsMergedCells": true,
  "IsWrapped": false,
  "AutoFitMergedCells": true,
  "AutoFitWrappedCells": false
}
```

### **Response**

```json
[
  {
    "Name": "CellsCloudResponse",
    "DataType": {
      "Identifier": "Class",
      "Reference": "CellsCloudResponse"
    }
  }
]
```

**Sample response headers**

```http
HTTP/1.1 200 OK
Content-Type: application/json
```

### Error Handling

The API returns standard HTTP status codes. Common error responses for this endpoint are:

| HTTP Code | Example Payload                                           | Meaning                                                                           |
| --------- | --------------------------------------------------------- | --------------------------------------------------------------------------------- |
| 400       | `{ "Code": 400, "Message": "Row index out of range." }`   | The supplied `rowIndex` does not exist in the worksheet.                          |
| 401       | `{ "Code": 401, "Message": "Invalid or expired token." }` | Authentication failed – check the JWT token and ensure the request is over HTTPS. |
| 404       | `{ "Code": 404, "Message": "File not found." }`           | The specified Excel file or worksheet cannot be located.                          |
| 500       | `{ "Code": 500, "Message": "Internal server error." }`    | An unexpected server‑side problem occurred.                                       |

### Entity Definitions

| Entity              | Description                                                                              |
| ------------------- | ---------------------------------------------------------------------------------------- |
| `rowIndex`          | Zero‑based index of the target row.                                                      |
| `firstColumn`       | Starting column for the autofit operation.                                               |
| `lastColumn`        | Ending column for the autofit operation.                                                 |
| `autoFitterOptions` | Optional settings that influence how the row is autofit (merged cells, wrap text, etc.). |

The [OpenAPI Specification](/cells/#/Worksheets/PostAutofitWorksheetRow) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

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

## Cloud SDK Family

Using an SDK is the fastest way to develop. An SDK abstracts low‑level details, allowing you to focus on your business logic. See the [GitHub repository](https://github.com/aspose-cells-cloud){:rel="noopener noreferrer"} for a complete list of Aspose.Cells Cloud SDKs.

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

**See also:** [Autofit column](/worksheets/autofit/column/), [Autofit rows](/worksheets/autofit/rows/), [AutoFitterOptions](/cells/auto-fitter-options).
