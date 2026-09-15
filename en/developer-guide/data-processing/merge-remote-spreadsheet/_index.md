---
url: /merge-remote-spreadsheet/
title: "Merge Excel Files in Cloud via Aspose.Cells Cloud API"
date: 2024-05-10
lastmod: 2024-06-15
description: "Merge Excel files online via Aspose.Cells Cloud API — combine workbooks stored in AWS S3, Azure Blob, or Google Cloud Storage with output format control (XLSX, PDF, CSV). Free trial, no login required."
keywords: ["merge Excel files", "combine spreadsheets", "cloud API", "Aspose.Cells Cloud", "Excel workbook merge", "online Excel merge", "merge Excel files via API"]
weight: 100
---

Quickly merge Excel workbooks stored in cloud storage using Aspose.Cells Cloud API. Specify output format (e.g., XLSX, PDF, CSV), merge strategy (single or multiple worksheets), and target storage location in a single HTTPS call — all executed remotely, with no local file download required.

> **Note**: Before calling this operation, ensure you have:
> - A valid **JWT access token** (see our [JWT token guide](/getting-started/authentication/)).
> - All source workbooks uploaded to your cloud storage (AWS S3, Azure Blob, Google Cloud Storage, or Aspose Cloud default storage).
> - Read permissions on source folders and write permissions on target folders.

## Merge Remote Spreadsheet API

### REST API Endpoint

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/merge/spreadsheet
```

### Request Parameters

| Parameter Name    | Type    | Location | Required | Default | Description |
|-------------------|---------|----------|----------|---------|-------------|
| `name`            | String  | Path     | ✅ Yes   | —       | The name of the source workbook file to be merged. |
| `mergedSpreadsheet` | String | Query    | ✅ Yes   | —       | Comma-separated list of workbook file names to merge into the source. |
| `folder`          | String  | Query    | ❌ No     | `null`  | Folder path in cloud storage containing the source workbook. |
| `outFormat`       | String  | Query    | ❌ No     | `"xlsx"` | Output format: `XLSX`, `PDF`, `CSV`, `XLS`, `ODS`, etc. |
| `mergeInOneSheet` | Boolean | Query    | ❌ No     | `false` | `true`: merge all data into one worksheet; `false`: create separate worksheets per file. |
| `storageName`     | String  | Query    | ❌ No     | `null`  | Name of the storage where the source workbook resides (default storage used if omitted). |
| `outPath`         | String  | Query    | ❌ No     | `null`  | Target folder path in cloud storage for the merged output file. |
| `outStorageName`  | String  | Query    | ❌ No     | `null`  | Name of the storage for saving the output file. |
| `fontsLocation`   | String  | Query    | ❌ No     | `null`  | Custom folder path for fonts (used during conversion to PDF/image formats). |
| `region`          | String  | Query    | ❌ No     | `null`  | Locale/region for formatting (e.g., `en-US`, `de-DE`, `fr-FR`). Affects date/number/currency display. |
| `password`        | String  | Query    | ❌ No     | `null`  | Password for protected source workbook (if applicable). |

### Security & Authentication

All Aspose.Cells Cloud APIs require [JWT token-based authentication](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/){: rel="noopener noreferrer" target="_blank"}.

### Response

**Status:** `200 OK`  
**Content-Type:** `application/octet-stream`  
**Body:** Binary stream of the merged workbook file.

The file can be downloaded directly or saved to the location specified by `outPath`.

#### HTTP Status Codes

| Code | Meaning               | Description |
|------|-----------------------|-------------|
| `200` | OK | Merge and conversion successful. Response contains the merged file as a binary stream. |
| `400` | Bad Request | Invalid or missing parameters (e.g., unsupported file extension, malformed query). |
| `401` | Unauthorized | Invalid, expired, or missing JWT token. |
| `403` | Forbidden | Insufficient permissions to read source or write to output location. |
| `404` | Not Found | Source file or specified folder not found in storage. |
| `413` | Payload Too Large | Request exceeds size limits. |
| `500` | Internal Server Error | Unexpected error during processing (e.g., data corruption, service unavailable). |

### Example: cURL Request

```bash
curl -X PUT \
  "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/merge/spreadsheet?mergedSpreadsheet=Report1.xlsx,Report2.xlsx&outFormat=XLSX&mergeInOneSheet=true" \
  -H "Authorization: Bearer {access_token}"
