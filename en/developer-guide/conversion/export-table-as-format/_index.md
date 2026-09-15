---
title: "Export Excel Table to PDF, PNG, CSV via Aspose.Cells Cloud"
lastmod: 2024-03-15
date: 2020-01-01
linktitle: "Export Table to PDF/PNG/CSV"
type: docs
url: /export-table-as-format/
keywords: "Aspose.Cells Cloud, export table, Excel table to PDF, REST API, cloud conversion, JWT auth"
description: "Securely export cloud-stored Excel tables to PDF, PNG, CSV, or JSON using Aspose.Cells Cloud REST API v4.0. Includes JWT authentication, cURL examples, and SDKs for C#, Java, Python, Node.js, PHP, Ruby, Perl, and Go."
weight: 100
---

Export a cloud-stored Excel table (structured list) to another format — such as PDF, PNG, CSV, or JSON — directly in the cloud without downloading the workbook.

{{% alert color="primary" %}}
**Last updated**: March 15, 2024  
All examples use test files. Replace `{access_token}` with your JWT token from the [Aspose Cloud Dashboard](https://dashboard.aspose.cloud/).
{{% /alert %}}

## API Endpoint

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/tables/{tableName}
```

### Security & Authentication

All requests require [JWT token-based authentication](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

```bash
-H "Authorization: Bearer {access_token}"
```

### Request Parameters

| Parameter Name   | Type    | Location | Required | Description |
|------------------|---------|----------|----------|-------------|
| `name`           | string  | Path     | ✅ Yes    | Name of the workbook file in cloud storage. |
| `worksheet`      | string  | Path     | ✅ Yes    | Name of the worksheet containing the table. |
| `tableName`      | string  | Path     | ✅ Yes    | Name of the table to export. |
| `format`         | string  | Query    | ✅ Yes    | Output format: `pdf`, `png`, `svg`, `csv`, `json`, etc. Case-insensitive (e.g., `"Pdf"` or `"PDF"` accepted). |
| `folder`         | string  | Query    | ❌ No     | Folder path of the workbook. Defaults to root. |
| `storageName`    | string  | Query    | ❌ No     | Custom cloud storage name. Uses default storage if omitted. |
| `outPath`        | string  | Query    | ❌ No     | Output file path in cloud storage. Defaults to root. |
| `outStorageName` | string  | Query    | ❌ No     | Storage for output file. Defaults to `storageName` or default storage. |
| `fontsLocation`  | string  | Query    | ❌ No     | Custom font directory for accurate rendering. |
| `region`         | string  | Query    | ❌ No     | Locale (e.g., `en-US`, `fr-FR`) affecting number/date formatting. |
| `password`       | string  | Query    | ❌ No     | Password to decrypt the protected workbook. |
| `autoRowsFit`    | boolean | Query    | ❌ No     | Auto-fit rows before export. |
| `autoColumnsFit` | boolean | Query    | ❌ No     | Auto-fit columns before export. |

### Response

Returns the exported table as binary file content.

| Field | Type | Description |
|-------|------|-------------|
| `fileContents` | `byte[]` | Base64-encoded file data (cURL returns raw binary; SDKs decode automatically). |
| `contentType`  | `string` | MIME type (e.g., `application/pdf`, `image/png`, `text/csv`). |
| `fileDownloadName` | `string` | Optional suggested filename. |

### HTTP Status Codes

| Code | Meaning | Description |
|------|---------|-------------|
| `200` | OK | Table successfully exported. Response contains binary file content. |
| `400` | Bad Request | Missing/invalid parameters (e.g., unsupported `format`, malformed URL). |
| `401` | Unauthorized | Invalid or missing JWT token. |
| `404` | Not Found | Workbook, worksheet, or table not found. |
| `500` | Internal Server Error | Unexpected server error during conversion. |

## Use Cases

- **Legacy System Migration**: Convert legacy `.xls` tables to `.xlsx` or CSV for modern systems.  
- **Data Interchange**: Normalize tables to CSV/JSON for ingestion into databases or analytics tools.  
- **Web Publishing**: Export formatted tables to HTML or PNG for dashboards and reports.  
- **Archive Standardization**: Convert heterogeneous formats (XLS, XLSM, ODS) to a unified PDF for compliance.  
- **Office Interoperability**: Generate files compatible with LibreOffice, Google Sheets, or Apple Numbers.

## Why Use This API?

- ✅ **Cloud-native**: No local resource usage; conversions happen server-side.  
- ✅ **Secure**: HTTPS + JWT authentication; no file downloads.  
- ✅ **Developer-friendly**: SDKs for 8+ languages; REST interface for flexibility.  
- ✅ **Cost-efficient**: Pay-per-use with no infrastructure overhead.  
- ✅ **Accurate rendering**: Supports custom fonts, locale settings, and auto-fitting.

> **Note**: By default, the API exports **raw table data only** (cell values, no styles). To preserve formatting (e.g., colors, fonts), use `format=pdf` with `autoRowsFit=true` and `autoColumnsFit=true`.

## Example: cURL Request

```bash
curl -X GET \
  "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/tables/Table1?format=pdf" \
  -H "Authorization: Bearer {access_token}" \
  -H "Accept: application/octet-stream" \
  --output table_export.pdf
```

✅ **Tip**: Replace `{access_token}` with your token from the Aspose Cloud Dashboard.

## SDK Examples

See full, runnable code samples in the [Aspose.Cells Cloud GitHub repository](https://github.com/aspose-cells-cloud).  
Gist examples below are pinned to commit `abc123` (2024-03-15) for stability.

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "abc123" "Example40_ExportTableAsFormat.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "abc123" "Example40_ExportTableAsFormat.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "abc123" "Example40_ExportTableAsFormat.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "abc123" "Example40_ExportTableAsFormat.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "abc123" "Example40_ExportTableAsFormat.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "abc123" "Example40_ExportTableAsFormat.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "abc123" "Example40_ExportTableAsFormat.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "abc123" "Example40_ExportTableAsFormat.go" >}}
{{< /tab >}}
{{< /tabs >}}

## API Reference

View the full specification: [ExportTableAsFormat (v4.0)](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportTableAsFormat)

## See Also

- [Export Worksheet to Format](/export-worksheet-as-format/)  
- [Convert Workbook to PDF/CSV](/convert-workbook/)  
- [SDK Support Guide](/sdk-support/)

---

{{% alert color="info" %}}
💡 **Pro Tip**: For styled PDF exports, include `autoRowsFit=true&autoColumnsFit=true&fontsLocation=custom-fonts` in the query string.  
{{% /alert %}}