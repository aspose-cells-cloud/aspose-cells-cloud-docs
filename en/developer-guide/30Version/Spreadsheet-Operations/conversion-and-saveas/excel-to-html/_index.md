---
title: Convert Excel to HTML
description: Convert an Excel workbook (XLSX, XLS, CSV, etc.) to HTML using Aspose.Cells Cloud API v3.0. Includes cURL examples, SDK support for 8+ languages, and comprehensive error handling.
date: 2024-10-01
lastmod: 2026-03-20
draft: false
tags: ["excel", "html", "conversion", "api"]
categories: ["cells", "conversion"]
weight: 100
canonical: https://docs.aspose.cloud/cells/convert-excel-file-to-html-file/
robots: index,follow
---

Aspose.Cells Cloud provides a robust REST endpoint that converts Excel workbooks (XLS, XLSX, CSV, etc.) into HTML documents. The operation returns a **FileInfo** object containing the generated HTML file (name, size, and Base64‑encoded content).

## Convert Excel Workbooks to HTML Web API

```
POST https://api.aspose.cloud/v3.0/cells/convert/html
```

> **Note**: The request must be sent as `multipart/form-data`. The Excel file is the first part of the multipart body.

## Request Parameters

### Query Parameters

| Name                    | Type    | Required | Default | Description                                                                              |
| ----------------------- | ------- | -------- | ------- | ---------------------------------------------------------------------------------------- |
| `password`              | string  | No       | –       | Password to open a protected workbook.                                                   |
| `storageName`           | string  | No       | –       | Name of the storage where the source file resides.                                       |
| `checkExcelRestriction` | boolean | No       | `true`  | When `true`, the service validates Excel‑specific restrictions (e.g., protected sheets). |
| `region`                | string  | No       | –       | Regional settings for the workbook (e.g., `en-US`).                                      |
| `FontsLocation`         | string  | No       | –       | URL or path to a folder that contains custom fonts required for rendering.               |

### Form‑Data (Multipart)

| Name     | Type | Required | Description                                                                                      |
| -------- | ---- | -------- | ------------------------------------------------------------------------------------------------ |
| **File** | file | **Yes**  | The Excel workbook to be converted. Must be supplied as the first part of the multipart request. |

## Request Examples

### cURL

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/html?checkExcelRestriction=true&region=en-US" \
     -H "accept: multipart/form-data" \
     -H "Authorization: Bearer <access-token>" \
     -H "Content-Type: multipart/form-data" \
     -F "File=@/path/to/your_workbook.xlsx"
```

## Successful Response

**Status Code:** `200 OK`

| Field         | Type   | Description                                             |
| ------------- | ------ | ------------------------------------------------------- |
| `Filename`    | string | Name of the generated HTML file (e.g., `example.html`). |
| `FileSize`    | int    | Size of the HTML file in bytes.                         |
| `FileContent` | string | Base64‑encoded HTML content.                            |

```json
{
  "Filename": "example.html",
  "FileSize": 12345,
  "FileContent": "base64_encoded_string"
}
```

The response schema is defined by the **FileInfo** model: [/cells/file-info](/cells/file-info/).

## Error Responses

| Code  | Meaning                                                    | Example Payload                                                                                   |
| ----- | ---------------------------------------------------------- | ------------------------------------------------------------------------------------------------- |
| `400` | Bad Request – missing/invalid parameters                   | `{ "Code": "BadRequest", "Message": "The 'File' part is required." }`                             |
| `401` | Unauthorized – invalid or missing JWT token                | `{ "Code": "InvalidToken", "Message": "Access token is missing or expired." }`                    |
| `404` | Not Found – source file not found in the specified storage | `{ "Code": "FileNotFound", "Message": "File 'my.xlsx' does not exist in storage 'MyStorage'." }`  |
| `413` | Payload Too Large – uploaded file exceeds the allowed size | `{ "Code": "RequestEntityTooLarge", "Message": "Uploaded file exceeds the 100 MB limit." }`       |
| `429` | Too Many Requests – rate limit exceeded                    | `{ "Code": "TooManyRequests", "Message": "Rate limit of 60 calls per minute exceeded." }`         |
| `500` | Internal Server Error – unexpected server condition        | `{ "Code": "InternalError", "Message": "An unexpected error occurred. Please try again later." }` |

## Rate Limits

| Limit                                            | Description                                                                                                                           |
| ------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------- |
| **60 requests per minute** per account (default) | Exceeding this limit returns `429 Too Many Requests`. Adjust your client logic or request a higher quota via the Aspose Cloud portal. |

## Use Cases

- **Web Archiving**: Convert Excel reports to HTML for long-term preservation in web-friendly formats.
- **Legacy System Integration**: Embed Excel data into older web applications without client-side dependencies.
- **Automated Reporting**: Generate dynamic HTML dashboards from Excel templates via CI/CD pipelines.

## Related Endpoints

| Endpoint                    | Description                                                                                   |
| --------------------------- | --------------------------------------------------------------------------------------------- |
| `POST /cells/{name}/saveAs` | Save an existing Excel file as HTML (or other formats) directly to storage.                   |
| `GET /cells/{name}`         | Retrieve a workbook already stored as HTML (or other formats) with optional query parameters. |

### SDK Examples

#### C#

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var apiInstance = new ConversionApi();
var file = File.ReadAllBytes("your.xlsx");
var result = apiInstance.PostConvertWorkbookToHtml(
    file,
    password: null,
    checkExcelRestriction: true,
    region: "en-US",
    fontsLocation: "/fonts"
);
Console.WriteLine(result.Filename);
```

