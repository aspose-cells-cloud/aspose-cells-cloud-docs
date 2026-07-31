---
title: "Spreadsheet Operations"
second_title: "Document"
type: docs
url: /spreadsheet-operations/
keywords: "Aspose Cells Cloud, Excel API, spreadsheet operations, auto fit, batch processing, file protection, conversion, import export, text processing"
description: "Learn how to perform spreadsheet operations such as auto‑fit, batch conversion, protection, merging, and search‑replace using Aspose.Cells Cloud REST API. Includes concise usage notes and code‑sample guidance."
weight: 100
ArticleTitle: "Spreadsheet Operations – Aspose.Cells Cloud API Guide"
---

Spreadsheet Operations provides a concise guide to the most common actions you can perform on Excel workbooks with **Aspose.Cells Cloud** (v3.0). Whether you need to auto‑fit columns, batch‑process files, protect worksheets, or manipulate text, the REST API offers dedicated endpoints that work across languages like Python, C#, and Java. The list below links to the detailed documentation for each operation and includes a brief usage note to help you get started quickly.

**Prerequisites**: To call these endpoints you must have a valid Aspose.Cells Cloud API key and include the `Authorization` header (`Bearer <access-token>`). The examples assume API version v3.0.

- **[Auto Fitter Options](/cells/auto-fitter-options/)** – Automatically adjusts column widths and row heights. `POST /cells/{file}/worksheets/{sheet}/autoFitColumns`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/autoFitColumns
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "autoFitOptions": {
      "autoFitType": "All",
      "autoFitMergedCells": true
    }
  }
  ```
- **[Batch processing of Excel files: conversion, lock, protect, split, and unlock](/cells/batch/)** – Perform bulk actions (convert, lock, protect, split, unlock) on up to 100 files per request. `POST /cells/batch`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/batch
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "tasks": [
      { "file": "Book1.xlsx", "action": "convert", "format": "pdf" },
      { "file": "Book2.xlsx", "action": "protect", "password": "Secret123" }
    ]
  }
  ```
- **[Compress and Repair Excel Files](/cells/compress-and-repair-excel-files/)** – Reduces file size and fixes structural issues. `POST /cells/{file}/compressAndRepair`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Report.xlsx/compressAndRepair
  Authorization: Bearer {access-token}
  ```
- **[Convert an Excel file to another format or save it differently](/cells/conversion-and-save-as/)** – Convert Excel to PDF, CSV, HTML, etc., or change the output format. `GET /cells/{file}/saveAs`  
  ```http
  GET https://api.aspose.cloud/v3.0/cells/Financials.xlsx/saveAs?format=pdf
  Authorization: Bearer {access-token}
  ```
- **[Convert Workbook Options](/cells/convert-workbook-options/)** – Fine‑tune conversion settings such as page size, rendering options, and password protection. `POST /cells/{file}/convert`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Presentation.xlsx/convert
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "format": "pdf",
    "options": {
      "pageSetup": { "orientation": "landscape" },
      "pdfSaveOptions": { "compressImages": true }
    }
  }
  ```
- **[Create Excel Files or Build Excel Reports](/cells/creating-files-and-reports/)** – Generate new workbooks from scratch or from templates. `PUT /cells/{newFile}`  
  ```http
  PUT https://api.aspose.cloud/v3.0/cells/NewReport.xlsx
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "templateFile": "Template.xlsx",
    "dataSource": { "name": "Q1 Sales", "value": 12345 }
  }
  ```
- **[Import Data into Excel files and Export data from Excel files](/cells/data-import-and-export/)** – Load data from CSV, JSON, or databases and export worksheet data. `POST /cells/{file}/importData`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Orders.xlsx/importData
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "importOptions": {
      "source": "json",
      "jsonData": [{ "OrderId": 1, "Amount": 250.0 }]
    }
  }
  ```
- **[Encrypt, Decrypt, and Digitally Sign Excel Files](/cells/protect/)** – Apply password protection, encryption, or digital signatures. `POST /cells/{file}/encrypt`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Sensitive.xlsx/encrypt
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "password": "StrongPass!23",
    "encryptionType": "Standard"
  }
  ```
- **[File Info](/cells/file-info/)** – Retrieve metadata such as size, format, and creation date. `GET /cells/{file}/info`  
  ```http
  GET https://api.aspose.cloud/v3.0/cells/Archive.xlsx/info
  Authorization: Bearer {access-token}
  ```
- **[Merge and Split Excel Files](/cells/merge-and-split/)** – Combine multiple workbooks into one or split a workbook into separate files. `POST /cells/merge` / `POST /cells/split`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/merge
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "files": ["Q1.xlsx", "Q2.xlsx"],
    "outputFile": "FullYear.xlsx"
  }
  ```
- **[Search and Replace text content within Excel Files](/cells/search-and-replace/)** – Find and replace strings across worksheets. `POST /cells/{file}/searchReplace`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Report.xlsx/searchReplace
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "text": "Draft",
    "newText": "Final",
    "options": { "matchCase": false }
  }
  ```
- **[Excel Text Processing: Add Text, Remove Characters, Trim Text, Update Word Case, and More](/cells/text-processing/)** – Perform advanced text manipulations on cell values. `POST /cells/{file}/textProcessing`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Notes.xlsx/textProcessing
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "operations": [
      { "type": "trim", "range": "A1:A10" },
      { "type": "toUpper", "range": "B1:B5" }
    ]
  }
  ```
- **[Insert Watermarks or Set Backgrounds in Excel Files](/cells/watermark-and-background/)** – Add image or text watermarks and set worksheet backgrounds. `POST /cells/{file}/watermark`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Presentation.xlsx/watermark
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "type": "text",
    "text": "Confidential",
    "fontSize": 36,
    "color": "FF0000"
  }
  ```
- **[Working with Excel Files: Formula Calculation, Auto‑Fit, Clear Objects, etc.](/cells/workbook/)** – Execute common workbook tasks like calculating formulas, clearing objects, and auto‑fitting. `POST /cells/{file}/workbookOperations`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Analytics.xlsx/workbookOperations
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "operations": [
      { "type": "calculateFormula" },
      { "type": "clearObjects", "objectType": "charts" }
    ]
  }
  ```