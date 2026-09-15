---
title: "Delete Vertical Page Break | Aspose.Cells Cloud REST API"
date: 2024-03-15
lastmod: 2024-03-15
description: "Learn how to delete a vertical page break from an Excel worksheet using the Aspose.Cells Cloud REST API v3.0. Includes cURL examples, error codes, and SDK snippets in C#, Java, Python, Node.js, and Go."
tags:
  - "page-break"
  - "excel-api"
  - "rest-api"
categories:
  - "cells"
  - "api-reference"
weight: 10
draft: false
slug: delete-vertical-page-break
api_version: v3.0
---

# Delete Vertical Page Break

Delete a vertical page break from a worksheet in an Excel workbook using the Aspose.Cells Cloud REST API.

> 💡 **Tip**: Replace `client_id` and `client_secret` with valid credentials from your [Aspose Cloud Dashboard](https://dashboard.aspose.cloud/). For JWT token generation, see our [Authentication Guide]（https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/）.

---

## Prerequisites

- A **JWT authentication token** must be supplied in the `Authorization` header.
- The workbook (`{name}`) must be stored in the specified **folder** or **storage** and be accessible to the API client.

> 🔗 **Related**: [Get Vertical Page Breaks](/cells/get-vertical-page-breaks/) to list existing breaks before deletion.

---

## HTTP Request

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/verticalpagebreaks/{index}
```

| Parameter       | Type    | Location | Required | Description                                             |
| --------------- | ------- | -------- | -------- | ------------------------------------------------------- |
| **name**        | string  | path     | Yes      | The name of the Excel file.                             |
| **sheetName**   | string  | path     | Yes      | The name of the worksheet that contains the page break. |
| **index**       | integer | path     | Yes      | Zero‑based index of the vertical page break to delete.  |
| **folder**      | string  | query    | No       | Folder path where the file is stored.                   |
| **storageName** | string  | query    | No       | Name of the storage service.                            |

---

## Request Example

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/verticalpagebreaks/0?folder=Docs&storageName=MyStorage" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt_token>"
```

---

## Success Response

| Code    | Description                                       |
| ------- | ------------------------------------------------- |
| **200** | The vertical page break was deleted successfully. |

**Example payload**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

---

## Error Responses

| HTTP Code | Description                                                                    |
| --------- | ------------------------------------------------------------------------------ |
| **401**   | Unauthorized – missing or invalid token.                                       |
| **404**   | Not Found – the specified file, worksheet, or page‑break index does not exist. |
| **400**   | Bad Request – malformed request syntax or invalid parameters.                  |
| **500**   | Internal Server Error – an unexpected condition was encountered.               |

**Sample error payloads**

_401 – Unauthorized_

```json
{
  "Code": 401,
  "Message": "Invalid authentication token."
}
```

_404 – Not Found_

```json
{
  "Code": 404,
  "Message": "The specified file, worksheet, or page‑break index was not found."
}
```

_400 – Bad Request_

```json
{
  "Code": 400,
  "Message": "The request parameters are invalid or malformed."
}
```

_500 – Internal Server Error_

```json
{
  "Code": 500,
  "Message": "An unexpected server error occurred."
}
```

---

## SDK Code Samples

The following examples demonstrate how to call the **DeleteVerticalPageBreak** operation using various Aspose.Cells Cloud SDKs.

<details><summary>**C#**</summary>

```csharp
// Install-Package Aspose.Cells-Cloud
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var apiInstance = new CellsApi("client_id", "client_secret");
string name = "Book1.xlsx";
string sheetName = "Sheet1";
int index = 0;
string folder = "Docs";
string storageName = "MyStorage";

try
{
    var response = apiInstance.DeleteVerticalPageBreak(name, sheetName, index, folder, storageName);
    Console.WriteLine($"Status: {response.Status}");
}
catch (Exception e)
{
    Console.WriteLine("Exception when calling CellsApi.DeleteVerticalPageBreak: " + e.Message );
}
```

</details>

<details><summary>**Java**</summary>

```java
import com.aspose.cloud.cells.api.CellsApi;
import com.aspose.cloud.cells.model.CellsCloudResponse;

public class DeleteVerticalPageBreak {
    public static void main(String[] args) {
        CellsApi api = new CellsApi("client_id", "client_secret");
        String name = "Book1.xlsx";
        String sheetName = "Sheet1";
        int index = 0;
        String folder = "Docs";
        String storageName = "MyStorage";

        try {
            CellsCloudResponse resp = api.deleteVerticalPageBreak(name, sheetName, index, folder, storageName);
            System.out.println("Status: " + resp.getStatus());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

</details>

<details><summary>**Python**</summary>

```python
from asposecellscloud import CellsApi, ApiClient, Configuration

config = Configuration()
config.client_id = "client_id"
config.client_secret = "client_secret"
api_client = ApiClient(configuration=config)
api = CellsApi(api_client)

name = "Book1.xlsx"
sheet_name = "Sheet1"
index = 0
folder = "Docs"
storage_name = "MyStorage"

try:
    response = api.delete_vertical_page_break(name, sheet_name, index, folder, storage_name)
    print("Status:", response.status)
except Exception as e:
    print("Error:", e)
```

</details>

<details><summary>**Node.js**</summary>

```javascript
const { CellsApi, ApiClient, Configuration } = require("asposecellscloud");

const config = new Configuration();
config.clientId = "client_id";
config.clientSecret = "client_secret";

const api = new CellsApi(new ApiClient(config));

const name = "Book1.xlsx";
const sheetName = "Sheet1";
const index = 0;
const folder = "Docs";
const storageName = "MyStorage";

api
  .deleteVerticalPageBreak(name, sheetName, index, folder, storageName)
  .then((response) => console.log("Status:", response.status))
  .catch((error) => console.error("Error:", error));
```

</details>

<details><summary>**Go**</summary>

```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3"
)

func main() {
    config := asposecellscloud.NewConfiguration()
    config.ClientId = "client_id"
    config.ClientSecret = "client_secret"

    api := asposecellscloud.NewAPIClient(config).CellsApi
    name := "Book1.xlsx"
    sheetName := "Sheet1"
    index := int32(0)
    folder := "Docs"
    storageName := "MyStorage"

    resp, _, err := api.DeleteVerticalPageBreak(name, sheetName, index, folder, storageName)
    if err != nil {
        fmt.Println("Error:", err)
        return
    }
    fmt.Println("Status:", resp.Status)
}
```

</details>

> 📦 **SDKs for other languages** (PHP, Ruby, Perl, etc.) are available in the [Aspose.Cells Cloud GitHub repository](https://github.com/aspose-cells-cloud).

---

## Related Resources

- **OpenAPI Specification (Swagger)** – [Download JSON](https://raw.githubusercontent.com/aspose-cells-cloud/aspose-cells-cloud-go/master/docs/openapi.yaml)
- **Aspose.Cells Cloud SDKs** – <https://github.com/aspose-cells-cloud>
- **Authentication Guide** – <https://docs.aspose.cloud/cells/authentication/>

---

Was this page helpful?  
✅ Yes | ❌ No

_(Feedback helps us improve our documentation.)_

---

_Document last updated: 2024-03-15_
