---
title: "Delete All Pivot Tables in an Excel Worksheet"
description: "Deletes every pivot table from a specified worksheet using the Aspose.Cells Cloud REST API."
keywords: "Aspose.Cells, Pivot Table, Delete, REST API, Excel"
date: 2026-07-30
api_version: "v3.0"
---

# Delete All Pivot Tables in an Excel Worksheet

## Overview
This operation removes **all** pivot tables from a given worksheet in an Excel file. It is useful when you need to reset a worksheet’s analysis or clean up unused pivot tables in a single call.

## Prerequisites
Before calling the API, ensure you have completed the following steps:

1. **Aspose Cloud Account** – Sign up for an Aspose Cloud account if you do not already have one.  
2. **JWT Token** – Generate a JSON Web Token (JWT) for authentication. See the [Authentication guide](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) for details.  
3. **Storage Setup** – Upload the target Excel file to Aspose Cloud storage or to a connected external storage. Note the **folder** and **storage name** (if applicable) where the file resides.

## Authentication
The Aspose.Cells Cloud APIs require **JWT token‑based authentication**. Include the token in the `Authorization` header of each request:

```
Authorization: Bearer <jwt token>
```

## HTTP Request

```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables
```

### Path Parameters
| Name | Type   | Required | Description |
|------|--------|----------|-------------|
| `name` | string | Yes | The name of the Excel file (e.g., `Sample.xlsx`). |
| `sheetName` | string | Yes | The name of the worksheet from which all pivot tables will be removed (e.g., `Sheet1`). |

### Query Parameters
| Name | Type   | Required | Description |
|------|--------|----------|-------------|
| `folder` | string | No | The folder that contains the file. |
| `storageName` | string | No | The storage name to use (if the file is not in the default storage). |

## Request Example (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables?folder=SampleFolder&storageName=MyStorage" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
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

| HTTP Status | Meaning | Example Payload |
|-------------|---------|-----------------|
| **400** | Bad Request – missing or invalid parameters | `{ "Code": 400, "Message": "Missing required parameter 'name'." }` |
| **401** | Unauthorized – invalid or expired JWT | `{ "Code": 401, "Message": "Invalid authentication token." }` |
| **404** | Not Found – file or worksheet does not exist | `{ "Code": 404, "Message": "Worksheet not found." }` |
| **500** | Internal Server Error – unexpected failure | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

## SDK Examples

The following snippets demonstrate how to invoke the operation with several Aspose.Cells Cloud SDKs.

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

// Initialise the API client
var apiInstance = new CellsApi("<client-id>", "<client-secret>");

// Configure request parameters
string name = "Sample_Pivot_Table_Example.xls";
string sheetName = "Sheet2";
string folder = "SampleFolder";
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
import com.aspose.cells.cloud.model.*;

public class DeletePivotTables {
    public static void main(String[] args) {
        CellsApi api = new CellsApi("<client-id>", "<client-secret>");
        String name = "Sample_Pivot_Table_Example.xls";
        String sheetName = "Sheet2";
        String folder = "SampleFolder";
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
import asposecellscloud_sdk
from asposecellscloud_sdk import CellsApi, ApiException

# Configure API client
configuration = asposecellscloud_sdk.Configuration()
configuration.api_key['client_id'] = '<client-id>'
configuration.api_key['client_secret'] = '<client-secret>'

api_instance = CellsApi(asposecellscloud_sdk.ApiClient(configuration))

name = 'Sample_Pivot_Table_Example.xls'
sheet_name = 'Sheet2'
folder = 'SampleFolder'
storage_name = 'MyStorage'

try:
    response = api_instance.delete_worksheet_pivot_tables(name, sheet_name, folder, storage_name)
    print(f'Code: {response.code}, Status: {response.status}')
except ApiException as e:
    print("Exception when calling CellsApi->delete_worksheet_pivot_tables: %s\n" % e)
```

### Node.js

```javascript
const { CellsApi, Configuration } = require('asposecellscloud-sdk');

const config = new Configuration({
    clientId: '<client-id>',
    clientSecret: '<client-secret>'
});
const apiInstance = new CellsApi(config);

const name = 'Sample_Pivot_Table_Example.xls';
const sheetName = 'Sheet2';
const folder = 'SampleFolder';
const storageName = 'MyStorage';

apiInstance.deleteWorksheetPivotTables(name, sheetName, folder, storageName)
    .then(result => {
        console.log(`Code: ${result.code}, Status: ${result.status}`);
    })
    .catch(err => {
        console.error('Error:', err);
    });
```

*Additional SDKs (Go, PHP, Ruby, Swift, Perl, Android) are available in the [Aspose.Cells Cloud SDK repository](https://github.com/aspose-cells-cloud).*

## See Also
- [Delete a Specific Pivot Table](https://docs.aspose.cloud/cells/pivot-tables/delete-specific/)
- [Get All Pivot Tables in a Worksheet](https://docs.aspose.cloud/cells/pivot-tables/get-all/)
- [Authentication Overview](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)
- [OpenAPI Specification for DeleteWorksheetPivotTables](https://apireference.aspose.cloud/cells/#/PivotTables/DeleteWorksheetPivotTables)

--- 

*Document last updated on 2026-07-30. All content is UTF‑8 encoded.*