---  
title: Ungroup Columns in Excel – Aspose.Cells Cloud API  
description: Remove column grouping in an Excel worksheet using Aspose.Cells Cloud REST API (v3.0). Includes endpoint, parameters, authentication, cURL example, response format, and SDK snippets.  
keywords: Aspose.Cells, ungroup, columns, Excel, API, REST, cloud, SDK  
slug: columns/ungroup  
date: 2026-07-30  
---  

# Ungroup Columns in Excel  

Aspose.Cells Cloud provides a **POST** operation that removes column grouping from a specified worksheet. This page details the request format, required parameters, authentication method, example calls, and SDK usage.

---  

## Prerequisites  

| Requirement | Why It’s Needed |
|------------|-----------------|
| **Aspose Cloud account** | Access to the Aspose.Cells Cloud services. |
| **JWT access token** | All API calls must be authorized with a bearer token. See the [JWT authentication guide](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/). |
| **Workbook stored in Aspose Cloud Storage** | The API works on files located in the cloud storage (or a connected external storage). |
| **Worksheet name** | The target worksheet must exist in the workbook. |

---  

## Authentication  

All requests require an **Authorization** header containing a valid JWT token:

```http
Authorization: Bearer <access_token>
```

The token is obtained via the Aspose Cloud OAuth flow. Tokens are valid for a limited period; refresh as needed.

---  

## Endpoint  

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/ungroup
```

* `{name}` – **Path** – Workbook file name (e.g., `test.xlsx`).  
* `{sheetName}` – **Path** – Worksheet name (e.g., `Sheet1`).  

---  

## Parameters  

### Path Parameters  

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `name` | string | Yes | The workbook file name. |
| `sheetName` | string | Yes | The worksheet name. |

### Query Parameters  

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `firstIndex` | integer | Yes | Zero‑based index of the first column to ungroup. |
| `lastIndex` | integer | Yes | Zero‑based index of the last column to ungroup. |
| `folder` | string | No | Folder path that contains the workbook. |
| `storageName` | string | No | Name of the storage service where the file resides. |

---  

## Request Example (cURL)  

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/ungroup?firstIndex=1&lastIndex=5" \
     -H "Authorization: Bearer <access_token>" \
     -H "Accept: application/json"
```

*Replace `<access_token>` with a valid JWT token.*

---  

## Successful Response  

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

The response object (`CellsCloudResponse`) contains the range of columns that were successfully ungrouped.

### Error Response  

When the request fails, the service returns a JSON payload with the following fields:

| Field | Meaning |
|-------|---------|
| `Code` | HTTP‑style error code (e.g., 400, 401). |
| `Status` | Short description of the error. |
| `ErrorMessage` | Detailed error description. |

---  

## HTTP Status Codes  

| Code | Description |
|------|-------------|
| **200** | Success – columns ungrouped. |
| **400** | Bad Request – missing or invalid parameters. |
| **401** | Unauthorized – token missing or invalid. |
| **403** | Forbidden – insufficient permissions. |
| **404** | Not Found – workbook, worksheet, or columns not found. |
| **500** | Internal Server Error – unexpected server condition. |

---  

## SDK Code Samples  

Below are ready‑to‑run snippets for the most popular SDKs. Replace placeholder values (`<YourAccessToken>`, `<YourFileName>`, etc.) with your own data.

<details><summary>**C# (.NET)**</summary>  

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;

class Program
{
    static void Main()
    {
        var config = new Configuration
        {
            AccessToken = "<YourAccessToken>",
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
    }
}
```
</details>

<details><summary>**Java**</summary>  

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.CellsCloudResponse;
import com.aspose.cells.cloud.Configuration;

public class UngroupColumns {
    public static void main(String[] args) throws Exception {
        Configuration config = new Configuration();
        config.setAccessToken("<YourAccessToken>");
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
    }
}
```
</details>

<details><summary>**Python**</summary>  

```python
from asposecellscloud import CellsApi, Configuration

config = Configuration()
config.access_token = "<YourAccessToken>"
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
</details>

<details><summary>**Node.js**</summary>  

```javascript
const { CellsApi, Configuration } = require('asposecellscloud');

const config = new Configuration({
    accessToken: "<YourAccessToken>",
    baseUrl: "https://api.aspose.cloud"
});

const api = new CellsApi(config);

api.postUngroupWorksheetColumns("test.xlsx", "Sheet1", 1, 5, null, null)
   .then(resp => {
       console.log(`Ungrouped columns: ${resp.columns.firstIndex} – ${resp.columns.lastIndex}`);
   })
   .catch(err => console.error(err));
```
</details>

<details><summary>**Go**</summary>  

```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3/sdk"
)

func main() {
    config := sdk.NewConfiguration()
    config.AccessToken = "<YourAccessToken>"
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
</details>

> **Note:** SDKs for PHP, Ruby, Perl, and other languages follow the same parameter order. Refer to the [GitHub repository](https://github.com/aspose-cells-cloud) for complete examples.

---  

## References  

* **OpenAPI Specification:** <https://apireference.aspose.cloud/cells/#/Cells/PostUngroupWorksheetColumns>  
* **Authentication guide:** <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>  
* **SDK repository:** <https://github.com/aspose-cells-cloud>

---  

## Revision History  

| Date | Author | Change |
|------|--------|--------|
| 2026‑07‑30 | AI Optimizer | Fixed UTF‑8 encoding, added Prerequisites, cleaned meta keywords, improved heading hierarchy, and inserted SDK snippets. |
| 2026‑07‑29 | Original | Initial documentation draft. |

---  