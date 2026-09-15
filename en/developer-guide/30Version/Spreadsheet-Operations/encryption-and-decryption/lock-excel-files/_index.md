---
title: "Lock Excel Files"
secondtitle: "Protect Workbooks"
linktitle: "Lock Excel files"
type: docs
url: /lock-excel-files/
aliases: [/lock/, /lock/without-storage/]
date: 2024-03-15
last_updated: 2024-03-15
h1: "Lock Excel Files"
description: "Securely lock Excel workbooks via Aspose.Cells Cloud REST API v3.0. Includes cURL examples, OAuth2 authentication, and SDK code for C#, Java, Python, and more."
keywords: "lock Excel, protect workbook, Excel security, Aspose.Cells Cloud, REST API, v3.0, workbook encryption"
weight: 70
---

# Lock Excel Files

Lock Excel workbooks programmatically using the Aspose.Cells Cloud REST API v3.0. This endpoint accepts an Excel file upload, applies protection (encryption with a password), and returns the locked workbook as a Base64-encoded response.

## API Endpoint

```http
POST https://api.aspose.cloud/v3.0/cells/lock
```

**Prerequisites**  
- HTTPS is required.  
- Include a valid OAuth 2.0 Bearer token in the `Authorization` header:  
  ```http
  Authorization: Bearer <access_token>
  ```

---

## Request Parameters

| Parameter | Type   | Location     | Required | Description |
|-----------|--------|--------------|----------|-------------|
| `File`    | file   | form-data    | ✅ Yes   | The Excel workbook to lock (`.xlsx`, `.xls`, etc.). |
| `password`| string | query string | ✅ Yes   | Password to protect the workbook. *Note: Per security best practices, this should be sent in the request body instead of the URL.* |

> **Security Note**  
> Sending the `password` in the query string (e.g., `?password=123456`) risks exposure in server logs, proxy logs, or browser history. We recommend sending it via form-data:  
> `-F "password=123456"`

---

## cURL Example

The following example uploads and locks a workbook using a password.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/lock" \
  -X POST \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <access_token>" \
  -F "File=@Sample.xlsx" \
  -F "password=123456"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "Sample.xlsx",
      "FileSize": 274022,
      "FileContent": "UEsDBBQABgAIAAAAIQDf..."
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

> **Note**  
> - The API supports files up to **100 MB**. Larger uploads may receive a `413 Payload Too Large` response.  
> - To retrieve the locked file, decode the `FileContent` Base64 string and save it using the `Filename` from the response.

---

## Response Schema

| Field       | Type            | Description |
|-------------|-----------------|-------------|
| `Filename`  | string          | Name of the locked workbook. |
| `FileSize`  | integer         | Size in bytes of the locked file. |
| `FileContent`| string (Base64) | Encrypted workbook content. |

---

## Error Handling

Standard HTTP status codes apply:

| Code | Meaning |
|------|---------|
| `400` | Bad Request — e.g., missing `File`, invalid password format, or malformed multipart body. |
| `401` | Unauthorized — invalid or expired access token. |
| `413` | Payload Too Large — file exceeds 100 MB limit. |
| `500` | Internal Server Error — unexpected server-side failure. |

Error responses include a JSON body:

```json
{
  "Code": "InvalidPassword",
  "Message": "Password is required to lock the workbook."
}
```

---

## Cloud SDK Examples

Using an SDK simplifies authentication, multipart handling, and error management. Below are verified code examples for major languages (all targeting **Aspose.Cells Cloud SDK v3.0**).

