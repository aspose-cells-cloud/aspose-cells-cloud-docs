---
title: "Get Files List (Folder Contents)"
description: "Retrieve files and subfolders from Aspose.Cells Cloud storage via GET /storage/folder/{path}. Includes authentication, request parameters, cURL, and SDK examples for Python, Java, and Node.js."
linktitle: "Get Files List"
type: docs
date: 2024-03-15T09:00:00Z
canonical: https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Folder/GetFilesList
url: /get-files-list/
keywords:
  - Aspose.Cells
  - API
  - Get Files List
  - Cloud Storage
  - Excel
  - REST
  - folder contents
weight: 100
---

## Overview

The **Get Files List** operation retrieves a paginated list of files and subfolders from a specified folder in Aspose.Cells Cloud storage. This endpoint is the primary method for exploring and navigating cloud-based Excel workbooks, templates, and other supported file formats.

```
GET https://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

## Security and Authentication

All Aspose.Cells Cloud API requests require JWT token-based authentication. Refer to the [Authentication Guide](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) for step-by-step instructions.

## Request Parameters

| Name            | Location | Type    | Required | Description                                                                 |
|-----------------|----------|---------|----------|-----------------------------------------------------------------------------|
| **path**        | Path     | string  | Yes      | Path to the target folder in cloud storage (e.g., `/Reports/2024/Q1`).     |
| **storageName** | Query    | string  | No       | Name of the storage to use. If omitted, the default storage is used.       |
| **pageSize**    | Query    | integer | No       | Maximum number of items per page. *(default: 100)*                        |
| **pageNumber**  | Query    | integer | No       | Page number to retrieve (1-indexed). *(default: 1)*                       |

### Response Structure

The response returns a `FilesList` object containing:

- **Value** – Array of `StorageFile` objects with:
  - `Name` – File or folder name (string)
  - `IsFolder` – Boolean (`true` for folders)
  - `Size` – Size in bytes (folders report `0`)
  - `ModifiedDate` – Last modification timestamp (ISO 8601 format)

## HTTP Status Codes

| Code | Status                | Description                                                                 |
|------|-----------------------|-----------------------------------------------------------------------------|
| 200  | OK                    | Request succeeded; folder contents returned.                               |
| 400  | Bad Request           | Invalid or missing `path` parameter, or unsupported storage name.         |
| 401  | Unauthorized          | Invalid, expired, or missing JWT token.                                    |
| 403  | Forbidden             | Insufficient permissions for the requested folder.                         |
| 404  | Not Found             | Specified folder does not exist.                                           |
| 500  | Internal Server Error | An unexpected server error occurred.                                       |

## cURL Example

{{< code-block lang="bash" alt="cURL command to list folder contents in Aspose.Cells Cloud" >}}
```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/folder/Reports/2024?storageName=MyStorage&pageSize=50&pageNumber=1" \
     -H "Authorization: Bearer <your_access_token>"
```
{{< /code-block >}}

### Example Response

{{< code-block lang="json" alt="JSON response showing folder contents including files and subfolders" >}}
```json
{
  "Value": [
    {
      "Name": "Q1_Sales.xlsx",
      "IsFolder": false,
      "Size": 142856,
      "ModifiedDate": "2024-04-02T15:30:12Z"
    },
    {
      "Name": "Archives",
      "IsFolder": true,
      "Size": 0,
      "ModifiedDate": "2024-02-15T09:45:00Z"
    }
  ]
}
```
{{< /code-block >}}

> 💡 **Note**: Timestamps in examples are illustrative. Actual `ModifiedDate` values reflect real-time updates.

## Using Aspose.Cells Cloud SDKs

SDKs handle authentication, request serialization, and error handling—accelerating development. Below are code examples for popular languages.

### Python

```python
import asposecellscloud
from asposecellscloud.api import cells_api
from asposecellscloud.models import *

configuration = asposecellscloud.Configuration(
    app_sid="your_app_sid",
    app_key="your_app_key"
)
api = cells_api.CellsApi(configuration)

try:
    response = api.storage_folder_get_files_list(
        path="Reports/2024",
        storage_name="MyStorage",
        page_size=50,
        page_number=1
    )
    for file in response.value:
        print(f"{file.name} ({'folder' if file.is_folder else 'file'})")
except Exception as e:
    print(f"Error: {e}")
```

### Java

```java
import com.aspose.cells.cloud.*;
import com.aspose.cells.cloud.api.*;
import com.aspose.cells.cloud.model.*;

ApiClient apiClient = new ApiClient("your_app_sid", "your_app_key", null);
CellsApi cellsApi = new CellsApi(apiClient);

try {
    FilesList response = cellsApi.storageFolderGetFilesList(
        "Reports/2024", 
        "MyStorage", 
        50, 
        1
    );
    for (StorageFile file : response.getValue()) {
        System.out.printf("%s (%s)%n", file.getName(), 
            file.getIsFolder() ? "folder" : "file");
    }
} catch (ApiException e) {
    System.err.println("Error: " + e.getMessage());
}
```

### Node.js

```javascript
const { CellsApi, StorageFile } = require("asposecellscloud");

const apiClient = new CellsApi(
  "your_app_sid",
  "your_app_key"
);

try {
  const response = await apiClient.storageFolderGetFilesList(
    "Reports/2024",
    "MyStorage",
    50,
    1
  );
  response.value.forEach(file => {
    console.log(`${file.name} (${file.isFolder ? 'folder' : 'file'})`);
  });
} catch (error) {
  console.error("Error:", error);
}
```

> 📘 **Learn More**:  
> - [Download a File](/cells/get-file/)  
> - [Upload a File](/cells/upload-file/)  
> - [Using the Python SDK](/cells/python-sdk/)  
> - [Using the Java SDK](/cells/java-sdk/)  
> - [Using the Node.js SDK](/cells/nodejs-sdk/)

## Folder Structure Example

![Folder tree diagram: root contains Reports and Archives folders; Reports contains quarterly subfolders](https://docs.aspose.cloud/cells/folder-hierarchy.png)

*alt="Folder tree diagram: root contains Reports and Archives folders; Reports contains quarterly subfolders"*

## External Resources

- [OpenAPI Specification (GitHub)](https://github.com/aspose-cells-cloud/aspose-cells-cloud-openapi-spec/blob/master/spec/cells_api.yaml)
- [Swagger UI Demo](https://petstore.swagger.io/?url=https://raw.githubusercontent.com/aspose-cells-cloud/aspose-cells-cloud-openapi-spec/master/spec/cells_api.yaml)

---

*Last updated: 2024-03-15*