---
url: /merge-spreadsheets-in-remote-folder/
title: "Merge Matching Spreadsheets in Remote Folder"
linktitle: "Merge files in remote folder"
description: "Merge spreadsheets in Aspose Cloud remote folder to PDF, XLSX, CSV, ODS, JSON, XPS—no local download."
keywords:
  [
    "Aspose.Cells",
    "merge spreadsheets",
    "remote folder",
    "cloud API",
    "PDF merge",
    "XLSX merge",
    "CSV merge",
    "ODS merge",
  ]
weight: 100
type: docs
ArticleTitle: "Merge Spreadsheets in Remote Aspose.Cells Cloud Folder"
---

## Overview

Merge multiple spreadsheet files stored in a remote Aspose Cloud storage folder into a single output file, fully in the cloud—no local file downloads required. The operation supports over 30 output formats, including **PDF**, **CSV**, **JSON**, **XLSX**, **ODS**, and **XPS**.

Key benefits:

- **Cloud-native processing**: Eliminates bandwidth overhead and local resource constraints.
- **Flexible formatting**: Choose between consolidating all data into one worksheet or preserving per-file sheets.
- **Locale-aware output**: Apply region-specific number, date, and currency formatting.

## API Endpoint

```http
PUT https://api.aspose.cloud/v4.0/cells/merge/remote-spreadsheets
```

### Security & Authentication

All requests require JWT token-based authentication. See [Authenticating API Requests](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) for setup instructions.

## Request Parameters

| Parameter             | Type      | Location | Required | Description                                                                                                                                  |
| --------------------- | --------- | -------- | -------- | -------------------------------------------------------------------------------------------------------------------------------------------- |
| `folder`              | `string`  | Query    | ✅ Yes   | Cloud storage folder containing source spreadsheets.                                                                                         |
| `fileMatchExpression` | `string`  | Query    | ❌ No    | Pattern to match files (e.g., `*report*.xlsx`). Supports `*` (any characters) and `?` (single character). Defaults to all files in `folder`. |
| `outFormat`           | `string`  | Query    | ❌ No    | Output format: `PDF`, `CSV`, `JSON`, `XLSX`, `ODS`, `XPS`, etc. Default: `XLSX`.                                                             |
| `mergeInOneSheet`     | `boolean` | Query    | ❌ No    | `true`: All data merged into one worksheet. `false`: Each source file → its own worksheet. Default: `false`.                                 |
| `storageName`         | `string`  | Query    | ❌ No    | Custom storage name. Omit to use primary storage.                                                                                            |
| `outPath`             | `string`  | Query    | ❌ No    | Destination folder for the merged file. Omit to save in `folder`.                                                                            |
| `outStorageName`      | `string`  | Query    | ❌ No    | Storage where the output file is saved. Omit to use `storageName`.                                                                           |
| `fontsLocation`       | `string`  | Query    | ❌ No    | Path to custom fonts folder (required for PDF/image exports).                                                                                |
| `region`              | `string`  | Query    | ❌ No    | Locale for formatting (e.g., `en-US`, `de-DE`, `fr-FR`).                                                                                     |
| `password`            | `string`  | Query    | ❌ No    | Password to decrypt protected source spreadsheets.                                                                                           |

## Example Request (cURL)

```bash
curl -X PUT \
  "https://api.aspose.cloud/v4.0/cells/merge/remote-spreadsheets?folder=Reports&fileMatchExpression=*_Q1.xlsx&outFormat=PDF&mergeInOneSheet=true" \
  -H "Authorization: Bearer <access_token>" \
  -H "Accept: application/json"
```

> 💡 **Tip**: For programmatic integration, use one of our [SDKs](https://github.com/aspose-cells-cloud). See [Using Aspose.Cells Cloud SDKs](#using-asposecells-cloud-sdks) below.

## Response

### Success Response

| Status Code    | Content-Type               | Description                                               |
| -------------- | -------------------------- | --------------------------------------------------------- |
| `200 OK`       | `application/octet-stream` | Binary stream of the merged workbook (e.g., PDF or XLSX). |
| `202 Accepted` | `application/json`         | JSON object with `FileUrl`, `FileName`, and `FileSize`.   |

#### Sample 202 JSON Response

```json
{
  "FileName": "MergedReport_2024-05-22.pdf",
  "FileSize": 245678,
  "FileUrl": "https://api.aspose.cloud/v4.0/cells/MergedReport_2024-05-22.pdf?token=..."
}
```

Download the merged file directly from `FileUrl`, or save it to the specified `outPath`.

## HTTP Status Codes

| Code  | Meaning               | Description                                                                         |
| ----- | --------------------- | ----------------------------------------------------------------------------------- |
| `200` | OK                    | Merged file returned as binary stream.                                              |
| `202` | Accepted              | Merged file saved to cloud storage; details in response body.                       |
| `400` | Bad Request           | Invalid parameter (e.g., unsupported `outFormat`, malformed `fileMatchExpression`). |
| `401` | Unauthorized          | Missing or invalid JWT token.                                                       |
| `404` | Not Found             | Source folder or files not found in storage.                                        |
| `413` | Payload Too Large     | Total input size exceeds cloud limits.                                              |
| `500` | Internal Server Error | Unexpected server-side failure during merge.                                        |
