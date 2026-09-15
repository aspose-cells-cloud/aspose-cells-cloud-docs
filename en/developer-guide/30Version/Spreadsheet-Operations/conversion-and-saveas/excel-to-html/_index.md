---
title: Convert Excel to HTML
description: Convert an Excel workbook (XLSX, XLS, CSV, etc.) to HTML using Aspose.Cells Cloud API v3.0. Includes cURL examples, SDK support for 8+ languages, and comprehensive error handling.
date: 2024-10-01
lastmod: 2026-03-20
draft: false
tags: ["excel", "html", "conversion", "api"]
categories: ["cells", "conversion"]
weight: 20
canonical: https://docs.aspose.cloud/cells/convert-excel-file-to-html-file/
robots: index,follow
---

# Convert Excel Workbooks to HTML

Aspose.Cells Cloud provides a robust REST endpoint that converts Excel workbooks (XLS, XLSX, CSV, etc.) into HTML documents. The operation returns a **FileInfo** object containing the generated HTML file (name, size, and Base64‑encoded content).

## Prerequisites

| Requirement              | How to satisfy                                                                                                                           |
| ------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------- |
| **Aspose Cloud account** | Sign‑up at [aspose.cloud](https://www.aspose.cloud)                                                                                      |
| **JWT access token**     | Obtain a bearer token via the OAuth 2.0 `POST /connect/token` endpoint. See [Authentication](/cells/authentication/) for details.      |
| **Storage (optional)**   | If you want the API to read/write files from a specific storage, create it first (e.g., Amazon S3, Azure Blob, or Aspose Cloud storage). |
| **cURL / SDK**           | Any HTTP client capable of multipart/form-data (cURL, Postman, or one of the Aspose.Cells SDKs).                                        |

## Authentication

All Aspose.Cells Cloud requests require JWT token-based authentication:

```http
Authorization: Bearer <access-token>
```

Include the token in the `Authorization` header of every request.

## Endpoint

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

### SDK Examples

| Language | Code |
|----------|------|
| **C#** | ```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar apiInstance = new ConversionApi();\nvar file = File.ReadAllBytes("your.xlsx");\nvar result = apiInstance.PostConvertWorkbookToHtml(\n    file, \n    password: null, \n    checkExcelRestriction: true,\n    region: "en-US",\n    fontsLocation: "/fonts"\n);\nConsole.WriteLine(result.Filename);\n``` |
| **Java** | ```java\nConversionApi api = new ConversionApi();\nFile file = new File("your.xlsx");\nFileInfo info = api.postConvertWorkbookToHtml(\n    file, \n    null, \n    true,\n    "en-US",\n    "/fonts"\n);\nSystem.out.println(info.getFilename());\n``` |
| **Python** | ```python\nfrom asposecellscloud import ConversionApi\napi = ConversionApi()\nwith open('your.xlsx', 'rb') as f:\n    file_info = api.post_convert_workbook_to_html(\n        file=f.read(),\n        password=None,\n        check_excel_restriction=True,\n        region="en-US",\n        fonts_location="/fonts"\n    )\nprint(file_info.filename)\n``` |
| **Node.js** | ```javascript\nconst { ConversionApi } = require('asposecellscloud');\nconst api = new ConversionApi();\nconst fs = require('fs');\napi.postConvertWorkbookToHtml({\n  File: fs.createReadStream('your.xlsx'),\n  password: null,\n  checkExcelRestriction: true,\n  region: 'en-US',\n  fontsLocation: '/fonts'\n}).then(info => console.log(info.Filename));\n``` |
| **Go** | ```go\nimport (\n    "asposecellscloud"\n    "os"\n)\nfunc main() {\n    api := asposecellscloud.NewConversionApi()\n    f, _ := os.Open("your.xlsx")\n    info, _ := api.PostConvertWorkbookToHtml(\n        f, \n        nil, \n        true,\n        "en-US",\n        "/fonts"\n    )\n    fmt.Println(info.Filename)\n}\n``` |
| **PHP** | ```php\nuse Aspose\Cells\ConversionApi;\n$api = new ConversionApi();\n$file = fopen('your.xlsx', 'r');\n$info = $api->postConvertWorkbookToHtml(\n    $file,\n    null,\n    true,\n    "en-US",\n    "/fonts"\n);\necho $info->getFilename();\n``` |
| **Ruby** | ```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::ConversionApi.new\nfile = File.open('your.xlsx')\ninfo = api.post_convert_workbook_to_html(\n  file: file,\n  password: nil,\n  check_excel_restriction: true,\n  region: 'en-US',\n  fonts_location: '/fonts'\n)\nputs info.filename\n``` |
| **Perl** | ```perl\nuse Aspose::Cells::ConversionApi;\nmy $api = Aspose::Cells::ConversionApi->new();\nopen my $fh, '<', 'your.xlsx' or die $!;\nmy $info = $api->post_convert_workbook_to_html(\n  file => $fh,\n  password => undef,\n  check_excel_restriction => 1,\n  region => 'en-US',\n  fonts_location => '/fonts'\n);\nprint $info->{Filename};\n``` |

> **Tip**: For full SDK installation instructions, see the [Aspose.Cells Cloud SDKs repository](https://github.com/aspose-cells-cloud).

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

| Code  | Meaning                                                    | Example Payload                                                                                         |
| ----- | ---------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| `400` | Bad Request – missing/invalid parameters                   | `{ "Code": "BadRequest", "Message": "The 'File' part is required." }`                                  |
| `401` | Unauthorized – invalid or missing JWT token                | `{ "Code": "InvalidToken", "Message": "Access token is missing or expired." }`                         |
| `404` | Not Found – source file not found in the specified storage | `{ "Code": "FileNotFound", "Message": "File 'my.xlsx' does not exist in storage 'MyStorage'." }`       |
| `413` | Payload Too Large – uploaded file exceeds the allowed size | `{ "Code": "RequestEntityTooLarge", "Message": "Uploaded file exceeds the 100 MB limit." }`            |
| `429` | Too Many Requests – rate limit exceeded                    | `{ "Code": "TooManyRequests", "Message": "Rate limit of 60 calls per minute exceeded." }`              |
| `500` | Internal Server Error – unexpected server condition        | `{ "Code": "InternalError", "Message": "An unexpected error occurred. Please try again later." }`      |

## Rate Limits

| Limit                                            | Description                                                                                                                           |
| ------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------- |
| **60 requests per minute** per account (default) | Exceeding this limit returns `429 Too Many Requests`. Adjust your client logic or request a higher quota via the Aspose Cloud portal. |

## Use Cases

- **Web Archiving**: Convert Excel reports to HTML for long-term preservation in web-friendly formats.
- **Legacy System Integration**: Embed Excel data into older web applications without client-side dependencies.
- **Automated Reporting**: Generate dynamic HTML dashboards from Excel templates via CI/CD pipelines.

## Related Endpoints

| Endpoint                    | Description                                                                                             |
| --------------------------- | ------------------------------------------------------------------------------------------------------- |
| `POST /cells/{name}/saveAs` | Save an existing Excel file as HTML (or other formats) directly to storage.                             |
| `GET /cells/{name}`         | Retrieve a workbook already stored as HTML (or other formats) with optional query parameters.           |

## Frequently Asked Questions

**Q:** *How do I authenticate when calling the Excel‑to‑HTML conversion API?*  
**A:** Include an `Authorization: Bearer <access-token>` header obtained from the OAuth 2.0 `/connect/token` endpoint.

**Q:** *What does the `FileInfo` response contain?*  
**A:** Three fields – `Filename` (string), `FileSize` (integer, bytes), and `FileContent` (Base64‑encoded HTML content).

**Q:** *Which error codes might I encounter?*  
**A:** `400` (Bad Request), `401` (Unauthorized), `404` (File Not Found), `413` (Payload Too Large), `429` (Too Many Requests), `500` (Internal Server Error). Each returns a JSON payload with `Code` and `Message`.

**Q:** *Can I specify a custom font location?*  
**A:** Yes. Use the `FontsLocation` query parameter to point to a folder or URL that contains the required fonts.

**Q:** *Is there a rate‑limit for this operation?*  
**A:** The default limit is **60 calls per minute** per account. Exceeding it returns `429 Too Many Requests`.

## Change Log

| Version  | Date       | Changes                                                                            |
| -------- | ---------- | ---------------------------------------------------------------------------------- |
| **v3.0** | 2024-10-01 | Initial public release of `PostConvertWorkbookToHtml`.                             |
| **v3.1** | 2025-04-15 | Added `region` and `FontsLocation` query parameters; updated error payload format. |
| **v3.2** | 2026-03-20 | Introduced rate‑limit documentation and sample error responses.                    |

---

_For any further assistance, please contact Aspose support or visit the official API reference:_ [https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToHtml](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToHtml)

## JSON‑LD Breadcrumb (Structured Data)

```html
<script type="application/ld+json">
  {
    "@context": "https://schema.org",
    "@type": "BreadcrumbList",
    "itemListElement": [
      {
        "@type": "ListItem",
        "position": 1,
        "name": "Home",
        "item": "https://docs.aspose.cloud/"
      },
      {
        "@type": "ListItem",
        "position": 2,
        "name": "Developer Center",
        "item": "https://docs.aspose.cloud/cells/"
      },
      {
        "@type": "ListItem",
        "position": 3,
        "name": "Conversion",
        "item": "https://docs.aspose.cloud/cells/conversion/"
      },
      {
        "@type": "ListItem",
        "position": 4,
        "name": "Excel to HTML",
        "item": "https://docs.aspose.cloud/cells/convert-excel-file-to-html-file/"
      }
    ]
  }
</script>
```