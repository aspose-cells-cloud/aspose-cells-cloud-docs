---
title: "How to Merge Cells in an Excel Worksheet – Aspose.Cells Cloud API (v3.0)"
date: 2024-03-15T10:00:00Z
lastmod: 2024-05-20T14:30:00Z
draft: false
tags: ["excel", "cells-merge", "rest-api", "cloud", "aspose.cells", "worksheet"]
categories: ["aspose.cells-cloud", "tutorials"]
description: "Step-by-step guide to merge cells in Excel worksheets using Aspose.Cells Cloud REST API, with cURL and SDK examples (C#, Java, Python, Node.js, PHP, Ruby, Perl, Go)."
keywords: "merge cells, Excel, Aspose.Cells Cloud, REST API, v3.0, worksheet merge, cURL, SDK"
canonical: "https://docs.aspose.cloud/cells/merge-cells-in-excel-worksheet/"
weight: 110
---

The **PostWorksheetMerge** API (`POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/merge`) enables developers to merge a rectangular block of cells into a single cell spanning specified rows and columns in an Excel worksheet via Aspose.Cells Cloud, supporting tasks like formatting reports and dashboards by combining multiple cells into one unified, larger cell.

> **Note**: This guide applies to Aspose.Cells Cloud API v3.0 (released March 2024). For v2.0, see [Legacy Merge Documentation](/docs/cells/merge-cells-v2/).

## The Post Worksheet Merge Web API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/merge
```

### Security and Authentication

The Aspose.Cells Cloud APIs use [JWT token-based authentication](/docs/total/getting-started/authentication/). Ensure your requests include a valid `Authorization: Bearer <token>` header.

### Request Parameters

| Parameter Name | Type    | Path/Query String/HTTPBody | Description                                  |
| -------------- | ------- | -------------------------- | -------------------------------------------- |
| name           | String  | Path                       | The file name.                               |
| sheetName      | String  | Path                       | The worksheet name.                          |
| startRow       | Integer | Query                      | The start row index.                         |
| startColumn    | Integer | Query                      | The start column index.                      |
| totalRows      | Integer | Query                      | The total rows number.                       |
| totalColumns   | Integer | Query                      | The total columns number.                    |
| folder         | String  | Query                      | The folder where the file is situated.       |
| storageName    | String  | Query                      | The storage name where the file is situated. |

### Response

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

Returns a `CellsCloudResponse` object.

### HTTP Status Codes

| Code | Meaning               | Description                                                 |
| ---- | --------------------- | ----------------------------------------------------------- |
| 200  | OK                    | Merge operation completed successfully.                     |
| 400  | Bad Request           | Missing or invalid parameters (e.g., out-of-range indices). |
| 401  | Unauthorized          | Invalid or missing JWT token.                               |
| 413  | Payload Too Large     | Request exceeds size limits (not applicable here).          |
| 500  | Internal Server Error | Unexpected server-side failure.                             |

## How to Use the Post Worksheet Merge API with SDKs?

### Post Worksheet Merge API Specification

The <a href="https://reference.aspose.cloud/cells/#/Cells/PostWorksheetMerge" rel="noopener noreferrer">Post Worksheet Merge API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

### cURL Example

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/merge?startRow=10&startColumn=10&totalRows=2&totalColumns=3" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your JWT token>"
```

#### Expected Response

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetMerge.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetMerge.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetMerge.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetMerge.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetMerge.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetMerge.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetMerge.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetMerge.go" >}}
{{</tab>}}
{{< /tabs >}}
