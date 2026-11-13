---
title: "Unlock Excel Files"
second_title: "Developer Guide"
linktitle: "Unlock Excel Files"
type: docs
url: /unlock-excel-files/
aliases: [/unlock/without-storage/, /unlock/, /unlock/without-using-storage/]
keywords: "Unlock Excel, Aspose.Cells Cloud, REST API, Excel unlocking, password-protected workbook, SDK, C#, Java, Python, Node.js, Go, PHP, Ruby, Swift"
description: "Unlock password-protected Excel files via Aspose.Cells Cloud REST API using JWT, cURL, or SDKs for major languages."
date: 2024-05-10
last_updated: May 10, 2024
weight: 70
ArticleTitle: "Unlock Password-Protected Excel Files with Aspose.Cells Cloud REST API"
---
The **PostUnlock** API (`POST https://api.aspose.cloud/v3.0/cells/unlock`) in Aspose.Cells Cloud unlocks password-protected Excel files by accepting the encrypted file and its password as inputs, enabling secure removal of protection in a single request.

## The Post Unlock Web API

```http
POST https://api.aspose.cloud/v3.0/cells/unlock
```

### Security and Authentication

The Aspose.Cells Cloud APIs use [JWT token-based authentication](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/rel="noopener noreferrer" target="\_blank"). Ensure you include a valid bearer token in the `Authorization` header.

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| File | File | FormData | File to upload |
| password | String | Query | The password needed to open an Excel file. |

> ⚠️ **Security Note**  
> Passing passwords via query parameters is insecure—they may appear in server logs, browser history, or proxy logs. We strongly recommend using environment variables or secure vaults (e.g., AWS Secrets Manager, HashiCorp Vault) to manage credentials. For enhanced security, consider moving sensitive parameters to headers (e.g., `X-Password`) in your client implementation.

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

On successful unlock, the API returns a `FilesResult` object containing the decrypted files:


| Field    | Type    | Description                                                                                             |
| -------- | ------- | ------------------------------------------------------------------------------------------------------- |
| `Files`  | Array   | Array of unlocked files (each with `Filename`, `FileSize`, `FileContent`, and optionally `FileFormat`). |
| `Code`   | integer | HTTP status code (e.g., 200).                                                                           |
| `Status` | string  | Status message ("OK" on success).                                                                       |

#### HTTP Status Codes


---

### Request Examples

#### cURL (Secure Pattern)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/unlock" \
  -X POST \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your_jwt_token>" \
  -H "X-Password: ${ASPOSE_PASSWORD}" \
  -F 'file=@sample_protected.xlsx'
```

> ✅ **Best Practice**: Use environment variables (`${ASPOSE_PASSWORD}`) instead of hardcoding passwords.

#### cURL (Legacy — Not Recommended)

```bash
# ❗ Avoid: Password exposed in URL and logs
curl -v "https://api.aspose.cloud/v3.0/cells/unlock?password=123456" \
  -X POST \
  -H "Authorization: Bearer <your_jwt_token>" \
  -F 'file=@sample_protected.xlsx'
