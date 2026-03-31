---
title: "Aspose.Cells Cloud – Merge, Split & Import Spreadsheet Data"
second_title: "Document"
ArticleTitle: "Spreadsheet Data Processing – Merge, Split & Import"
linktitle: "Data Processing"
type: docs
url: /data-processing/
keywords: "Aspose.Cells, Cloud API, spreadsheet merge, spreadsheet split, data import"
description: "Learn how to import CSV/JSON, merge remote Excel files, and split worksheets using Aspose.Cells Cloud REST API."
weight: 30
---

**Aspose.Cells Cloud** – a RESTful service that enables programmatic manipulation of Excel files in the cloud. It supports importing data from various formats, merging workbooks, and splitting large spreadsheets.

The **Data Processing** section of Aspose.Cells Cloud API enables you to import, merge, and split spreadsheet data programmatically. Use the endpoints below to handle CSV/JSON imports, combine workbooks, or split large files into manageable pieces.

**Prerequisites**

- An active Aspose.Cloud account with a valid OAuth 2.0 access token.  
- Required scope: `Cells.ReadWrite`.  
- Supported storage locations: Aspose Cloud storage, Amazon S3, Azure Blob, Google Cloud Storage.  
- API version: **v3.0 (June 2026)**.

## Data Import and Management

- **[Import CSV, JSON, XML data into Excel files](https://docs.aspose.cloud/cells/import-data-into-spreadsheet/)**  
  - Supports multiple data‑format conversions,  
  - Batch data‑import processing,  
  - Field mapping and format preservation.  

  **When to use**  
  - *Use case*: Load external data sources into a workbook for further analysis.  
  - *Typical payload size*: Up to 50 MB per request.  
  - *Supported file types*: CSV, JSON, XML.

## File Merging Operation

### Basic Merging Functionality

- **[Merge Remote Excel Files into Specified Workbook](https://docs.aspose.cloud/cells/merge-remote-spreadsheet/)**  
  - Merging across cloud‑storage files,  
  - Sheet‑level merging control.  

  **When to use**  
  - *Use case*: Consolidate several workbooks stored in cloud storage into a single workbook.  
  - *Typical payload size*: Up to 200 MB total source size.  
  - *Supported file types*: XLSX, XLS, CSV.

### Batch Merging Function

- **[Merge Multiple Excel Files into a Single Workbook](https://docs.aspose.cloud/cells/merge-spreadsheets/)**  
  - Intelligent merging of multiple files,  
  - Automatic handling of conflicting data.  

  **When to use**  
  - *Use case*: Combine a collection of related reports into one comprehensive document.  
  - *Typical payload size*: Up to 500 MB aggregated source size.  
  - *Supported file types*: XLSX, XLS.

### Folder‑level Merging

- **[Merge Excel files that match in a remote folder](https://docs.aspose.cloud/cells/merge-spreadsheets-in-remote-folder/)**  
  - Filter files by rules,  
  - Batch folder operations.  

  **When to use**  
  - *Use case*: Merge all spreadsheets that follow a naming convention within a specific cloud folder.  
  - *Typical payload size*: Dependent on the number of matched files (recommended ≤ 1 GB total).  
  - *Supported file types*: XLSX, XLS.

## File Splitting Operation

### Worksheet Level Splitting

- **[Split an Excel file into multiple files based on worksheets](https://docs.aspose.cloud/cells/split-remote-spreadsheet/)**  
  - Each worksheet generates an independent file,  
  - Preserves formatting and formulas.  

  **When to use**  
  - *Use case*: Distribute individual worksheets to different stakeholders.  
  - *Typical payload size*: Up to 100 MB per source workbook.  
  - *Supported file types*: XLSX, XLS.

### Custom Rule Splitting

- **[Split Excel File According to Custom Rules](https://docs.aspose.cloud/cells/split-spreadsheet/)**  
  - Split by row count, column count, content conditions,  
  - Flexible rule‑based partitioning.  

  **When to use**  
  - *Use case*: Partition a large dataset into smaller, more manageable files for batch processing.  
  - *Typical payload size*: Up to 200 MB per source workbook.  
  - *Supported file types*: XLSX, XLS.

## Frequently Asked Questions

**How can I import JSON data into a spreadsheet using Aspose.Cells Cloud?**  
Use the `POST /cells/{fileName}/import/json` endpoint. Set `Content-Type: application/json` and include a mapping object that aligns JSON keys to worksheet columns.

**What is the best way to merge multiple workbooks stored in cloud storage?**  
Call the `POST /cells/merge` operation, providing a list of source file URIs (e.g., `https://mybucket.s3.amazonaws.com/file1.xlsx`). The API fetches each file, merges them, and returns a new workbook.

**Can I merge worksheets from different cloud storages in one request?**  
Yes. Provide full URIs for each source file—whether they reside in Aspose Cloud storage, Amazon S3, Azure Blob, or Google Cloud Storage—in the `sourceFiles` array of the `POST /cells/merge` call.

**What limits exist for splitting a workbook by rows?**  
The API allows up to **1 000 000 rows** per split file. Use the `rowsPerFile` parameter in the `POST /cells/split` request to define the chunk size.

**Which HTTP status codes indicate common errors, and how should I handle them?**  

| Status Code | Meaning                              | Remediation                              |
|-------------|--------------------------------------|------------------------------------------|
| 400         | Bad request – invalid parameters     | Verify required fields and data formats. |
| 401         | Unauthorized – token missing/invalid | Refresh the OAuth token.                 |
| 413         | Payload too large                    | Reduce file size or split before upload. |
| 500         | Internal server error                | Retry after a short delay; contact support if persistent. |

## Next Steps

- Explore the detailed endpoint documentation for each operation.  
- View SDK sample code (e.g., .NET 23.4, Java 23.4) in the **Aspose.Cells Cloud SDK** repository.  
- Follow the **Quick‑Start tutorial** to authenticate, upload a file, and perform a merge or split in under five minutes.  

---