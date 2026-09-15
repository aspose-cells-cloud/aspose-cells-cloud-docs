---
title: "Compress Excel Files with Aspose.Cells Cloud API"
second_title: "Aspose.Cells Cloud Documentation"
linktitle: "Compress Spreadsheet"
type: docs
url: /compress-spreadsheet/
description: "Learn how to programmatically compress Excel workbooks using Aspose.Cells Cloud API — reduce file size, optimize storage, and improve transfer performance with configurable compression levels."
keywords: "Excel compression, Aspose.Cells Cloud API, reduce Excel file size, workbook optimization, spreadsheet compression level, cloud Excel compression"
date: 2024-03-15T10:00:00Z
lastmod: 2024-05-22T14:30:00Z
weight: 100
aliases:
  - /excel/compression/
  - /cells/compress-spreadsheet/
---

Compress Excel spreadsheets programmatically with the Aspose.Cells Cloud API to reduce file size, optimize cloud storage usage, and accelerate data transfer. The API supports configurable compression levels (0–9), handles encrypted workbooks, and integrates seamlessly into automated workflows across reporting, data pipelines, and user upload optimization.

## Compress Spreadsheet API Endpoint

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/compress
```

## Authentication

All requests require [JWT token-based authentication](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

```bash
-H "Authorization: Bearer {access_token}"
```

## Request Parameters

| Parameter Name   | Type    | Location     | Required | Description |
|------------------|---------|--------------|----------|-------------|
| `Spreadsheet`    | File    | FormData     | Yes      | The source Excel file (`.xlsx`, `.xls`, `.xlsm`, `.xlsb`, etc.) to compress. |
| `level`          | Integer | Query        | Yes      | Compression intensity: `0` (fastest/lowest compression) to `9` (slowest/highest). Default: `5`. |
| `outPath`        | String  | Query        | No       | Destination folder path in cloud storage. If omitted, output is saved in the source folder. |
| `outStorageName` | String  | Query        | No       | Identifier of the configured cloud storage (e.g., `MyStorage`). |
| `region`         | String  | Query        | No       | Locale setting (e.g., `en-US`, `de-DE`). Affects number/date formatting and locale-sensitive parsing. |
| `password`       | String  | Query        | No       | Password for encrypted workbooks. Omit if file is not protected. |

> **Note**: Though `outStorageName` is marked *Not Required* in the spec, it is strongly recommended for predictable storage routing. Omitting it may result in fallback behavior depending on account configuration.

## Response

The API returns the compressed Excel file as a binary stream.

**Example JSON metadata response (when using SDKs with wrapper):**
```json
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 encoded)",
  "contentType": "application/vnd.openxmlformats-officedocument.spreadsheetml.sheet",
  "fileDownloadName": "compressed_workbook.xlsx"
}
```

### HTTP Status Codes

| Code | Meaning               | Description |
|------|-----------------------|-------------|
| 200  | OK                    | Compression succeeded; response contains the optimized file. |
| 400  | Bad Request           | Invalid or missing parameters (e.g., unsupported file type, invalid `level` range). |
| 401  | Unauthorized          | Missing or invalid JWT token. |
| 404  | Not Found             | Source file not found in cloud storage. |
| 413  | Payload Too Large     | Uploaded file exceeds the 2 GB limit. |
| 500  | Internal Server Error | Unexpected server-side error during processing. |

## Usage Scenarios

- **Automated Report Distribution**  
  Compress monthly financial statements before email delivery to avoid size limits and improve recipient experience.

- **User Upload Optimization**  
  Reduce storage costs and improve upload reliability by compressing user-submitted Excel files in the background.

- **ETL & Data Pipeline Processing**  
  Optimize intermediate Excel files generated during extraction-transform-load workflows to minimize network latency and temporary storage pressure.

## Why Use Aspose.Cells Cloud for Compression?

- ✅ **No infrastructure overhead** — Aspose.Cells Cloud handles server maintenance, updates, and compatibility.  
- ✅ **Configurable compression** — Balance speed and size with compression levels `0`–`9`.  
- ✅ **Pay-per-use pricing** — Only pay for API calls made; no fixed infrastructure costs.  
- ✅ **Multi-language SDK support** — Accelerate development with official SDKs for C#, Java, PHP, Python, Node.js, Ruby, Perl, and Go.  
- ✅ **Encrypted file support** — Compress password-protected workbooks securely via the `password` parameter.

## Getting Started

### cURL Example

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/compress?level=7&outStorageName=MyStorage" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/input.xlsx" \
  --output compressed_output.xlsx
```

### SDK Examples

