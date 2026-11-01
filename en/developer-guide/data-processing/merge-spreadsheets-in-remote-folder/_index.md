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
The **MergeSpreadsheetsInRemoteFolder** API (`PUT https://api.aspose.cloud/v4.0/cells/merge/remote-spreadsheets`) enables Aspose.Cells Cloud users to merge multiple spreadsheet files stored in a remote cloud storage folder into a single output file—fully in the cloud—without downloading files locally, supporting over 30 output formats including XLSX, CSV, PDF, ODS, JSON, and XPS.

## Overview

Merge multiple spreadsheet files stored in a remote Aspose Cloud storage folder into a single output file, fully in the cloud—no local file downloads required. The operation supports over 30 output formats, including **PDF**, **CSV**, **JSON**, **XLSX**, **ODS**, and **XPS**.

Key benefits:

- **Cloud-native processing**: Eliminates bandwidth overhead and local resource constraints.
- **Flexible formatting**: Choose between consolidating all data into one worksheet or preserving per-file sheets.
- **Locale-aware output**: Apply region-specific number, date, and currency formatting.

## The Merge Spreadsheets in Remote Folder Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/merge/remote-spreadsheets
```

### Security & Authentication

All requests require JWT token-based authentication. See [Authenticating API Requests](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) for setup instructions.

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| folder | String | Query | The folder used to store the merged files. |
| fileMatchExpression | String | Query | - |
| outFormat | String | Query | The out file format. |
| mergeInOneSheet | Boolean | Query | Whether to combine all data into a single worksheet. |
| storageName | String | Query | (Optional) The name of the storage if using custom cloud storage. Use default storage if omitted. |
| outPath | String | Query | (Optional) The folder path where the workbook is stored. The default is null. |
| outStorageName | String | Query | Output file Storage Name. |
| fontsLocation | String | Query | Use Custom fonts. |
| region | String | Query | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior. |
| password | String | Query | The password for opening spreadsheet file. |

### **Response**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**Sample response headers**

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="result"
```

**HTTP Status Codes**

| Code | Meaning | Description |
|---|---|---|
| 200 | OK | The request completed successfully. |
| 400 | Bad Request | Invalid url. |
| 401 | Unauthorized | Authentication has failed, or no credentials were provided. |
| 404 | Not Found | Source file not accessible. |
| 500 | Server Error | The spreadsheet has encountered an anomaly in obtaining data. |

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