```

> **Tip**: For local development and testing, use our [Postman collection](https://github.com/aspose-cells-cloud/aspose-cells-cloud-postman).

## Use Cases

### Enterprise Data Consolidation
- **Multi-department reporting**: Combine sales, marketing, and finance Excel reports into a unified summary.
- **Global branch consolidation**: Merge regional performance dashboards into one enterprise view.
- **Partner/vendor integration**: Aggregate order, quote, or feedback data from multiple external sources.

### Cloud-First Document Workflows
- **ETL pipeline enrichment**: Automate merge steps in data pipelines (e.g., merge daily transaction files before loading to BI tools).
- **Cross-storage consolidation**: Merge workbooks stored in AWS S3, Azure Blob, and Google Cloud Storage in one call.
- **Template population**: Inject dynamic data files into standardized reporting templates.

### Document Lifecycle Automation
- **Version consolidation**: Merge historic versions of a budget or project plan workbook into a single baseline.
- **Report scheduling**: Generate weekly/monthly summaries by automatically merging source files.
- **Compliance reporting**: Standardize audit-ready formats by merging source data into templated outputs.

### Remote & Collaborative Work
- **Distributed team coordination**: Merge deliverables from remote contributors into a final deliverable.
- **Customer/supplier data aggregation**: Combine product catalogs, pricing sheets, or order forms from multiple stakeholders.

## Why Use Aspose.Cells Cloud Merge API?

- ✅ **Zero infrastructure**: Fully managed cloud service — no servers, updates, or compatibility overhead.
- ✅ **Developer-friendly**: SDKs for C#, Java, PHP, Python, Node.js, Ruby, Perl, and Go — with full source examples.
- ✅ **Flexible output**: Generate consolidated workbooks in XLSX, PDF, CSV, and 20+ other formats.
- ✅ **Secure & scalable**: Enterprise-grade encryption, regional data residency, and auto-scaling.
- ✅ **Pay-per-use pricing**: No fixed costs — only pay for API calls made.

## SDK Examples

### C#
```csharp
var cellsApi = new CellsApi(clientId, clientSecret);
var mergedFile = "MyWorkbook.xlsx";
var sources = "Report1.xlsx,Report2.xlsx";
var result = cellsApi.CellsWorkbookMergeRemoteSpreadsheet(
    mergedFile, 
    sources, 
    folder: "input", 
    outFormat: "XLSX", 
    mergeInOneSheet: true);
File.WriteAllBytes("output.xlsx", result.fileContents);
```

### Java
```java
CellsApi cellsApi = new CellsApi(clientId, clientSecret);
String mergedFile = "MyWorkbook.xlsx";
String sources = "Report1.xlsx,Report2.xlsx";
File result = cellsApi.cellsWorkbookMergeRemoteSpreadsheet(
    mergedFile, sources, "input", "XLSX", true, null, null, null, null, null, null);
Files.copy(result.toPath(), Paths.get("output.xlsx"), StandardCopyOption.REPLACE_EXISTING);
```

### Python
```python
from asposecellscloud.api import CellsApi
from asposecellscloud.configuration import Configuration

config = Configuration(client_id, client_secret)
api = CellsApi(config)
response = api.cells_workbook_merge_remote_spreadsheet(
    "MyWorkbook.xlsx",
    merged_spreadsheet="Report1.xlsx,Report2.xlsx",
    folder="input",
    out_format="XLSX",
    merge_in_one_sheet=True
)
with open("output.xlsx", "wb") as f:
    f.write(response.file_contents)
```

> See full code samples in our [GitHub repository](https://github.com/aspose-cells-cloud){: rel="noopener noreferrer" target="_blank"}.

## Related Resources

- 📖 [Split Excel Files in Cloud](/split-spreadsheet/)  
- 🔐 [Authentication Guide](/getting-started/authentication/)  
- 📊 [Aspose.Cells Cloud API Reference](https://reference.aspose.cloud/cells/#/DataProcessingController/MergeRemoteSpreadsheet){: rel="noopener noreferrer" target="_blank"}  
- 🔄 [Compare Local vs Cloud Merge](/merge-local-spreadsheet/)  

> 💡 **Pro Tip**: Use `region` and `fontsLocation` parameters when generating PDFs or images for localized reports with custom fonts.