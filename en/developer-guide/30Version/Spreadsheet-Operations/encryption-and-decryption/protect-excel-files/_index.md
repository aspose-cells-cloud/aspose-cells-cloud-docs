---
title: "Protect Excel Files"
second_title: "Developer Guide"
linktitle: "Encrypt Excel files"
date: 2024-05-22
lastmod: 2024-05-22
type: docs
url: /protect-excel-files/
aliases: [/protect/without-storage/]
keywords: "Aspose.Cells, Excel protection API, encrypt Excel workbook, cloud spreadsheet security, REST API"
description: "Encrypt and protect Excel workbooks using Aspose.Cells Cloud REST API with JWT authentication. Includes cURL, SDK examples, and error codes."
weight: 40
ArticleTitle: "Protect Excel Files with Aspose.Cells Cloud REST API"
---
The **PostProtect** API (`POST https://api.aspose.cloud/v3.0/cells/protect`) in Aspose.Cells Cloud enables Excel file encryption by allowing users to upload a workbook and specify protection settings via a `protectWorkbookRequest` body, supporting password-based workbook protection as part of a broader information security strategy; the operation accepts a `File` form-data parameter and an optional `password` query parameter to set access credentials for the protected workbook.

## The Post Protect Web API

```http
POST https://api.aspose.cloud/v3.0/cells/protect
```

### Authentication

All requests must include a valid [JWT token](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).  
Include the token in the `Authorization` header:

```http
Authorization: Bearer <your_jwt_token>
```

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| File | File | FormData | File to upload |
| protectWorkbookRequest | class:protectworkbookrequest | HTTPBody | - |
| password | String | Query | The password needed to open an Excel file. |

> **Note**: If `password` is provided in the query string, it takes precedence over any password in the request body.

### Response

```json
[
  {
    "Name": "FilesResult",
    "DataType": {
      "Identifier": "Class",
      "Reference": "FilesResult"
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

On success (`200 OK`), the API returns a `FilesResult` object containing the protected file(s) as Base64-encoded content.


#### HTTP Status Codes


#### Example Error Response

```json
{
  "Code": 400,
  "Message": "File is required."
}
```

> **Security Note**: This endpoint requires HTTPS. Using HTTP exposes credentials to interception.

### Request Example (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/protect?password=MySecretPwd" \
  -X POST \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your_jwt_token>" \
  -F 'file=@sample.xlsx'
```

## Best Practices

- **Use HTTPS only** — Never send passwords over unencrypted connections.
- **Store passwords securely** — Use environment variables or secret managers (e.g., AWS Secrets Manager).
- **Validate file types** — Ensure uploaded files are valid Excel workbooks (`.xlsx`, `.xls`, `.xlsm`).
- **Handle Base64 content** — Decode the `FileContent` field before saving to disk.
- **Update SDKs** — Use the latest SDK versions for security patches and feature support.

---

_Last updated: 2024-05-22_

## How to Use the Post Protect API with SDKs?

### Post Protect API Specification

The <a href="https://reference.aspose.cloud/cells/#/Protection/PostProtect" rel="noopener noreferrer">Post Protect API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

Using an SDK simplifies authentication, request construction, and response parsing. The Aspose.Cells Cloud SDKs are open-source and available on [GitHub](https://github.com/aspose-cells-cloud).

### Node.js (JavaScript)

```javascript
// Aspose.Cells Cloud SDK for Node.js v22.5.0
const { CellsApi, PostProtectRequest } = require("aspose-cells-cloud");

const clientId = process.env["CELLS_CLOUD_CLIENT_ID"];
const clientSecret = process.env["CELLS_CLOUD_CLIENT_SECRET"];

const cellsApi = new CellsApi(clientId, clientSecret);

const fileName = "sample.xlsx";
const password = "MySecretPwd";

const request = new PostProtectRequest({
  file: fileName,
  password: password,
});

cellsApi
  .postProtect(request)
  .then((response) => {
    console.log("Protected workbook downloaded.");
    // Handle response.files[0].fileContent (Base64)
  })
  .catch((error) => console.error("Error:", error));
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

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostProtect.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostProtect.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostProtect.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostProtect.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostProtect.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostProtect.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostProtect.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostProtect.go" >}}
{{</tab>}}
{{< /tabs >}}