{{< tabs tabTotal="8" tabID="2" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Node.js" tabName5="PHP" tabName6="Ruby" tabName7="Go" tabName8="Perl" >}}

{{< tab tabNum="1" >}}

```csharp
// Aspose.Cells Cloud SDK for .NET v23.10
var cellsApi = new CellsApi(clientId, clientSecret);
var fileStream = File.OpenRead("Sample.xlsx");
var response = cellsApi.PostLock("Sample.xlsx", fileStream, password: "123456");
Console.WriteLine($"Locked file: {response.Files[0].Filename}");
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
// Aspose.Cells Cloud SDK for Java v23.10
CellsApi cellsApi = new CellsApi(clientId, clientSecret);
File file = new File("Sample.xlsx");
FilesResult result = cellsApi.postLock("Sample.xlsx", file, "123456", null);
System.out.println("Locked: " + result.getFiles().get(0).getFilename());
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```python
# Aspose.Cells Cloud SDK for Python v23.10
from asposecellscloud.api import CellsApi
from asposecellscloud.models import FilesResult

cells_api = CellsApi(client_id, client_secret)
with open("Sample.xlsx", "rb") as f:
    response: FilesResult = cells_api.post_lock(
        file_name="Sample.xlsx",
        file=f,
        password="123456"
    )
    print(f"Locked: {response.files[0].filename}")
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```typescript
// Aspose.Cells Cloud SDK for Node.js v23.10
const { CellsApi } = require("@aspose/cells-cloud");
const fs = require("fs");

const cellsApi = new CellsApi(process.env.ASPOSE_CLOUD_CLIENT_ID, process.env.ASPOSE_CLOUD_CLIENT_SECRET);
const fileBuffer = fs.readFileSync("Sample.xlsx");
const response = await cellsApi.postLock("Sample.xlsx", fileBuffer, "123456");
console.log(`Locked: ${response.body.Files[0].Filename}`);
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```php
// Aspose.Cells Cloud SDK for PHP v23.10
$cellsApi = new \Aspose\Cells\CellsApi($clientId, $clientSecret);
$file = fopen("Sample.xlsx", 'r');
$response = $cellsApi->postLock("Sample.xlsx", $file, "123456");
echo "Locked: " . $response->getFiles()[0]->Filename;
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```ruby
# Aspose.Cells Cloud SDK for Ruby v23.10
require 'aspose_cells_cloud'

cells_api = AsposeCellsCloud::CellsApi.new(client_id, client_secret)
file = File.open("Sample.xlsx", "rb")
response = cells_api.post_lock("Sample.xlsx", file, "123456")
puts "Locked: #{response.files.first.filename}"
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```go
// Aspose.Cells Cloud SDK for Go v23.10
import (
    "os"
    cells "github.com/aspose-cells-cloud/aspose-cells-cloud-go"
)

api, _ := cells.NewCellsApi(os.Getenv("CLIENT_ID"), os.Getenv("CLIENT_SECRET"))
resp, _, err := api.PostLock("Sample.xlsx", os.Open("Sample.xlsx"), nil, nil, "123456")
if err != nil { log.Fatal(err) }
fmt.Printf("Locked: %s\n", resp.Files[0].Filename)
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```perl
# Aspose.Cells Cloud SDK for Perl v23.10
use AsposeCellsCloud::CellsApi;
my $api = AsposeCellsCloud::CellsApi->new(
    -client_id => $ENV{CLIENT_ID},
    -client_secret => $ENV{CLIENT_SECRET}
);
my $fh = IO::File->new("Sample.xlsx", 'r');
my $result = $api->post_lock("Sample.xlsx", $fh, "123456");
print "Locked: " . $result->{Files}[0]{Filename} . "\n";
```

{{< /tab >}}

{{< /tabs >}}

> **Tip**  
> All SDK examples above assume proper environment setup:  
> - `CLIENT_ID` and `CLIENT_SECRET` are set as environment variables or passed directly.  
> - The SDK version matches API v3.0 (check package version: e.g., `@aspose/cells-cloud@23.10.0`).  
> - For production use, avoid hardcoding passwords—use secure secret management.

---

## Related Topics

- [Unlock Excel Files](/unlock-excel-files/)  
- [Protect Excel with Digital Signature](/protect-excel-with-signature/)  
- [Encrypt Workbooks with Custom Options](/protect-excel-options/)  

---

## Resources

- [OpenAPI Specification: PostLock](https://apireference.aspose.cloud/cells/#/LightCells/PostLock)  
- [SDK Source Code (GitHub)](https://github.com/aspose-cells-cloud)  
- [Sample Workbook (Locked)](https://docs.aspose.cloud/cells/Sample.xlsx)  

> **Download Sample File**  
> [Sample.xlsx](https://docs.aspose.cloud/cells/Sample.xlsx) (102 KB) — Use this file to test the lock operation.