#### Java

```java
ConversionApi api = new ConversionApi();
File file = new File("your.xlsx");
FileInfo info = api.postConvertWorkbookToHtml(
    file,
    null,
    true,
    "en-US",
    "/fonts"
);
System.out.println(info.getFilename());
```

#### Python

```python
from asposecellscloud import ConversionApi

api = ConversionApi()
with open('your.xlsx', 'rb') as f:
    file_info = api.post_convert_workbook_to_html(
        file=f.read(),
        password=None,
        check_excel_restriction=True,
        region="en-US",
        fonts_location="/fonts"
    )
print(file_info.filename)
```

#### Node.js

```javascript
const { ConversionApi } = require("asposecellscloud");
const fs = require("fs");

const api = new ConversionApi();
api
  .postConvertWorkbookToHtml({
    File: fs.createReadStream("your.xlsx"),
    password: null,
    checkExcelRestriction: true,
    region: "en-US",
    fontsLocation: "/fonts",
  })
  .then((info) => console.log(info.Filename));
```

#### Go

```go
import (
    "fmt"
    "os"

    "asposecellscloud"
)

func main() {
    api := asposecellscloud.NewConversionApi()
    f, _ := os.Open("your.xlsx")
    info, _ := api.PostConvertWorkbookToHtml(
        f,
        nil,
        true,
        "en-US",
        "/fonts"
    )
    fmt.Println(info.Filename)
}
```

#### PHP

```php
use Aspose\Cells\ConversionApi;

$api = new ConversionApi();
$file = fopen('your.xlsx', 'r');
$info = $api->postConvertWorkbookToHtml(
    $file,
    null,
    true,
    "en-US",
    "/fonts"
);
echo $info->getFilename();
```

#### Ruby

```ruby
require 'aspose_cells_cloud'

api = AsposeCellsCloud::ConversionApi.new
file = File.open('your.xlsx')
info = api.post_convert_workbook_to_html(
  file: file,
  password: nil,
  check_excel_restriction: true,
  region: 'en-US',
  fonts_location: '/fonts'
)
puts info.filename
```

#### Perl

```perl
use Aspose::Cells::ConversionApi;

my $api = Aspose::Cells::ConversionApi->new();
open my $fh, '<', 'your.xlsx' or die $!;
my $info = $api->post_convert_workbook_to_html(
  file => $fh,
  password => undef,
  check_excel_restriction => 1,
  region => 'en-US',
  fonts_location => '/fonts'
);
print $info->{Filename};
```

> **Tip**: For full SDK installation instructions, see the [Aspose.Cells Cloud SDKs repository](https://github.com/aspose-cells-cloud).
