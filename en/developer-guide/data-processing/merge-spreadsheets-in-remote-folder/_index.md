---
url: /merge-spreadsheets-in-remote-folder/
title: "Merge Matching Spreadsheets in Remote Folder"
date: 2024-03-15
lastmod: 2024-05-22
version: "v4.0"
description: "Combine multiple spreadsheet files stored in Aspose Cloud storage into a single file. Supports 30+ output formats including PDF, CSV, JSON, XLSX, ODS, and XPS—fully in the cloud."
keywords: ["Aspose.Cells", "merge spreadsheets", "remote folder", "cloud API", "PDF merge", "XLSX merge", "CSV merge", "ODS merge"]
weight: 10
type: docs
---

> **Deprecation Notice**  
> This API is stable as of Aspose.Cells Cloud v4.0. For older versions, see [API Versioning Guide]({{< relref "/docs/api-versioning" >}}).

---

## Overview

Merge multiple spreadsheet files stored in a remote Aspose Cloud storage folder into a single output file, fully in the cloud—no local file downloads required. The operation supports over 30 output formats, including **PDF**, **CSV**, **JSON**, **XLSX**, **ODS**, and **XPS**.

Key benefits:
- **Cloud-native processing**: Eliminates bandwidth overhead and local resource constraints.
- **Flexible formatting**: Choose between consolidating all data into one worksheet or preserving per-file sheets.
- **Locale-aware output**: Apply region-specific number, date, and currency formatting.

---

## API Endpoint

```http
PUT https://api.aspose.cloud/v4.0/cells/merge/remote-spreadsheets
```

### Security & Authentication

All requests require JWT token-based authentication. See [Authenticating API Requests]({{< relref "/docs/getting-started/authenticating-api-requests" >}}) for setup instructions.

---

## Request Parameters

| Parameter             | Type      | Location | Required | Description |
|-----------------------|-----------|----------|----------|-------------|
| `folder`              | `string`  | Query    | ✅ Yes    | Cloud storage folder containing source spreadsheets. |
| `fileMatchExpression` | `string`  | Query    | ❌ No     | Pattern to match files (e.g., `*report*.xlsx`). Supports `*` (any characters) and `?` (single character). Defaults to all files in `folder`. |
| `outFormat`           | `string`  | Query    | ❌ No     | Output format: `PDF`, `CSV`, `JSON`, `XLSX`, `ODS`, `XPS`, etc. Default: `XLSX`. |
| `mergeInOneSheet`     | `boolean` | Query    | ❌ No     | `true`: All data merged into one worksheet. `false`: Each source file → its own worksheet. Default: `false`. |
| `storageName`         | `string`  | Query    | ❌ No     | Custom storage name. Omit to use primary storage. |
| `outPath`             | `string`  | Query    | ❌ No     | Destination folder for the merged file. Omit to save in `folder`. |
| `outStorageName`      | `string`  | Query    | ❌ No     | Storage where the output file is saved. Omit to use `storageName`. |
| `fontsLocation`       | `string`  | Query    | ❌ No     | Path to custom fonts folder (required for PDF/image exports). |
| `region`              | `string`  | Query    | ❌ No     | Locale for formatting (e.g., `en-US`, `de-DE`, `fr-FR`). |
| `password`            | `string`  | Query    | ❌ No     | Password to decrypt protected source spreadsheets. |

---

## Example Request (cURL)

```bash
curl -X PUT \
  "https://api.aspose.cloud/v4.0/cells/merge/remote-spreadsheets?folder=Reports&fileMatchExpression=*_Q1.xlsx&outFormat=PDF&mergeInOneSheet=true" \
  -H "Authorization: Bearer <access_token>" \
  -H "Accept: application/json"
```

