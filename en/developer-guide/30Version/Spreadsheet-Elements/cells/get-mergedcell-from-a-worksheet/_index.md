---
title: "Get Merged Cells from Excel Worksheet – Aspose.Cells Cloud API"
date: 2024-03-15
lastmod: 2024-06-15
type: docs
url: /get-mergedcell-from-a-worksheet/
weight: 60
keywords: "Aspose.Cells Cloud, merged cells, Excel worksheet, REST API, Aspose.Cells SDK, Excel merged cells"
description: "Retrieve merged cell ranges from an Excel worksheet using Aspose.Cells Cloud API v3.0. Includes authentication, cURL examples, SDK code snippets in C#, Java, Python, and more."
---

## Overview

This API retrieves information about **merged cells** in a specified Excel worksheet. The returned data includes the positions and links to each merged cell range.

> **Note**: The API model uses the singular `MergedCell` for individual objects, while the collection is represented as `MergedCellList` in the response. The endpoint name and prose refer to the *concept* of merged cells (plural).

## REST API

### Endpoint

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/mergedCells
```

### Request Parameters

| Parameter     | Type   | Location | Required | Description                              |
|---------------|--------|----------|----------|------------------------------------------|
| `name`        | string | path     | ✅ Yes   | The Excel file name.                     |
| `sheetName`   | string | path     | ✅ Yes   | The worksheet name.                      |
| `folder`      | string | query    | ❌ No    | Folder where the file is located.        |
| `storageName` | string | query    | ❌ No    | Name of the storage to use.              |

### Authentication

All requests require [JWT token-based authentication](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/). Include the token in the `Authorization` header as a Bearer token.

## Response

Returns a `MergedCellsResponse` object.

### Example Response

```json
{
  "Code": 200,
  "Status": "OK",
  "MergedCells": {
    "Count": 1,
    "MergedCellList": [
      {
        "link": {
          "Href": "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/cells/mergedcells/0",
          "Rel": "self",
          "Type": "",
          "Title": ""
        }
      }
    ]
  }
}
```

### Response Schema

| Field             | Type     | Description                                  |
|-------------------|----------|----------------------------------------------|
| `Code`            | integer  | HTTP status code.                            |
| `Status`          | string   | Human-readable status message (e.g., `"OK"`). |
| `MergedCells.Count` | integer  | Total number of merged cells in the worksheet. |
| `MergedCells.MergedCellList` | array | Array of `MergedCell` objects, each containing a `link` to the merged cell resource. |

### HTTP Status Codes

| Code | Meaning              | Description                                      |
|------|----------------------|--------------------------------------------------|
| 200  | OK                   | Merged cells retrieved successfully.            |
| 400  | Bad Request          | Missing or invalid parameters (e.g., unsupported file type). |
| 401  | Unauthorized         | Invalid or missing JWT token.                   |
| 413  | Payload Too Large    | File size exceeds the service limit.            |
| 500  | Internal Server Error| Unexpected server error.                        |

## cURL Example

### Request

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/mergedCells" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your_jwt_token>"
```

### Response

```json
{
  "Code": 200,
  "Status": "OK",
  "MergedCells": {
    "Count": 1,
    "MergedCellList": [
      {
        "link": {
          "Href": "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/cells/mergedcells/0",
          "Rel": "self"
        }
      }
    ]
  }
}
```

## SDK Examples

Using an SDK simplifies integration by handling authentication, serialization, and error handling. The [Aspose.Cells-Cloud SDKs repository on GitHub](https://github.com/aspose-cells-cloud) provides open-source implementations.

### Quick Start Recommendation

| SDK   | Best For             |
|-------|----------------------|
| Python| Rapid prototyping    |
| C#    | .NET applications    |
| Java  | Enterprise systems   |
| Go    | Microservices        |

### C#

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetMergedCells.cs" >}}

### Java

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetMergedCells.java" >}}

### Python

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetMergedCells.py" >}}

### PHP

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetMergedCells.php" >}}

### Ruby

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetMergedCells.rb" >}}

### Node.js (TypeScript)

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetMergedCells.ts" >}}

### Perl

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetMergedCells.pl" >}}

### Go

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetMergedCells.go" >}}

## OpenAPI Specification

The official API reference is available at the [Aspose.Cells Cloud API Reference](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetMergedCells).

## Related Documentation

- [Set Merged Cells in Excel](/set-mergedcells-in-excel)  
- [List All Cells in a Worksheet](/list-cells-in-a-worksheet)  
- [Excel Worksheet Operations Overview](/worksheet-operations)

## Notes

- This API does not use visual diagrams; all operations are text-based.
- Ensure your JWT token has the required scopes (`cells.read` or `cells.write`) to access the endpoint.
- For large workbooks, consider pagination or filtering to improve performance.