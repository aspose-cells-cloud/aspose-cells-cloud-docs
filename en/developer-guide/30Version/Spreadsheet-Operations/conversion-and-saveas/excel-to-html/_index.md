---
title: Convert Excel to HTML  
description: Convert an Excel workbook to an HTML file using Aspose.Cells Cloud API v3.0.  
api_version: v3.0  
base_url: https://api.aspose.cloud/v3.0  
---

# Convert Excel to HTML  

Aspose.Cells Cloud provides a robust REST endpoint that converts an Excel workbook (XLS, XLSX, CSV, etc.) into an HTML document. The operation returns a **FileInfo** object that contains the generated HTML file (name, size, and Base64‑encoded content).

---

## Prerequisites

| Requirement | How to satisfy |
|-------------|----------------|
| **Aspose Cloud account** | Sign‑up at [aspose.cloud](https://www.aspose.cloud). |
| **JWT access token** | Obtain a bearer token via the OAuth 2.0 `POST /connect/token` endpoint. |
| **Storage (optional)** | If you want the API to read/write files from a specific storage, create it first (e.g., Amazon S3, Azure Blob, or Aspose Cloud storage). |
| **cURL / SDK** | Any HTTP client capable of multipart/form‑data (cURL, Postman, or one of the Aspose.Cells SDKs). |

---

## Authentication

All Aspose.Cells Cloud requests require **JWT token‑based authentication**.

```http
Authorization: Bearer <access-token>
```

The token must be included in the `Authorization` header of every request.

---

## Endpoint

```
POST https://api.aspose.cloud/v3.0/cells/convert/html
```

> **Note** – The request must be sent as `multipart/form-data`. The Excel file is the first part of the multipart body.

---

## Request Parameters  

### Query Parameters  

| Name                     | Type    | Required | Default | Description |
|--------------------------|---------|----------|---------|-------------|
| `password`               | string  | No       | –       | Password to open a protected workbook. |
| `storageName`            | string  | No       | –       | Name of the storage where the source file resides. |
| `checkExcelRestriction` | boolean | No       | `true`  | When `true`, the service validates Excel‑specific restrictions (e.g., protected sheets). |
| `region`                 | string  | No       | –       | Regional settings for the workbook (e.g., `en-US`). |
| `FontsLocation`          | string  | No       | –       | URL or path to a folder that contains custom fonts required for rendering. |

### Form‑Data (Multipart)  

| Name | Type | Required | Description |
|------|------|----------|-------------|
| **File** | file | **Yes** | The Excel workbook to be converted. Must be supplied as the first part of the multipart request. |

---

## Request Example (cURL)

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/html?checkExcelRestriction=true" \
     -H "accept: multipart/form-data" \
     -H "Authorization: Bearer <access-token>" \
     -H "Content-Type: multipart/form-data" \
     -F "File=@/path/to/your_workbook.xlsx"
```

---

## Successful Response  

**Status Code:** `200 OK`

| Field        | Type   | Description |
|--------------|--------|-------------|
| `Filename`   | string | Name of the generated HTML file (e.g., `example.html`). |
| `FileSize`   | int    | Size of the HTML file in bytes. |
| `FileContent`| string | Base64‑encoded HTML content. |

```json
{
  "Filename": "example.html",
  "FileSize": 12345,
  "FileContent": "base64_encoded_string"
}
```

The response schema is defined by the **FileInfo** model: [/cells/file-info](/cells/file-info/).

---

## Error Responses  

| Code | Meaning                | Example Payload |
|------|------------------------|-----------------|
| `400` | Bad Request – missing/invalid parameters | ```json { "Code": "BadRequest", "Message": "The 'File' part is required." } ``` |
| `401` | Unauthorized – invalid or missing JWT token | ```json { "Code": "InvalidToken", "Message": "Access token is missing or expired." } ``` |
| `404` | Not Found – source file not found in the specified storage | ```json { "Code": "FileNotFound", "Message": "File 'my.xlsx' does not exist in storage 'MyStorage'." } ``` |
| `413` | Payload Too Large – uploaded file exceeds the allowed size | ```json { "Code": "RequestEntityTooLarge", "Message": "Uploaded file exceeds the 100 MB limit." } ``` |
| `429` | Too Many Requests – rate limit exceeded | ```json { "Code": "TooManyRequests", "Message": "Rate limit of 60 calls per minute exceeded." } ``` |
| `500` | Internal Server Error – unexpected server condition | ```json { "Code": "InternalError", "Message": "An unexpected error occurred. Please try again later." } ``` |

---

## Rate Limits  

| Limit | Description |
|-------|-------------|
| **60 requests per minute** per account (default) | Exceeding this limit returns `429 Too Many Requests`. Adjust your client logic or request a higher quota via the Aspose Cloud portal. |

---

## SDK Support  

Aspose provides first‑class SDKs that wrap this endpoint for several languages. The examples below demonstrate the same conversion using the official SDKs.

| Language | Sample |
|----------|--------|
| C#       | <details><summary>View example</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar apiInstance = new ConversionApi();\nvar file = File.ReadAllBytes(\"your.xlsx\");\nvar result = apiInstance.PostConvertWorkbookToHtml(file, password: null, checkExcelRestriction: true);\nConsole.WriteLine(result.Filename);\n```</details> |
| Java     | <details><summary>View example</summary>```java\nConversionApi api = new ConversionApi();\nFile file = new File(\"your.xlsx\");\nFileInfo info = api.postConvertWorkbookToHtml(file, null, true);\nSystem.out.println(info.getFilename());\n```</details> |
| Python   | <details><summary>View example</summary>```python\nfrom asposecellscloud import ConversionApi\napi = ConversionApi()\nwith open('your.xlsx', 'rb') as f:\n    file_info = api.post_convert_workbook_to_html(file=f.read())\nprint(file_info.filename)\n```</details> |
| Node.js  | <details><summary>View example</summary>```javascript\nconst { ConversionApi } = require('asposecellscloud');\nconst api = new ConversionApi();\nconst fs = require('fs');\napi.postConvertWorkbookToHtml({ File: fs.createReadStream('your.xlsx') })\n   .then(info => console.log(info.Filename));\n```</details> |
| Go       | <details><summary>View example</summary>```go\nimport (\n    \"asposecellscloud\"\n    \"os\"\n)\nfunc main() {\n    api := asposecellscloud.NewConversionApi()\n    f, _ := os.Open(\"your.xlsx\")\n    info, _ := api.PostConvertWorkbookToHtml(f, nil, true)\n    fmt.Println(info.Filename)\n}\n```</details> |
| PHP      | <details><summary>View example</summary>```php\nuse Aspose\Cells\ConversionApi;\n$api = new ConversionApi();\n$file = fopen('your.xlsx', 'r');\n$info = $api->postConvertWorkbookToHtml($file);\necho $info->getFilename();\n```</details> |
| Ruby     | <details><summary>View example</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::ConversionApi.new\nfile = File.open('your.xlsx')\ninfo = api.post_convert_workbook_to_html(file: file)\nputs info.filename\n```</details> |
| Perl     | <details><summary>View example</summary>```perl\nuse Aspose::Cells::ConversionApi;\nmy $api = Aspose::Cells::ConversionApi->new();\nopen my $fh, '<', 'your.xlsx' or die $!;\nmy $info = $api->post_convert_workbook_to_html(file => $fh);\nprint $info->{Filename};\n```</details> |

For the full list of supported SDKs and installation instructions, see the **Aspose.Cells Cloud SDKs** repository: <https://github.com/aspose-cells-cloud>.

---

## Related Endpoints  

| Endpoint | Description |
|----------|-------------|
| `POST /cells/{name}/saveAs` | Save an existing Excel file as HTML (or other formats) directly to storage. |
| `PUT /cells/convert` | Convert a workbook to HTML with additional conversion options; result is returned in the response body. |
| `GET /cells/{name}` | Retrieve a workbook already stored as HTML (or other formats) with optional query parameters. |

---

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

---

## JSON‑LD Breadcrumb (Structured Data)

Adding this block improves SEO by enabling rich‑snippet breadcrumbs in search results.

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "BreadcrumbList",
  "itemListElement": [
    { "@type": "ListItem", "position": 1, "name": "Home", "item": "https://docs.aspose.cloud/" },
    { "@type": "ListItem", "position": 2, "name": "Developer Center", "item": "https://docs.aspose.cloud/cells/" },
    { "@type": "ListItem", "position": 3, "name": "Conversion", "item": "https://docs.aspose.cloud/cells/conversion/" },
    { "@type": "ListItem", "position": 4, "name": "Excel to HTML", "item": "https://docs.aspose.cloud/cells/convert-excel-file-to-html-file/" }
  ]
}
</script>
```

---

## Change Log  

| Version | Date | Changes |
|---------|------|---------|
| **v3.0** | 2024‑10‑01 | Initial public release of `PostConvertWorkbookToHtml`. |
| **v3.1** | 2025‑04‑15 | Added `region` and `FontsLocation` query parameters; updated error payload format. |
| **v3.2** | 2026‑03‑20 | Introduced rate‑limit documentation and sample error responses. |

--- 

*For any further assistance, please contact Aspose support or visit the official API reference:* <https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToHtml>  