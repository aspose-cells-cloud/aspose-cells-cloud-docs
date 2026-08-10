---
title: "Convert Excel Range to Image – Aspose.Cells Cloud API"
description: "Convert a specific range from a local Excel file to PNG, JPEG, SVG, TIFF, or BMP via Aspose.Cells Cloud REST API – no full workbook upload required."
keywords: "Aspose.Cells Cloud, Convert Range to Image, Excel API, Image Formats, PNG, JPEG, SVG, TIFF, BMP"
slug: convert-range-to-image
api_version: "v4.0"
date: 2026-07-30
---

# Convert a Specific Excel Range to an Image File  
*Step‑by‑Step Guide*

![Aspose.Cells Cloud – Convert Range to Image example](/cells/images/Aspose-image-for-open-graph.jpg "Aspose.Cells Cloud – Convert Range to Image example")

---

## Table of Contents
1. [Prerequisites](#prerequisites)  
2. [Authentication](#authentication)  
3. [Endpoint & HTTP Method](#endpoint--http-method)  
4. [Request Parameters](#request-parameters)  
5. [cURL Example](#curl-example)  
6. [SDK Code Samples](#sdk-code-samples)  
7. [Response](#response)  
8. [Error Handling](#error-handling)  
9. [Best Practices & Notes](#best-practices--notes)  
10. [Related Topics](#related-topics)  

---

## Prerequisites
| Requirement | Details |
|-------------|---------|
| **JWT Access Token** | Obtain a JWT token using your **Client Id** and **Client Secret**. See the [authentication guide](/getting-started/rest-api-overview/authenticating-api-requests/). |
| **Supported Excel Versions** | Excel 97‑2003 (`.xls`) and Excel 2007+ (`.xlsx`, `.xlsm`). |
| **Image Formats** | PNG, JPEG, SVG, TIFF, BMP. |
| **Network** | Outbound HTTPS access to `api.aspose.cloud`. |
| **Permissions** | The token must have **Cells** scope. |

---

## Authentication
All requests must include the JWT token in the `Authorization` header:

```http
Authorization: Bearer {access_token}
```

> **Tip:** Store the token securely and refresh it before expiration (default 1 hour).

---

## Endpoint & HTTP Method
```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/image
```

The call reads a local spreadsheet file, converts the specified range, and returns the image as a binary stream.

---

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

## Request Parameters  

| Name | Location | Type | Required | Description |
|------|----------|------|----------|-------------|
| **Spreadsheet** | Form‑Data (`multipart/form-data`) | File | **Yes** | The Excel file to be processed. |
| **worksheet** | Query | String | **Yes** | Worksheet name that contains the range (e.g., `Sheet1`). |
| **range** | Query | String | **Yes** | Cell area to convert, e.g., `A1:C10`. |
| **format** | Query | String | **Yes** | Output image format (`png`, `jpeg`, `svg`, `tiff`, `bmp`). |
| **printHeadings** | Query | Boolean | No | `true` to include row/column headings in the image. |
| **outPath** | Query | String | No | Folder path for the generated file if you want to store it in cloud storage. |
| **outStorageName** | Query | String | No | Name of the storage service (e.g., `MyStorage`). |
| **fontsLocation** | Query | String | No | URL or path to custom fonts used during conversion. |
| **region** | Query | String | No | Locale identifier (e.g., `en-US`, `fr-FR`). Affects number and date formatting. |
| **password** | Query | String | No | Password for encrypted workbooks. |
| **AutoRowsFit** | Query | Boolean | No | Auto‑fit rows before rendering. |
| **AutoColumnsFit** | Query | Boolean | No | Auto‑fit columns before rendering. |

> **Note:** All query parameters are case‑sensitive.

---

## cURL Example
```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/range/image?worksheet=Sheet1&range=A1:C10&format=png&printHeadings=true" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@/path/to/your/file.xlsx"
```

The response body contains the binary image (`Content-Type: image/png` in this example).

---

## SDK Code Samples  

Below are minimal snippets for the most popular languages. All SDKs are available on the [Aspose.Cells Cloud GitHub repo](https://github.com/aspose-cells-cloud).

### C# (.NET)
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model.Requests;
using System.IO;

var apiInstance = new ConversionApi();
var request = new ConvertRangeToImageRequest(
    file: File.OpenRead("sample.xlsx"),
    worksheet: "Sheet1",
    range: "A1:C10",
    format: "png",
    printHeadings: true,
    outPath: null,
    outStorageName: null,
    fontsLocation: null,
    region: "en-US",
    password: null,
    autoRowsFit: null,
    autoColumnsFit: null
);
var response = apiInstance.ConvertRangeToImage(request);
File.WriteAllBytes("range.png", response);
```

### Java
```java
ConversionApi api = new ConversionApi();
ConvertRangeToImageRequest request = new ConvertRangeToImageRequest()
        .file(new File("sample.xlsx"))
        .worksheet("Sheet1")
        .range("A1:C10")
        .format("png")
        .printHeadings(true);
byte[] image = api.convertRangeToImage(request);
Files.write(Paths.get("range.png"), image);
```

### Python
```python
from asposecellscloud.apis.conversion_api import ConversionApi
from asposecellscloud.models import ConvertRangeToImageRequest
import pathlib

api = ConversionApi()
request = ConvertRangeToImageRequest(
    file=pathlib.Path("sample.xlsx"),
    worksheet="Sheet1",
    range="A1:C10",
    format="png",
    print_headings=True
)
result = api.convert_range_to_image(request)
with open("range.png", "wb") as f:
    f.write(result)
```

### Node.js (TypeScript)
```typescript
import { ConversionApi, ConvertRangeToImageRequest } from "asposecellscloud";

const api = new ConversionApi();
const request = new ConvertRangeToImageRequest({
    file: fs.createReadStream("sample.xlsx"),
    worksheet: "Sheet1",
    range: "A1:C10",
    format: "png",
    printHeadings: true
});
api.convertRangeToImage(request).then((data) => {
    fs.writeFileSync("range.png", data);
});
```

### PHP
```php
<?php
require_once __DIR__ . '/vendor/autoload.php';

use Aspose\Cells\Cloud\Api\ConversionApi;
use Aspose\Cells\Cloud\Model\ConvertRangeToImageRequest;

$api = new ConversionApi();
$request = new ConvertRangeToImageRequest([
    "file" => fopen("sample.xlsx", "r"),
    "worksheet" => "Sheet1",
    "range" => "A1:C10",
    "format" => "png",
    "printHeadings" => true
]);
$image = $api->convertRangeToImage($request);
file_put_contents("range.png", $image);
?>
```

*(Samples for Ruby, Perl, and Go are available in the repository.)*

---

## Response
| Status | Content-Type | Body |
|--------|--------------|------|
| **200 OK** | `image/png`, `image/jpeg`, `image/svg+xml`, `image/tiff`, or `image/bmp` (depending on `format`) | Binary image stream. |
| **200 OK** (JSON metadata) | `application/json` | `{ "Name": "range.png", "Size": 12456 }` *(when `outPath` is specified and the file is stored in cloud storage)* |

The `Content-Disposition` header contains the generated file name.

---

## Error Handling
| HTTP Code | Meaning |
|-----------|---------|
| **400 Bad Request** | Invalid URI or missing required parameters. |
| **401 Unauthorized** | Invalid or expired JWT token. |
| **404 Not Found** | The supplied spreadsheet cannot be accessed. |
| **500 Internal Server Error** | Server‑side processing failure (e.g., unsupported cell features). |

Error responses follow the standard Aspose error model:

```json
{
  "Code": "InvalidParameter",
  "Message": "The 'range' parameter is malformed."
}
```

---

## Best Practices & Notes
- **Secure the token** – never expose it in client‑side code or public repositories.  
- **Limit range size** – extremely large ranges may increase conversion time and memory usage.  
- **Encrypted workbooks** – provide the `password` query parameter; otherwise the request fails with `401`.  
- **Locale‑aware rendering** – use the `region` parameter to match the workbook’s language settings (e.g., dates, decimal separators).  
- **Headings** – set `printHeadings=true` when you need Excel‑style row/column labels in the image.  
- **Storage option** – if you specify `outPath` and `outStorageName`, the image is saved to cloud storage and a JSON metadata object is returned instead of a binary stream.  
- **Performance** – reuse the same JWT token for multiple calls within its lifetime to avoid unnecessary token requests.  

---

## Related Topics
- [Convert Worksheet to Image](/convert-worksheet-to-image/)  
- [Export Spreadsheet as PDF](/export-to-pdf/)  
- [Working with Password‑Protected Workbooks](/workbooks/password-protection/)  
- [Using Custom Fonts in Conversions](/fonts/custom-fonts/)  

--- 

*Document last updated on 2026‑07‑30.*