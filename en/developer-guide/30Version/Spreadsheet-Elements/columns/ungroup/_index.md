---
title: Ungroup Columns in Excel – Aspose.Cells Cloud API
second_title: "Aspose.Cells Cloud Documentation"
linktitle: "Ungroup Columns"
type: docs
url: /columns/ungroup/
aliases:
  [
    "/ungroup-columns-in-an-excel-worksheet/",
    "/ungroup-columns-in-excel-worksheet/",
  ]
description: Remove column grouping in an Excel worksheet using the Aspose.Cells Cloud REST API v3.0. Includes endpoint details, path and query parameters, authentication requirements, cURL examples, and ready-to-run SDK code snippets in C#, Java, Python, Node.js, and Go.
keywords: "ungroup columns, Excel API, Aspose.Cells Cloud, REST API, column grouping, worksheet operations"
slug: columns/ungroup
date: 2024-06-15
weight: 70
draft: false
---

# Ungroup Columns in Excel

Aspose.Cells Cloud provides a **POST** operation to remove column grouping from a specified worksheet in an Excel workbook. This page details the API endpoint, required parameters, authentication method, request examples (cURL), response format, and ready-to-use SDK code snippets for multiple programming languages.

## Prerequisites

| Requirement                                 | Why It’s Needed |
| ------------------------------------------- | --------------- |
| **Aspose Cloud account**                    | Required to access Aspose.Cells Cloud services. |
| **JWT access token**                        | All API calls must include an `Authorization: Bearer <access_token>` header. See the [JWT authentication guide](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/). |
| **Workbook in Aspose Cloud Storage**        | The target workbook must be stored in Aspose Cloud Storage or a connected external storage (e.g., Amazon S3, Google Drive). |
| **Worksheet name**                          | The worksheet containing the grouped columns must exist in the workbook. |

