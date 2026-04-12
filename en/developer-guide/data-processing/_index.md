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
  - _Use case_: Load external data sources into a workbook for further analysis.
  - _Typical payload size_: Up to 50 MB per request.
  - _Supported file types_: CSV, JSON, XML.

## File Merging Operation

### Basic Merging Functionality

- **[Merge Remote Excel Files into Specified Workbook](https://docs.aspose.cloud/cells/merge-remote-spreadsheet/)**
  - Merging across cloud‑storage files,
  - Sheet‑level merging control.

  **When to use**
  - _Use case_: Consolidate several workbooks stored in cloud storage into a single workbook.
  - _Typical payload size_: Up to 200 MB total source size.
  - _Supported file types_: XLSX, XLS, CSV.

### Batch Merging Function

- **[Merge Multiple Excel Files into a Single Workbook](https://docs.aspose.cloud/cells/merge-spreadsheets/)**
  - Intelligent merging of multiple files,
  - Automatic handling of conflicting data.

  **When to use**
  - _Use case_: Combine a collection of related reports into one comprehensive document.
  - _Typical payload size_: Up to 500 MB aggregated source size.
  - _Supported file types_: XLSX, XLS.

### Folder‑level Merging

- **[Merge Excel files that match in a remote folder](https://docs.aspose.cloud/cells/merge-spreadsheets-in-remote-folder/)**
  - Filter files by rules,
  - Batch folder operations.

  **When to use**
  - _Use case_: Merge all spreadsheets that follow a naming convention within a specific cloud folder.
  - _Typical payload size_: Dependent on the number of matched files (recommended ≤ 1 GB total).
  - _Supported file types_: XLSX, XLS.

## File Splitting Operation

### Worksheet Level Splitting

- **[Split an Excel file into multiple files based on worksheets](https://docs.aspose.cloud/cells/split-remote-spreadsheet/)**
  - Each worksheet generates an independent file,
  - Preserves formatting and formulas.

  **When to use**
  - _Use case_: Distribute individual worksheets to different stakeholders.
  - _Typical payload size_: Up to 100 MB per source workbook.
  - _Supported file types_: XLSX, XLS.

### Custom Rule Splitting

- **[Split Excel File According to Custom Rules](https://docs.aspose.cloud/cells/split-spreadsheet/)**
  - Split by row count, column count, content conditions,
  - Flexible rule‑based partitioning.

  **When to use**
  - _Use case_: Partition a large dataset into smaller, more manageable files for batch processing.
  - _Typical payload size_: Up to 200 MB per source workbook.
  - _Supported file types_: XLSX, XLS.
