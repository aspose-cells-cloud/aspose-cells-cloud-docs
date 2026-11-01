---
url: /merge-remote-spreadsheet/
title: "Merge Excel Files in Cloud via Aspose.Cells Cloud API"
linktitle: "Merge remote spreadsheet"
type: docs
description: "Merge Excel files online via Aspose.Cells Cloud API — combine workbooks stored in AWS S3, Azure Blob, or Google Cloud Storage with output format control (XLSX, PDF, CSV). Free trial, no login required."
keywords:
  [
    "merge Excel files",
    "combine spreadsheets",
    "cloud API",
    "Aspose.Cells Cloud",
    "Excel workbook merge",
    "online Excel merge",
    "merge Excel files via API",
  ]
weight: 100
ArticleTitle: "Merge Excel Files in Cloud with Aspose.Cells Cloud API"
---
The **MergeRemoteSpreadsheet** API (`PUT https://api.aspose.cloud/v4.0/cells/{name}/merge/spreadsheet`) enables developers to merge a remote spreadsheet file into an existing workbook stored in cloud storage and output the result in a specified format such as XLSX, PDF, or CSV, using Aspose.Cells Cloud’s remote processing—eliminating local file downloads and reducing data transfer by performing the merge entirely within the cloud environment.

> **Note**: Before calling this operation, ensure you have:
>
> - A valid **JWT access token** (see our [JWT token guide](/getting-started/authentication/)).
> - All source workbooks uploaded to your cloud storage (AWS S3, Azure Blob, Google Cloud Storage, or Aspose Cloud default storage).
> - Read permissions on source folders and write permissions on target folders.

## The Merge Remote Spreadsheet Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/merge/spreadsheet
```

### Security & Authentication

All Aspose.Cells Cloud APIs require [JWT token-based authentication](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/){: rel="noopener noreferrer" target="\_blank"}.

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| name | String | Path | The name of the workbook file to be split. |
| mergedSpreadsheet | String | Query | - |
| folder | String | Query | The folder path where the workbook is stored. |
| outFormat | String | Query | The out file format. |
| mergeInOneSheet | Boolean | Query | Whether to combine all data into a single worksheet. |
| storageName | String | Query | (Optional) The name of the storage if using custom cloud storage. Use default storage if omitted. |
| outPath | String | Query | (Optional) The folder path where the workbook is stored. The default is null. |
| outStorageName | String | Query | Output file Storage Name. |
| fontsLocation | String | Query | Use Custom fonts. |
| region | String | Query | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior. |
| password | String | Query | The password for opening spreadsheet file. |

### Response

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

**Status:** `200 OK`  
**Content-Type:** `application/octet-stream`  
**Body:** Binary stream of the merged workbook file.

The file can be downloaded directly or saved to the location specified by `outPath`.

#### HTTP Status Codes

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
