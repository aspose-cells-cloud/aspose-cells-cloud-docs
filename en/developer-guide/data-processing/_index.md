---
title: "Aspose.Cells Cloud – Merge, Split & Import Spreadsheet Data"
second_title: "Document"
ArticleTitle: "Spreadsheet Data Processing – Merge, Split & Import"
linktitle: "Data Processing"
type: docs
url: /data-processing/
keywords: "Aspose.Cells Cloud, spreadsheet data processing, Excel merge, Excel split, CSV import, JSON import, API"
description: "Detailed guide for importing CSV/JSON data, merging remote Excel workbooks, and splitting large spreadsheets using Aspose.Cells Cloud REST API, including request/response examples."
weight: 30
---

**Aspose.Cells Cloud** – a RESTful service that enables programmatic manipulation of Excel files in the cloud. It supports importing data from various formats, merging workbooks, and splitting large spreadsheets.

The **Data Processing** section of Aspose.Cells Cloud API enables you to import, merge, and split spreadsheet data programmatically. Use the endpoints below to handle CSV/JSON imports, combine workbooks, or split large files into manageable pieces.

## Data Import and Management

- **[Import CSV, JSON, XML data into Excel files](https://docs.aspose.cloud/cells/import-data-into-spreadsheet/)**  

The import operation accepts CSV, JSON, or XML payloads and creates a new worksheet (or updates an existing one) in the target workbook.

**Endpoint details**

| HTTP Method | Endpoint | Request Body | Success Response |
|-------------|----------|--------------|------------------|
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/import` | `application/json` or `text/csv` (depending on format) | `200 OK` with JSON containing the updated workbook metadata |
| GET | `https://api.aspose.cloud/v3.0/cells/{fileName}?format=excel` | *none* | Returns the processed workbook file |

**Sample cURL request (CSV import)**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/import" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: text/csv" \
     --data-binary @data.csv
```

**Sample JSON response**

```json
{
  "Code": 200,
  "Status": "OK",
  "Workbook": {
    "FileName": "MyWorkbook.xlsx",
    "Worksheets": 3
  }
}
```

> **Prerequisites**: An OAuth2 access token is required. The source file must reside in the Aspose Cloud storage or be provided via a multipart upload.

## File Merging Operation

- **[Merge Remote Excel Files into Specified Workbook](https://docs.aspose.cloud/cells/merge-remote-spreadsheet/)**
- **[Merge Multiple Excel Files into a Single Workbook](https://docs.aspose.cloud/cells/merge-spreadsheets/)**
- **[Merge Excel files that match in a remote folder](https://docs.aspose.cloud/cells/merge-spreadsheets-in-remote-folder/)**  

Merging combines two or more workbooks into a single target workbook. The API supports both explicit file lists and pattern‑based merges within a storage folder.

**Endpoint details**

| HTTP Method | Endpoint | Parameters | Success Response |
|-------------|----------|------------|------------------|
| POST | `https://api.aspose.cloud/v3.0/cells/merge` | `files` (array of file names), `target` (optional target workbook name) | `200 OK` with JSON describing the merged workbook |
| POST | `https://api.aspose.cloud/v3.0/cells/merge/remote` | `sourceFolder`, `pattern`, `target` | `200 OK` with merged workbook metadata |

**Sample cURL request (merge explicit list)**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/merge" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d '{
           "files": ["Book1.xlsx", "Book2.xlsx"],
           "target": "Combined.xlsx"
         }'
```

**Sample JSON response**

```json
{
  "Code": 200,
  "Status": "OK",
  "MergedWorkbook": {
    "FileName": "Combined.xlsx",
    "Worksheets": 10
  }
}
```

> **Prerequisites**: All source workbooks must be stored in the same cloud storage location and the caller must have read/write permissions.

## File Splitting Operation

- **[Split an Excel file into multiple files based on worksheets](https://docs.aspose.cloud/cells/split-remote-spreadsheet/)**
- **[Split Excel File According to Custom Rules](https://docs.aspose.cloud/cells/split-spreadsheet/)**  

Splitting extracts individual worksheets or groups of rows/columns into separate workbook files.

**Endpoint details**

| HTTP Method | Endpoint | Parameters | Success Response |
|-------------|----------|------------|------------------|
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/split` | `splitBy` (e.g., `worksheet`), `outputFolder` | `200 OK` with list of generated file URLs |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/split/custom` | Custom rule JSON (page size, row range, etc.) | `200 OK` with details of split files |

**Sample cURL request (split by worksheet)**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/BigReport.xlsx/split" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d '{
           "splitBy": "worksheet",
           "outputFolder": "Splits/"
         }'
```

**Sample JSON response**

```json
{
  "Code": 200,
  "Status": "OK",
  "Splits": [
    {"FileName": "BigReport_Sheet1.xlsx", "Url": "https://storage.aspose.cloud/..."},
    {"FileName": "BigReport_Sheet2.xlsx", "Url": "https://storage.aspose.cloud/..."}
  ]
}
```

> **Prerequisites**: The source workbook must be accessible in Aspose Cloud storage, and the caller needs write permission for the destination folder.