```

## Best Practices & Security Recommendations

1. **Use Secure Credential Storage**  
   Store API credentials and passwords in environment variables, vaults, or secure configuration services—not in source code.

2. **Prefer POST Body for Sensitive Data**  
   Where supported, pass passwords in headers (e.g., `X-Password`) instead of query parameters.

3. **Validate File Formats**  
   Only upload `.xlsx`, `.xls`, `.xlsm`, `.xlsb`, or `.ods` files to avoid errors.

4. **Handle Large Files**  
   For files >1 GB, consider chunked upload or server-side decryption (if available).

5. **Audit Logs**  
   Log only non-sensitive metadata (e.g., file size, timestamp)—never passwords or base64 content.

---

## Related Topics

- [Encrypt Excel Files](/encrypt-excel-files/)
- [Aspose.Cells Cloud SDK Overview](/cells-cloud-sdks/)
- [Bulk Workbook Operations](/bulk-operations/)

---

_Last updated: May 10, 2024_

## How to Use the Post Unlock API with SDKs?

### Post Unlock API Specification

The <a href="https://reference.aspose.cloud/cells/#/Protection/PostUnlock" rel="noopener noreferrer">Post Unlock API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

Using an SDK is the recommended approach to accelerate development and handle low-level details like authentication, multipart encoding, and error handling.

### SDK Requirements

- SDK version must be compatible with **API v3.0**.
- Check the [SDK Changelog](https://github.com/aspose-cells-cloud) for version-specific features and compatibility.

### Supported SDKs

The following SDKs support the `PostUnlock` operation:

{{< tabs tabTotal="8" tabID="sdk-tabs" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// Install: nuget install Aspose.Cells-Cloud
using Aspose.Cells.Cloud.Sdk.Api;
using Aspose.Cells.Cloud.Sdk.Model;

var cellsApi = new CellsApi("your_client_id", "your_client_secret");
var result = await cellsApi.PostUnlockAsync(
    file: "sample.xlsx",
    password: Environment.GetEnvironmentVariable("ASPOSE_PASSWORD")
);
Console.WriteLine($"Unlocked {result.Files.Count} file(s).");
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
// Install: Add aspose-cells-cloud JAR to classpath
import com.aspose.cells.cloud.*;

ApiClient client = new ApiClient("your_client_id", "your_client_secret", null);
CellsApi api = new CellsApi(client);
FilesResult result = api.postUnlock(
    "sample.xlsx",
    System.getenv("ASPOSE_PASSWORD"),
    null,
    null
);
System.out.println("Unlocked " + result.getFiles().size() + " file(s).");
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
<?php
require_once('vendor/autoload.php');
use Aspose\Cells\CellsApi;

$cellsApi = new CellsApi(getenv('ASPOSE_CLOUD_CLIENT_ID'), getenv('ASPOSE_CLOUD_CLIENT_SECRET'));
$result = $cellsApi->PostUnlock("sample.xlsx", getenv('ASPOSE_PASSWORD'));
echo "Unlocked " . count($result->Files) . " file(s).\n";
?>
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
# Install: gem install aspose_cells_cloud
require 'aspose_cells_cloud'

api = AsposeCellsCloud::CellsApi.new(
  ENV['ASPOSE_CLOUD_CLIENT_ID'],
  ENV['ASPOSE_CLOUD_CLIENT_SECRET']
)
result = api.post_unlock(file: 'sample.xlsx', password: ENV['ASPOSE_PASSWORD'])
puts "Unlocked #{result.files.count} file(s)."
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```javascript
// Install: npm install aspose-cells-cloud
const { CellsApi } = require("aspose-cells-cloud");

const cellsApi = new CellsApi(
  process.env.ASPOSE_CLOUD_CLIENT_ID,
  process.env.ASPOSE_CLOUD_CLIENT_SECRET,
);

const result = await cellsApi.postUnlock("sample.xlsx", {
  password: process.env.ASPOSE_PASSWORD,
});
console.log(`Unlocked ${result.body.Files.length} file(s).`);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```python
# Install: pip install asposecellscloud
from asposecellscloud.api import CellsApi
from asposecellscloud.models import FilesResult

api = CellsApi(
    client_id=os.getenv('ASPOSE_CLOUD_CLIENT_ID'),
    client_secret=os.getenv('ASPOSE_CLOUD_CLIENT_SECRET')
)
result: FilesResult = api.post_unlock(file='sample.xlsx', password=os.getenv('ASPOSE_PASSWORD'))
print(f"Unlocked {len(result.files)} file(s).")
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```perl
use AsposeCellsCloud::CellsApi;
my $api = AsposeCellsCloud::CellsApi->new(
    -client_id => $ENV{ASPOSE_CLOUD_CLIENT_ID},
    -client_secret => $ENV{ASPOSE_CLOUD_CLIENT_SECRET}
);
my $result = $api->post_unlock(file => 'sample.xlsx', password => $ENV{ASPOSE_PASSWORD});
print "Unlocked " . scalar(@{$result->{Files}}) . " file(s).\n";
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```go
// Install: go get github.com/aspose-cells-cloud/aspose-cells-cloud-go
import (
  "context"
  "os"
  "github.com/aspose-cells-cloud/aspose-cells-cloud-go"
)

cellsApi := cells.NewCellsApi(os.Getenv("ASPOSE_CLOUD_CLIENT_ID"), os.Getenv("ASPOSE_CLOUD_CLIENT_SECRET"))
filesResult, _, err := cellsApi.PostUnlock(context.Background(), "sample.xlsx", &cells.PostUnlockOptions{
  Password: os.Getenv("ASPOSE_PASSWORD"),
})
if err != nil {
  log.Fatal(err)
}
fmt.Printf("Unlocked %d file(s).\n", len(filesResult.Files))
```

{{< /tab >}}

{{< /tabs >}}

### Notes for SDK Users

- ✅ All SDK examples use environment variables (`ASPOSE_PASSWORD`, `ASPOSE_CLOUD_CLIENT_ID`, etc.) for credentials—**never hardcode secrets**.
- ✅ The `file` parameter accepts local file paths; the SDK handles upload and multipart encoding.
- ✅ Multiple files can be passed in a single call (e.g., `files = ["a.xlsx", "b.xlsx"]` in Python).
- 🔍 Verify SDK version compatibility: Check the [GitHub Releases](https://github.com/aspose-cells-cloud) for version-specific changes.

---

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUnlock.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUnlock.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUnlock.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUnlock.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUnlock.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUnlock.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUnlock.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUnlock.go" >}}
{{</tab>}}
{{< /tabs >}}