See the [Aspose.Cells Cloud GitHub repository](https://github.com/aspose-cells-cloud) for the latest SDK versions and pinned examples.

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
```csharp
var cellsApi = new CellsApi(clientId, clientSecret);
var result = cellsApi.CompressSpreadsheet(
    file: File.OpenRead("input.xlsx"),
    level: 6,
    outStorageName: "MyStorage"
);
File.WriteAllBytes("output.xlsx", result.FileContents);
```
{{< /tab >}}
{{< tab tabNum="2" >}}
```java
CellsApi cellsApi = new CellsApi(clientId, clientSecret);
FileInputStream fis = new FileInputStream("input.xlsx");
File compressed = cellsApi.compressSpreadsheet(
    "input.xlsx",
    fis,
    6,
    null,
    "MyStorage",
    null,
    null
);
```
{{< /tab >}}
{{< tab tabNum="3" >}}
```php
$cellsApi = new CellsApi($clientId, $clientSecret);
$response = $cellsApi->compressSpreadsheet(
    "input.xlsx",
    fopen("input.xlsx", "r"),
    6,
    null,
    "MyStorage",
    null,
    null
);
file_put_contents("output.xlsx", $response->fileContents);
```
{{< /tab >}}
{{< tab tabNum="4" >}}
```ruby
cells_api = AsposeCellsCloud::CellsApi.new(client_id, client_secret)
result = cells_api.compress_spreadsheet(
  'input.xlsx',
  File.open('input.xlsx', 'rb'),
  level: 6,
  out_storage_name: 'MyStorage'
)
File.write('output.xlsx', result.file_contents)
```
{{< /tab >}}
{{< tab tabNum="5" >}}
```typescript
import { CellsApi } from "@aspose/cells-cloud";
const cellsApi = new CellsApi(process.env.CLIENT_ID!, process.env.CLIENT_SECRET!);
const result = await cellsApi.compressSpreadsheet(
  "input.xlsx",
  fs.createReadStream("input.xlsx"),
  6,
  undefined,
  "MyStorage"
);
fs.writeFileSync("output.xlsx", Buffer.from(result.fileContents!));
```
{{< /tab >}}
{{< tab tabNum="6" >}}
```python
from asposecellscloud.api import CellsApi
from asposecellscloud.models import CompressionRequest

api = CellsApi(client_id, client_secret)
with open("input.xlsx", "rb") as f:
    result = api.compress_spreadsheet(
        file=f,
        level=6,
        out_storage_name="MyStorage"
    )
with open("output.xlsx", "wb") as f:
    f.write(result.file_contents)
```
{{< /tab >}}
{{< tab tabNum="7" >}}
```perl
my $api = AsposeCellsCloud::API->new(
    client_id => $clientId,
    client_secret => $clientSecret
);
my $result = $api->cells_compress_spreadsheet(
    'input.xlsx',
    'r',
    6,
    undef,
    'MyStorage'
);
```
{{< /tab >}}
{{< tab tabNum="8" >}}
```go
import (
    "os"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v43/api"
)

cellsApi, _ := api.NewCellsApiWithBasePath(
    os.Getenv("CLIENT_ID"),
    os.Getenv("CLIENT_SECRET"),
    "https://api.aspose.cloud",
)
resp, _, err := cellsApi.CompressSpreadsheet(
    context.Background(),
    "input.xlsx",
    6,
    "",
    "MyStorage",
    "",
    "",
)
```
{{< /tab >}}
{{< /tabs >}}

## Best Practices

- **Choose compression level wisely**:  
  - Use `level=0` or `1` for near-real-time processing where speed matters.  
  - Use `level=7`–`9` for archival or batch processing where size reduction is critical.  
- **Validate input files**: Ensure files are valid Excel formats before upload to avoid `400` errors.  
- **Handle locale explicitly**: Specify `region` when formatting-sensitive data (dates, currencies) is involved.  
- **Secure sensitive workbooks**: Always use `password` for protected files — never hardcode credentials.

## Related Resources

- [Encrypt Excel Files](/cells/encrypt-spreadsheet/) — Protect your compressed outputs with password encryption.  
- [SDK Developer Guide](/total/developer-guide/) — Learn to integrate Aspose.Cells Cloud SDKs in your stack.  
- [ETL Integration Patterns](/cells/etl-integration/) — Build scalable data pipelines with compressed spreadsheets.  
- [API Reference](https://reference.aspose.cloud/cells/#/ManagementController/CompressSpreadsheet) — Full endpoint specification and schema details.  

## Support & Feedback

For issues, questions, or feature requests:  
- Visit the [Aspose.Cells Cloud Forum](https://forum.aspose.cloud/c/cells/13)  
- Report bugs via the [GitHub Issues page](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet/issues)  
- Contact support: [support@aspose.cloud](mailto:support@aspose.cloud)