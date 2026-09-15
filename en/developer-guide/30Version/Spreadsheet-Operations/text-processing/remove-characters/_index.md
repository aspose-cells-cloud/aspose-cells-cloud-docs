---
url: /excel-remove-characters/
title: Remove Characters from Excel – Aspose.Cells Cloud API (POST /cells/removecharacters)
description: Clean Excel data by removing custom characters, character sets, or substrings via Aspose.Cells Cloud API. Supports bulk removal, substrings, and case-insensitive processing.
date: 2024-06-15
lastmod: 2024-06-15
tags:
  - excel
  - text-processing
  - api
keywords: "remove characters, Aspose.Cells, Excel API, text processing, cloud"
aliases:
  - /text-processing/remove-characters/
weight: 100
---

## Overview

The **Remove Characters** API enables you to clean and standardize text content in Excel worksheets by removing specific characters, predefined character sets, or substrings. This operation helps eliminate unwanted symbols, formatting artifacts, or inconsistent text patterns — ideal for data preprocessing, validation, and automation workflows.

> **Note**: This operation modifies cell values *in-place* and returns the updated workbook as a base64-encoded string in the response.

## Prerequisites

- An active [Aspose Cloud account](https://dashboard.aspose.cloud/).
- A valid JWT access token (see [Authentication Guide](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/){rel="noopener noreferrer"}).
- Your Excel file uploaded to Aspose Cloud storage (`.xlsx`, `.xls`, `.xlsm`, or other supported formats).
- An API client or SDK (e.g., cURL, Python, .NET, Java, Node.js). See [SDKs on GitHub](https://github.com/aspose-cells-cloud){rel="noopener noreferrer"}.

## API Endpoint

```http
POST https://api.aspose.cloud/v3.0/cells/removecharacters
```

### Request Headers

| Header | Value |
|--------|-------|
| `Authorization` | Bearer `{access_token}` |
| `Content-Type` | `application/json` |

---

## Request Parameters

| Parameter | Type | Location | Required | Description |
|-----------|------|----------|----------|-------------|
| `removeCharactersOptions` | `RemoveCharactersOptions` | Body | Yes | Object defining the scope and type of characters to remove. |

### `RemoveCharactersOptions` Schema

| Property | Type | Required | Description |
|----------|------|----------|-------------|
| `Range` | string | Yes | A1-style range (e.g., `"A1:C10"`) or named range to process. |
| `CustomCharacters` | string | No | String of characters to remove (e.g., `"@#$"`). Each character is treated individually. |
| `CharacterSet` | string | No | Predefined set: `"NonPrinting"`, `"Text"`, `"Numeric"`, `"Symbols"`, or `"Punctuation"`. |
| `Substring` | string | No | Exact substring to remove (e.g., `"USD"`, `"°C"`). |
| `IgnoreCase` | boolean | No | If `true`, substring and text-character removal is case-insensitive. Default: `false`. |

> **Tip**: Only one of `CustomCharacters`, `CharacterSet`, or `Substring` should be specified per request to avoid ambiguous behavior.

### Example Request Body

```json
{
  "Range": "A1:B20",
  "CustomCharacters": "@#$%",
  "CharacterSet": "NonPrinting",
  "Substring": "USD",
  "IgnoreCase": true
}
```

### Example cURL Request

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/removecharacters" \
  -H "Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9..." \
  -H "Content-Type: application/json" \
  -d '{
    "Range": "A1:B20",
    "CustomCharacters": "@#$",
    "Substring": "USD",
    "IgnoreCase": true
  }'
```

---

## Response

On success, the API returns a `FileInfo` object containing metadata and the updated file content.

### Success Response (200 OK)

```json
{
  "Code": 200,
  "Status": "OK",
  "Filename": "cleaned_report.xlsx",
  "Filesize": 45892,
  "FileContent": "UEsDBBQABgAIAAAAIQDf...[base64-encoded .xlsx content]"
}
```

| Field | Description |
|-------|-------------|
| `Code` | HTTP status code (200 for success). |
| `Status` | Operation result (`"OK"`). |
| `Filename` | Name of the modified file. |
| `Filesize` | Size of the updated file in bytes. |
| `FileContent` | Base64-encoded binary content of the updated Excel file. |

### Error Responses

| Status Code | Error | Description |
|-------------|-------|-------------|
| `400` | `Bad Request` | Invalid `Range`, missing/invalid parameters, or unsupported file type. |
| `401` | `Unauthorized` | Invalid, expired, or missing JWT token. |
| `413` | `Payload Too Large` | Input file exceeds the 2 GB limit. |
| `500` | `Internal Server Error` | Unexpected server-side failure. |

---

## Supported Character Sets

| Set | Characters Removed | Use Case |
|-----|-------------------|----------|
| `NonPrinting` | ASCII 0–31, 127, 129, 141, 143, 144, 157 | Remove hidden line breaks, control chars, and formatting artifacts. |
| `Text` | All letters (A–Z, a–z) | Strip alphabetic characters (e.g., to extract pure numbers). |
| `Numeric` | All digits (0–9) | Remove numbers, leaving text or symbols. |
| `Symbols` | Math (`+`, `×`, `π`), currency (`€`, `¥`), punctuation-like (™, №) | Standardize technical or financial data. |
| `Punctuation` | `.,;:!?'"()[]{}-` | Clean natural-language text for NLP or indexing. |

---

## SDK Code Examples

### Python (aspose-cells-cloud)

```python
import os
import asposecellscloud
from asposecellscloud.apis.text_processing_api import TextProcessingApi
from asposecellscloud.models.remove_characters_options import RemoveCharactersOptions

# Initialize API
client_id = "your_client_id"
client_secret = "your_client_secret"
api = TextProcessingApi(client_id, client_secret)

# Prepare request
options = RemoveCharactersOptions(
    range="A1:B20",
    custom_characters="@#$",
    substring="USD",
    ignore_case=True
)

# Call API
response = api.post_remove_characters(
    remove_characters_options=options,
    file="input.xlsx"
)

# Save result
with open("output.xlsx", "wb") as f:
    f.write(response.file_content.encode('utf-8'))
```

### .NET (C#)

```csharp
using Aspose.Cells.Cloud.Sdk;
using Aspose.Cells.Cloud.Sdk.Model;

var configuration = new Configuration
{
    ClientId = "your_client_id",
    ClientSecret = "your_client_secret"
};
var api = new TextProcessingApi(configuration);

var options = new RemoveCharactersOptions
{
    Range = "A1:B20",
    CustomCharacters = "@#$",
    Substring = "USD",
    IgnoreCase = true
};

var response = api.PostRemoveCharacters(options, "input.xlsx");
File.WriteAllBytes("output.xlsx", Convert.FromBase64String(response.FileContent));
```

> For more SDKs (Java, PHP, Node.js, Ruby, etc.), visit the [Aspose.Cells Cloud GitHub repository](https://github.com/aspose-cells-cloud){rel="noopener noreferrer"}.

---

## Best Practices

1. **Test on a copy**: Always verify the impact on a non-production file first.
2. **Combine with other tools**: Use in conjunction with `PostCleanObjects` or `PostRemoveBlankRows` for full data cleanup.
3. **Use `IgnoreCase` carefully**: Set `IgnoreCase = true` only when case-insensitive removal is intended (e.g., for user-facing substrings like `"USD"` or `"°C"`).
4. **Avoid overlapping operations**: Do not specify both `CustomCharacters` and `Substring` in the same request.

---

## Related Resources

- [Aspose.Cells Cloud Documentation](https://docs.aspose.cloud/cells/)
- [Full OpenAPI Specification](https://reference.aspose.cloud/cells/#/TextProcessingController/PostRemoveCharacters)
- [SDK Examples on GitHub](https://github.com/aspose-cells-cloud)
- [API Pricing & Free Trial](https://purchase.aspose.cloud/pricing)

---

> **Tip**: Need to remove characters *based on position* (e.g., first 3 chars)? Use the [`PostCellsTrimText`](/excel-trim-text/) API instead.