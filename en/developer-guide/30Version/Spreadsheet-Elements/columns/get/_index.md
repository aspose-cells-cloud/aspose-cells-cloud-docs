---
title: Get Column Details – Aspose.Cells Cloud API Reference (v4.0)
description: Retrieve detailed information about a worksheet column (index, width, style, hidden state) using Aspose.Cells Cloud REST API.
keywords: Aspose.Cells, Cloud API, Excel column, Get column, REST API, JWT, worksheet
date: 2026-07-30
---

# Get Column Details  

Retrieve detailed information about a specific worksheet column (index, width, style, hidden state) from an Excel workbook stored in Aspose Cloud.

## Table of Contents
1. [Prerequisites](#prerequisites)  
2. [Authentication](#authentication)  
3. [Endpoint](#endpoint)  
4. [Request Parameters](#request-parameters)  
5. [cURL Example](#curl-example)  
6. [Response Example](#response-example)  
7. [Response Schema](#response-schema)  
8. [Possible Errors](#possible-errors)  
9. [SDK Examples](#sdk-examples)  
10. [Additional Resources](#additional-resources)  

---

## Prerequisites
- A valid **JWT access token** obtained via Aspose Cloud authentication.  
- The workbook file must be stored in Aspose Cloud Storage (or another supported storage) and the folder path (if any) must be known.  

---

## Authentication
All Aspose.Cells Cloud APIs use **JWT token‑based authentication**. Include the token in the `Authorization` header:

```http
Authorization: Bearer <access_token>
```

For details on obtaining a token, see the [authentication guide](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

---

## Endpoint
```
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{sheetName}/cells/columns/{columnIndex}
```

- **{name}** – workbook file name (e.g., `test.xlsx`).  
- **{sheetName}** – worksheet name (e.g., `Sheet1`).  
- **{columnIndex}** – zero‑based index of the column to retrieve.

---

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

## Request Parameters

| Name          | Location | Type    | Required | Description |
|---------------|----------|---------|----------|-------------|
| **name**      | path     | string  | Yes      | The workbook file name. |
| **sheetName** | path     | string  | Yes      | The worksheet that contains the column. |
| **columnIndex** | path  | integer | Yes      | Zero‑based index of the column to retrieve. |
| **folder**    | query    | string  | No       | Storage folder where the workbook resides. |
| **storageName** | query  | string  | No       | Name of the storage service (e.g., Aspose Cloud Storage). |

---

## cURL Example
```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/0?folder=MyFolder&storageName=MyStorage" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>"
```

---

## Response Example
```json
{
  "Column": {
    "GroupLevel": 0,
    "Index": 0,
    "IsHidden": false,
    "Width": 8.5,
    "Style": {
      "link": {
        "Href": "/style",
        "Rel": "self"
      }
    },
    "link": {
      "Href": "https://api.aspose.cloud/v4.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/0",
      "Rel": "self"
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

---

## Response Schema
| Field               | Type    | Description |
|---------------------|---------|-------------|
| `Column.GroupLevel` | integer | Outline level of the column (used for grouping). |
| `Column.Index`      | integer | Zero‑based index of the column. |
| `Column.IsHidden`   | boolean | `true` if the column is hidden; otherwise `false`. |
| `Column.Width`      | number  | Width of the column expressed in characters. |
| `Column.Style`      | object  | Contains a `link` to the column’s style resource. |
| `Column.link`       | object  | Self‑link to the column resource. |
| `Code`              | integer | HTTP status code of the response. |
| `Status`            | string  | Textual description of the status (e.g., **OK**). |

---

## Possible Errors
| HTTP Status | Code | Message                | When it occurs |
|-------------|------|------------------------|----------------|
| 400         | 400  | Bad Request            | Missing or malformed required parameters. |
| 401         | 401  | Unauthorized           | Missing or invalid `Authorization` header. |
| 404         | 404  | Not Found              | Workbook, worksheet, or column does not exist. |
| 500         | 500  | Internal Server Error  | Unexpected server‑side problem. |

### Example – 404 Not Found
```json
{
  "Code": 404,
  "Message": "Column index out of range."
}
```

### Example – 401 Unauthorized
```json
{
  "Code": 401,
  "Message": "Invalid or missing authentication token."
}
```

---

## SDK Examples
The following code snippets demonstrate how to call the **Get Worksheet Columns** operation using the official Aspose.Cells Cloud SDKs. If a Gist becomes unavailable, the example code is also provided inline.

<details><summary>**C#**</summary>

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;

// Configure API client
var apiInstance = new CellsApi("client_id", "client_secret");

// Set required parameters
string name = "test.xlsx";
string sheetName = "Sheet1";
int columnIndex = 0;
string folder = "MyFolder";          // optional
string storageName = "MyStorage";    // optional

try
{
    var response = apiInstance.GetWorksheetColumns(name, sheetName, columnIndex, folder, storageName);
    Console.WriteLine("Column Index: " + response.Column.Index);
    Console.WriteLine("Width: " + response.Column.Width);
}
catch (Exception e)
{
    Console.WriteLine("Exception when calling CellsApi.GetWorksheetColumns: " + e.Message );
}
```

</details>

<details><summary>**Java**</summary>

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.ColumnsResponse;

public class GetWorksheetColumnsExample {
    public static void main(String[] args) {
        CellsApi apiInstance = new CellsApi("client_id", "client_secret");

        String name = "test.xlsx";
        String sheetName = "Sheet1";
        Integer columnIndex = 0;
        String folder = "MyFolder";          // optional
        String storageName = "MyStorage";    // optional

        try {
            ColumnsResponse result = apiInstance.getWorksheetColumns(name, sheetName, columnIndex, folder, storageName);
            System.out.println("Column index: " + result.getColumn().getIndex());
            System.out.println("Width: " + result.getColumn().getWidth());
        } catch (Exception e) {
            System.err.println("Exception while calling CellsApi#getWorksheetColumns");
            e.printStackTrace();
        }
    }
}
```

</details>

<details><summary>**Python**</summary>

```python
import asposecellscloudsdk
from asposecellscloudsdk import CellsApi, ApiClient, Configuration

config = Configuration()
config.client_id = "client_id"
config.client_secret = "client_secret"

api_instance = CellsApi(ApiClient(config))

name = "test.xlsx"
sheet_name = "Sheet1"
column_index = 0
folder = "MyFolder"       # optional
storage_name = "MyStorage"  # optional

try:
    response = api_instance.get_worksheet_columns(name, sheet_name, column_index, folder, storage_name)
    print("Column index:", response.column.index)
    print("Width:", response.column.width)
except Exception as e:
    print("Exception when calling CellsApi->get_worksheet_columns:", e)
```

</details>

<details><summary>**Node.js (TypeScript)**</summary>

```typescript
import { CellsApi, Configuration } from "@asposecloud/cells-sdk";

const config = new Configuration({
    clientId: "client_id",
    clientSecret: "client_secret"
});
const apiInstance = new CellsApi(config);

const name = "test.xlsx";
const sheetName = "Sheet1";
const columnIndex = 0;
const folder = "MyFolder";       // optional
const storageName = "MyStorage"; // optional

apiInstance.getWorksheetColumns(name, sheetName, columnIndex, folder, storageName)
    .then((result) => {
        console.log("Column index:", result.column?.index);
        console.log("Width:", result.column?.width);
    })
    .catch((error) => {
        console.error("Error calling getWorksheetColumns:", error);
    });
```

</details>

> **Note:** All SDKs automatically handle the `Authorization` header after you provide `client_id` and `client_secret`.

---

## Additional Resources
- **OpenAPI Specification:** <https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetColumns>  
- **Authentication Guide:** <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>  
- **GitHub Repository (SDKs & Samples):** <https://github.com/aspose-cells-cloud>  

--- 

*Document last updated on 2026‑07‑30.*