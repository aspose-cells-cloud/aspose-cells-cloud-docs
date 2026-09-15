---
title: "Delete All Pivot Tables in Excel Using Aspose.Cells Cloud REST API"
second_title: "Aspose.Cells Cloud Document"
linktitle: Clear
type: docs
url: /pivot-tables/clear/
aliases: [/delete-worksheet-pivot-tables/]
description: "Learn how to delete all pivot tables from an Excel worksheet using the Aspose.Cells Cloud REST API. Includes cURL, C#, Java, Python, and Node.js examples with best practices and security guidance."
keywords:
  - "Aspose.Cells"
  - "pivot table"
  - "delete"
  - "REST API"
  - "Excel"
date: 2024-06-15
api_version: "v3.0"
---

# Delete All Pivot Tables in an Excel Worksheet

## Overview

This operation removes **all** pivot tables from a specified worksheet in an Excel file. It is especially useful for resetting analysis layouts, cleaning up unused pivot tables, or preparing templates for reuse—without deleting the worksheet itself.

> 💡 **Best Practice Tip**: Bulk deletion is irreversible. For safety, consider backing up your file or using [versioning](https://docs.aspose.cloud/total/getting-started/storage/versioning/) before running this operation.

## Prerequisites

Before calling the API, ensure you have completed the following steps:

1. **Aspose Cloud Account** – Sign up for an Aspose Cloud account at [dashboard.aspose.cloud](https://dashboard.aspose.cloud/) if you do not already have one.
2. **JWT Token** – Generate a JSON Web Token (JWT) for authentication. See the [Authentication guide](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) for details.
3. **Storage Setup** – Upload the target Excel file to Aspose Cloud storage or a connected external storage. Note the **folder** and **storage name** (if applicable) where the file resides.

## Authentication

The Aspose.Cells Cloud APIs require **JWT token‑based authentication**. Include the token in the `Authorization` header of each request:

```
Authorization: Bearer <your-jwt-token>
```

> 🔒 **Security Note**: Never expose your JWT token in client-side code or public repositories. Store credentials securely (e.g., environment variables or secret managers).

## HTTP Request

```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables
```

### Path Parameters

| Name        | Type   | Required | Description                                             |
|-------------|--------|----------|---------------------------------------------------------|
| `name`      | string | Yes      | The name of the Excel file (e.g., `Sample.xlsx`).      |
| `sheetName` | string | Yes      | The name of the worksheet from which all pivot tables will be removed (e.g., `Sheet1`). |

### Query Parameters

| Name          | Type   | Required | Description                                                           |
|---------------|--------|----------|-----------------------------------------------------------------------|
| `folder`      | string | No       | The folder that contains the file (e.g., `input/`).                  |
| `storageName` | string | No       | The storage name to use (if the file resides in a non-default storage). |

## Request Example (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables?folder=input&storageName=MyStorage" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your-jwt-token>"
```

## Successful Response

The service returns a standard `CellsCloudResponse` object indicating the operation status.

```json
{
  "Code": 200,
  "Status": "OK"
}
```

## Error Handling

| HTTP Status | Meaning                                      | Example Payload                                                    |
|-------------|----------------------------------------------|--------------------------------------------------------------------|
| **400**     | Bad Request – missing or invalid parameters  | `{ "Code": 400, "Message": "Missing required parameter 'name'." }` |
| **401**     | Unauthorized – invalid or expired JWT        | `{ "Code": 401, "Message": "Invalid authentication token." }`      |
| **404**     | Not Found – file or worksheet does not exist | `{ "Code": 404, "Message": "Worksheet not found." }`               |
| **500**     | Internal Server Error – unexpected failure   | `{ "Code": 500, "Message": "An unexpected error occurred." }`      |

## SDK Examples

The following snippets demonstrate how to invoke the operation using Aspose.Cells Cloud SDKs.  
**Important**: Replace `<client-id>` and `<client-secret>` with your actual credentials from the [Aspose Cloud Dashboard](https://dashboard.aspose.cloud/).

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

// Initialize the API client
var apiInstance = new CellsApi("<client-id>", "<client-secret>");

// Configure request parameters
string name = "Sample_Pivot_Table_Example.xls";
string sheetName = "Sheet2";
string folder = "input";
string storageName = "MyStorage";

try
{
    var response = apiInstance.DeleteWorksheetPivotTables(name, sheetName, folder, storageName);
    Console.WriteLine($"Response code: {response.Code}, status: {response.Status}");
}
catch (Exception e)
{
    Console.WriteLine("Exception when calling CellsApi.DeleteWorksheetPivotTables: " + e.Message);
}
```

### Java

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.CellsCloudResponse;

public class DeletePivotTables {
    public static void main(String[] args) {
        CellsApi api = new CellsApi("<client-id>", "<client-secret>");
        String name = "Sample_Pivot_Table_Example.xls";
        String sheetName = "Sheet2";
        String folder = "input";
        String storageName = "MyStorage";

        try {
            CellsCloudResponse result = api.deleteWorksheetPivotTables(name, sheetName, folder, storageName);
            System.out.println("Code: " + result.getCode() + ", Status: " + result.getStatus());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

### Python

```python
import asposecellscloud
from asposecellscloud.api.cells_api import CellsApi

# Configure API client
configuration = asposecellscloud.Configuration()
configuration.api_key['client_id'] = '<client-id>'
configuration.api_key['client_secret'] = '<client-secret>'

api_instance = CellsApi(asposecellscloud.ApiClient(configuration))

name = 'Sample_Pivot_Table_Example.xls'
sheet_name = 'Sheet2'
folder = 'input'
storage_name = 'MyStorage'

try:
    response = api_instance.delete_worksheet_pivot_tables(name, sheet_name, folder, storage_name)
    print(f'Code: {response.code}, Status: {response.status}')
except Exception as e:
    print("Exception when calling CellsApi->delete_worksheet_pivot_tables: %s\n" % e)
```

### Node.js

```javascript
const { CellsApi, Configuration } = require("@aspose/cells-cloud");

const config = new Configuration({
  clientId: "<client-id>",
  clientSecret: "<client-secret>",
});
const apiInstance = new CellsApi(config);

const name = "Sample_Pivot_Table_Example.xls";
const sheetName = "Sheet2";
const folder = "input";
const storageName = "MyStorage";

apiInstance
  .deleteWorksheetPivotTables(name, sheetName, folder, storageName)
  .then((result) => {
    console.log(`Code: ${result.code}, Status: ${result.status}`);
  })
  .catch((err) => {
    console.error("Error:", err);
  });
```

> 📚 **Additional SDKs** (Go, PHP, Ruby, Swift, Perl, Android) are available in the [Aspose.Cells Cloud SDK repository](https://github.com/aspose-cells-cloud).

## See Also

- [Create a Pivot Table](https://docs.aspose.cloud/cells/pivot-tables/create/)
- [Delete a Specific Pivot Table](https://docs.aspose.cloud/cells/pivot-tables/delete-specific/)
- [Get All Pivot Tables in a Worksheet](https://docs.aspose.cloud/cells/pivot-tables/get-all/)
- [Authentication Overview](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)
- [OpenAPI Specification for DeleteWorksheetPivotTables](https://apireference.aspose.cloud/cells/#/PivotTables/DeleteWorksheetPivotTables)

---

_Document last updated on 2024-06-15. All content is UTF‑8 encoded._