> 💡 **Tip**: For programmatic integration, use one of our [SDKs](https://github.com/aspose-cells-cloud). See [Using Aspose.Cells Cloud SDKs](#using-asposecells-cloud-sdks) below.

---

## Response

### Success Response

| Status Code | Content-Type               | Description |
|-------------|----------------------------|-------------|
| `200 OK`    | `application/octet-stream` | Binary stream of the merged workbook (e.g., PDF or XLSX). |
| `202 Accepted` | `application/json`      | JSON object with `FileUrl`, `FileName`, and `FileSize`. |

#### Sample 202 JSON Response
```json
{
  "FileName": "MergedReport_2024-05-22.pdf",
  "FileSize": 245678,
  "FileUrl": "https://api.aspose.cloud/v4.0/cells/MergedReport_2024-05-22.pdf?token=..."
}
```

Download the merged file directly from `FileUrl`, or save it to the specified `outPath`.

---

## HTTP Status Codes

| Code | Meaning             | Description |
|------|---------------------|-------------|
| `200` | OK                 | Merged file returned as binary stream. |
| `202` | Accepted           | Merged file saved to cloud storage; details in response body. |
| `400` | Bad Request        | Invalid parameter (e.g., unsupported `outFormat`, malformed `fileMatchExpression`). |
| `401` | Unauthorized       | Missing or invalid JWT token. |
| `404` | Not Found          | Source folder or files not found in storage. |
| `413` | Payload Too Large  | Total input size exceeds cloud limits. |
| `500` | Internal Server Error | Unexpected server-side failure during merge. |

---

## Error Handling

- **400 Bad Request**: Invalid URL or malformed query parameters (e.g., `folder` missing, `outFormat` unsupported).  
- **401 Unauthorized**: Authentication failed or credentials expired.  
- **404 Not Found**: Source files inaccessible or storage path invalid.  
- **500 Server Error**: Internal failure (e.g., corrupted source file, service unavailability).

---

## Using Aspose.Cells Cloud SDKs

SDKs abstract low-level HTTP details and simplify integration. Supported languages include:
- [Go](https://github.com/aspose-cells-cloud/aspose-cells-cloud-go)
- [Java](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java)
- [Node.js](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node)
- [Python](https://github.com/aspose-cells-cloud/aspose-cells-cloud-python)
- [.NET](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet)

### Sample (Go SDK)
```go
import (
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v40/cells"
)

cfg := cells.NewConfiguration(clientId, clientSecret)
api := cells.NewCellsApiWithClientConfiguration(cfg)

mergeOpts := &cells.CellsMergeRequest{
    Folder:           "Reports",
    FileMatchExpression: "*.xlsx",
    OutFormat:        "PDF",
    MergeInOneSheet:  true,
}

resp, _, err := api.CellsMergeRemoteSpreadsheets(
    context.Background(),
    "MyFolder",
    mergeOpts,
    nil, // storageName
    nil, // outPath
    nil, // outStorageName
    nil, // fontsLocation
    nil, // region
    nil, // password
)
```

See the [OpenAPI Specification]({{< relref "/docs/api-reference/openapi-spec#mergeSpreadsheetsInRemoteFolder" >}}) for full schema details.

---

## Related Documentation

- [Upload Files to Cloud Storage]({{< relref "/upload-files-to-cloud-storage" >}})
- [Split Spreadsheets]({{< relref "/split-spreadsheets" >}})
- [Export to PDF with Custom Fonts]({{< relref "/export-to-pdf#custom-fonts" >}})
- [API Versioning Guide]({{< relref "/docs/api-versioning" >}})

---

## Best Practices

1. **Use `region` for locale-sensitive reports** (e.g., `en-US` for USD currency, `de-DE` for German date formats).  
2. **Set `outPath` explicitly** to avoid overwriting source files.  
3. **Include `fontsLocation`** when exporting to PDF/image to preserve formatting.  
4. **Leverage `fileMatchExpression`** to dynamically filter by naming conventions (e.g., `*2024*.ods`).  

---

## Changelog

| Version | Date       | Changes |
|---------|------------|---------|
| v4.0    | 2024-03-15 | Initial release of `MergeSpreadsheetsInRemoteFolder`. |
| —       | 2024-05-22 | Updated examples, added deprecation notice, fixed parameter defaults. |

---