> 💡 **Tip**: Upload your workbook first using the [Files API](https://apireference.aspose.cloud/cells/#/Files).

---

## Authentication

All requests require an `Authorization` header with a valid JWT bearer token:

```http
Authorization: Bearer <YOUR_ACCESS_TOKEN>
```

Tokens are issued via Aspose Cloud OAuth 2.0 and expire after a set period. Refresh tokens as needed.

---

## Endpoint

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/ungroup
```

### Path Parameters

| Name        | Type   | Required | Description             |
| ----------- | ------ | -------- | ----------------------- |
| `name`      | string | Yes      | The workbook file name (e.g., `test.xlsx`). |
| `sheetName` | string | Yes      | The worksheet name (e.g., `Sheet1`). |

### Query Parameters

| Name          | Type    | Required | Description                                         |
| ------------- | ------- | -------- | --------------------------------------------------- |
| `firstIndex`  | integer | Yes      | Zero-based index of the first column to ungroup.    |
| `lastIndex`   | integer | Yes      | Zero-based index of the last column to ungroup.     |
| `folder`      | string  | No       | Folder path containing the workbook (e.g., `docs/reports`). |
| `storageName` | string  | No       | Name of the storage service (e.g., `MyStorage`).    |

> 📌 **Note**: `firstIndex` and `lastIndex` are **inclusive**. Example: `firstIndex=1`, `lastIndex=5` ungroups columns B through F.

---

## Request Example (cURL)

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/ungroup?firstIndex=1&lastIndex=5" \
     -H "Authorization: Bearer <YOUR_ACCESS_TOKEN>" \
     -H "Accept: application/json"
```

Replace `<YOUR_ACCESS_TOKEN>` with your valid JWT token.

---

## Response

### Success Response (200 OK)

```json
{
  "Code": 200,
  "Status": "OK",
  "Columns": {
    "FirstIndex": 1,
    "LastIndex": 5
  }
}
```

The `Columns` object confirms the range of columns that were successfully ungrouped.

### Error Response

| Field          | Type   | Description                          |
| -------------- | ------ | ------------------------------------ |
| `Code`         | integer | HTTP status code (e.g., `400`, `401`). |
| `Status`       | string  | Short error description (e.g., `"Bad Request"`). |
| `ErrorMessage` | string  | Detailed error message.              |

### Common HTTP Status Codes

| Code | Meaning               | Description |
| ---- | --------------------- | ----------- |
| 200  | OK                    | Columns successfully ungrouped. |
| 400  | Bad Request           | Missing/invalid parameters (e.g., negative `firstIndex`, `lastIndex` < `firstIndex`). |
| 401  | Unauthorized          | Invalid, expired, or missing JWT token. |
| 404  | Not Found             | Workbook or worksheet not found. |
| 413  | Payload Too Large     | Request body exceeds size limits. |
| 500  | Internal Server Error | Unexpected server error. |

---

## SDK Code Samples

All SDKs follow the same parameter order:  
`name`, `sheetName`, `firstIndex`, `lastIndex`, `folder`, `storageName`.

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;

var config = new Configuration
{
    AccessToken = "<YOUR_ACCESS_TOKEN>",
    BaseUrl = "https://api.aspose.cloud"
};
var cellsApi = new CellsApi(config);

var response = cellsApi.PostUngroupWorksheetColumns(
    name: "test.xlsx",
    sheetName: "Sheet1",
    firstIndex: 1,
    lastIndex: 5,
    folder: null,
    storageName: null);

Console.WriteLine($"Ungrouped columns: {response.Columns.FirstIndex} – {response.Columns.LastIndex}");
```

### Java

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.CellsCloudResponse;
import com.aspose.cells.cloud.Configuration;

Configuration config = new Configuration();
config.setAccessToken("<YOUR_ACCESS_TOKEN>");
config.setBaseUrl("https://api.aspose.cloud");
CellsApi api = new CellsApi(config);

CellsCloudResponse resp = api.postUngroupWorksheetColumns(
    "test.xlsx",
    "Sheet1",
    1,
    5,
    null,
    null);

System.out.println("Ungrouped columns: " + resp.getColumns().getFirstIndex()
                   + " – " + resp.getColumns().getLastIndex());
```

### Python

```python
from asposecellscloud import CellsApi, Configuration

config = Configuration()
config.access_token = "<YOUR_ACCESS_TOKEN>"
config.base_url = "https://api.aspose.cloud"

api = CellsApi(config)

response = api.post_ungroup_worksheet_columns(
    name="test.xlsx",
    sheet_name="Sheet1",
    first_index=1,
    last_index=5,
    folder=None,
    storage_name=None)

print(f"Ungrouped columns: {response.columns.first_index} – {response.columns.last_index}")
```

### Node.js

```javascript
const { CellsApi, Configuration } = require("asposecellscloud");

const config = new Configuration({
  accessToken: "<YOUR_ACCESS_TOKEN>",
  baseUrl: "https://api.aspose.cloud",
});

const api = new CellsApi(config);

api
  .postUngroupWorksheetColumns("test.xlsx", "Sheet1", 1, 5, null, null)
  .then((resp) => {
    console.log(
      `Ungrouped columns: ${resp.columns.firstIndex} – ${resp.columns.lastIndex}`
    );
  })
  .catch((err) => console.error(err));
```

### Go

```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3/sdk"
)

func main() {
    config := sdk.NewConfiguration()
    config.AccessToken = "<YOUR_ACCESS_TOKEN>"
    config.BasePath = "https://api.aspose.cloud"

    api := sdk.NewCellsApi(config)

    resp, _, err := api.PostUngroupWorksheetColumns(
        "test.xlsx",
        "Sheet1",
        1,
        5,
        nil,
        nil,
    )
    if err != nil {
        panic(err)
    }
    fmt.Printf("Ungrouped columns: %d – %d\n", resp.Columns.FirstIndex, resp.Columns.LastIndex)
}
```

> 📦 **All SDKs**: Refer to the [Aspose.Cells Cloud GitHub repository](https://github.com/aspose-cells-cloud) for additional languages (PHP, Ruby, Perl) and full source examples.

---

## References

- **OpenAPI Specification**: [PostUngroupWorksheetColumns](https://apireference.aspose.cloud/cells/#/Cells/PostUngroupWorksheetColumns)
- **Authentication Guide**: [Authenticating API Requests](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)
- **SDK Repository**: [github.com/aspose-cells-cloud](https://github.com/aspose-cells-cloud)
- **Files API**: [Upload/Download Files](https://apireference.aspose.cloud/cells/#/Files)

---

## Revision History

| Date       | Author | Change |
| ---------- | ------ | ------ |
| 2024-06-15 | AI Optimizer | Fixed front matter: corrected future-dated `date`, added `description`, removed low-value `keywords`, standardized placeholders (`<YOUR_ACCESS_TOKEN>`), removed duplicate H1, and updated revision history. |
| 2024-06-14 | Original | Initial draft. |