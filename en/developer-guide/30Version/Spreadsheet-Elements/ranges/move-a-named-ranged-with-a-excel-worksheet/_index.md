---
title: "Move a named range with an Excel worksheet"
second_title: "Developer Guide"
linktitle: "Move"
type: docs
url: /ranges/move/
aliases: [/move-a-named-range-with-an-excel-worksheet/]
keywords: "Aspose.Cells Cloud, move named range, Excel worksheet, REST API, range move, SDK examples"
description: "Move a named range in an Excel worksheet via Aspose.Cells Cloud REST API v3.0 with JWT and SDK examples"
weight: 100
ArticleTitle: "Move a named range with an Excel worksheet using Aspose.Cells Cloud API"
---
The **PostWorksheetCellsRangeMoveTo** API (`POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/moveto`) enables programmatic relocation of a named range within a worksheet by specifying the source range in the request body and the destination row and column via query parameters. Using Aspose.Cells Cloud, developers can move ranges to new positions—such as adjusting layout after inserting or deleting rows/columns—while preserving formatting and formulas, supporting automation of dynamic spreadsheet reorganization tasks across Net, Java, Go, Node.js, and Python via SDKs.

This REST API moves a specified range to a destination range on an Excel worksheet.

## The Post Worksheet Cells Range Move to Web API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/moveto
```

### Authentication

The API requires a **Bearer JWT token** obtained through the Aspose Cloud OAuth flow. Include the token in the `Authorization` header:

```
Authorization: Bearer <jwt token>
```

The token must have the **Cells** scope.

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| name | String | Path | The file name. |
| sheetName | String | Path | The worksheet name. |
| range | class:range | HTTPBody | range in worksheet |
| destRow | Integer | Query | The start row of the dest range. |
| destColumn | Integer | Query | The start column of the dest range. |
| folder | String | Query | Original workbook folder. |
| storageName | String | Query | Storage name. |

### Example Request / Response

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

**HTTP Status Codes**

| Code | Meaning | Description |
|---|---|---|
| 200 | OK | The request completed successfully. |
| 400 | Bad Request | The request is malformed or one or more parameters are invalid. |
| 401 | Unauthorized | Authentication failed, or the JWT token is missing or expired. |
| 404 | Not Found | The requested workbook, worksheet, or resource was not found. |
| 413 | Payload Too Large | The uploaded file exceeds the allowed size limit. |
| 500 | Internal Server Error | The server encountered an unexpected error while processing the request. |

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/moveto?destRow=20&destColumn=20" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-d '{
  "ColumnCount": 7,
  "ColumnWidth": 19,
  "FirstColumn": 0,
  "FirstRow": 9,
  "Name": "MyRange",
  "RefersTo": "A10:G10",
  "RowCount": 1,
  "RowHeight": 15,
  "Worksheet": "Sheet1"
}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}


{{< /tab >}}

{{< /tabs >}}

When an error occurs, the response includes an optional `ErrorMessage` field that provides additional details about the failure.


**Response Schema**

| Field            | Type              | Description                                           |
| ---------------- | ----------------- | ----------------------------------------------------- |
| **Code**         | integer           | HTTP‑like status code returned by the API (e.g., 200) |
| **Status**       | string            | Textual description of the result (e.g., "OK")        |
| **ErrorMessage** | string (optional) | Human‑readable error details when the call fails      |

### Prerequisites

- The workbook must be stored in Aspose Cloud storage.
- Provide the storage name (`storageName`) and the folder path (`folder`) if the file is not in the root directory.
- Use the latest Aspose.Cells Cloud SDK version that supports API version **v3.0**.

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Body

| Field           | Type    | Required | Description                                              |
| --------------- | ------- | -------- | -------------------------------------------------------- |
| **ColumnCount** | integer | No       | Number of columns in the source range                    |
| **ColumnWidth** | integer | No       | Width of each column (in points)                         |
| **FirstColumn** | integer | No       | Zero‑based index of the first column of the source range |
| **FirstRow**    | integer | No       | Zero‑based index of the first row of the source range    |
| **Name**        | string  | No       | Name of the range (if it is a named range)               |
| **RefersTo**    | string  | No       | A‑1 style reference that defines the range               |
| **RowCount**    | integer | No       | Number of rows in the source range                       |
| **RowHeight**   | integer | No       | Height of each row (in points)                           |
| **Worksheet**   | string  | No       | Worksheet that contains the source range                 |

### Workflow

1. **Upload** the workbook to Aspose Cloud storage (if it does not already exist).
2. **Generate** a JWT token using the OAuth endpoint.
3. **Build** the JSON payload that describes the source range.
4. **Call** the `moveto` endpoint with the required path, query parameters, and the JSON body.
5. **Verify** the response; a successful call returns a `200 OK` status.

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeMoveTo.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeMoveTo.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeMoveTo.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeMoveTo.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeMoveTo.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeMoveTo.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeMoveTo.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeMoveTo.go" >}}

{{< /tab >}}

{{< /tabs >}}
