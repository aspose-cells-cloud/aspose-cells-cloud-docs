---
title: "Protect Excel Files"
second_title: "Document"
linktitle: "Encrypt Excel files"
date: 2024-05-22
lastmod: 2024-05-22
type: docs
url: /protect-excel-files/
aliases:
  [
    /protect/without-storage/
  ]
keywords: "Aspose.Cells, Excel protection API, encrypt Excel workbook, cloud spreadsheet security, REST API"
description: "Encrypt and protect Excel workbooks using Aspose.Cells Cloud REST API with JWT authentication. Includes cURL, SDK examples, and error codes."
weight: 40
---

Use Aspose.Cells Cloud REST API to encrypt and protect Excel workbooks. This guide demonstrates how to apply password protection via the `POST /cells/protect` endpoint using HTTP requests, cURL, and SDKs for multiple programming languages.

## REST API Endpoint

```http
POST https://api.aspose.cloud/v3.0/cells/protect
```

> **Security Note**: This endpoint requires HTTPS. Using HTTP exposes credentials to interception.

### Authentication

All requests must include a valid [JWT token](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).  
Include the token in the `Authorization` header:

```http
Authorization: Bearer <your_jwt_token>
```

### Request Parameters

| Parameter Name         | Type   | Location | Description                                      | Required |
|------------------------|--------|----------|--------------------------------------------------|----------|
| `file`                 | file   | formData | Excel file(s) to protect                         | Yes      |
| `password`             | string | query    | Password to encrypt the workbook                 | No       |
| `protectWorkbookRequest` | object | body     | Optional structured request payload (e.g., encryption options) | No       |

> **Note**: If `password` is provided in the query string, it takes precedence over any password in the request body.

### Request Example (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/protect?password=MySecretPwd" \
  -X POST \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your_jwt_token>" \
  -F 'file=@sample.xlsx'
```

### Response

On success (`200 OK`), the API returns a `FilesResult` object containing the protected file(s) as Base64-encoded content.

```json
{
  "Files": [
    {
      "Filename": "sample.xlsx",
      "FileSize": 274022,
      "FileContent": "[base64-encoded protected workbook]"
    }
  ]
}
```

#### HTTP Status Codes

| Code | Meaning                     | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Protection applied successfully.                 |
| 400  | Bad Request                 | Missing file, invalid password, or unsupported format. |
| 401  | Unauthorized                | Invalid or missing JWT token.                    |
| 403  | Forbidden                   | Insufficient permissions or account restrictions. |
| 413  | Payload Too Large           | File exceeds maximum upload size (1 GB).         |
| 500  | Internal Server Error       | Unexpected server-side error.                    |

#### Example Error Response

```json
{
  "Code": 400,
  "Message": "File is required."
}
```

## SDK Examples

Using an SDK simplifies authentication, request construction, and response parsing. The Aspose.Cells Cloud SDKs are open-source and available on [GitHub](https://github.com/aspose-cells-cloud).

### Node.js (JavaScript)

```javascript
// Aspose.Cells Cloud SDK for Node.js v22.5.0
const { CellsApi, PostProtectRequest } = require('aspose-cells-cloud');

const clientId = process.env['CELLS_CLOUD_CLIENT_ID'];
const clientSecret = process.env['CELLS_CLOUD_CLIENT_SECRET'];

const cellsApi = new CellsApi(clientId, clientSecret);

const fileName = 'sample.xlsx';
const password = 'MySecretPwd';

const request = new PostProtectRequest({
  file: fileName,
  password: password
});

cellsApi.postProtect(request)
  .then((response) => {
    console.log('Protected workbook downloaded.');
    // Handle response.files[0].fileContent (Base64)
  })
  .catch((error) => console.error('Error:', error));
```

### Java

```java
// Aspose.Cells Cloud SDK for Java v24.1.0
import com.aspose.cells.cloud.*;
import java.io.File;

public class ExamplePostProtect {
    public static void main(String[] args) {
        String clientId = "your_client_id";
        String clientSecret = "your_client_secret";
        
        CellsApi cellsApi = new CellsApi(clientId, clientSecret);
        
        try {
            File file = new File("sample.xlsx");
            String password = "MySecretPwd";
            
            FilesResult result = cellsApi.postProtect(file, password, null, null);
            System.out.println("Protected workbook saved.");
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

### Python

```python
# Aspose.Cells Cloud SDK for Python v22.9.0
import asposecellscloud
from asposecellscloud.api import CellsApi
from asposecellscloud.models import PostProtectRequest

api_client = asposecellscloud.ApiClient(
    api_base_url='https://api.aspose.cloud',
    auth_credentials={
        'client_id': 'your_client_id',
        'client_secret': 'your_client_secret'
    }
)

cells_api = CellsApi(api_client)

with open('sample.xlsx', 'rb') as f:
    file_content = f.read()

request = PostProtectRequest(
    file='sample.xlsx',
    password='MySecretPwd'
)

result = cells_api.post_protect(request)
print("Protected workbook retrieved.")
```

> See [GitHub](https://github.com/aspose-cells-cloud) for complete examples in C#, PHP, Ruby, Perl, and Go.

## Best Practices

- **Use HTTPS only** — Never send passwords over unencrypted connections.  
- **Store passwords securely** — Use environment variables or secret managers (e.g., AWS Secrets Manager).  
- **Validate file types** — Ensure uploaded files are valid Excel workbooks (`.xlsx`, `.xls`, `.xlsm`).  
- **Handle Base64 content** — Decode the `FileContent` field before saving to disk.  
- **Update SDKs** — Use the latest SDK versions for security patches and feature support.

---

_Last updated: 2024-05-22_