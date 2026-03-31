---
title: "Spreadsheet Operations"
second_title: "Document"
type: docs
url: /spreadsheet-operations/
keywords: "Aspose Cells Cloud, Excel API, spreadsheet operations, REST API, Python, C#, Java, code examples"
description: "Learn how to perform spreadsheet operations such as auto‑fit, batch conversion, protection, merging, and search‑replace using Aspose.Cells Cloud REST API. Includes concise usage notes and code‑sample guidance."
weight: 100
---

Spreadsheet Operations provides a concise guide to the most common actions you can perform on Excel workbooks with **Aspose.Cells Cloud** (v3.0). Whether you need to auto‑fit columns, batch‑process files, protect worksheets, or manipulate text, the REST API offers dedicated endpoints that work across languages like Python, C#, and Java. The list below links to the detailed documentation for each operation and includes a brief usage note to help you get started quickly.

- **[Auto Fitter Options](https://docs.aspose.cloud/cells/auto-fitter-options/)** – Automatically adjusts column widths and row heights. `POST /cells/{file}/worksheets/{sheet}/autoFitColumns`.
- **[Batch processing of Excel files: conversion, lock, protect, split, and unlock](https://docs.aspose.cloud/cells/batch/)** – Perform bulk actions (convert, lock, protect, split, unlock) on up to 100 files per request. `POST /cells/batch`.
- **[Compress and Repair Excel Files](https://docs.aspose.cloud/cells/compress-and-repair-excel-files/)** – Reduces file size and fixes structural issues. `POST /cells/{file}/compressAndRepair`.
- **[Convert an Excel file to another format or save it differently](https://docs.aspose.cloud/cells/conversion-and-save-as/)** – Convert Excel to PDF, CSV, HTML, etc., or change the output format. `GET /cells/{file}/saveAs`.
- **[Convert Workbook Options](https://docs.aspose.cloud/cells/convert-workbook-options/)** – Fine‑tune conversion settings such as page size, rendering options, and password protection. `POST /cells/{file}/convert`.
- **[Create Excel Files or Build Excel Reports](https://docs.aspose.cloud/cells/creating-files-and-reports/)** – Generate new workbooks from scratch or from templates. `PUT /cells/{newFile}`.
- **[Import Data into Excel files and Export data from Excel files](https://docs.aspose.cloud/cells/data-import-and-export/)** – Load data from CSV, JSON, or databases and export worksheet data. `POST /cells/{file}/importData`.
- **[Encrypt, Decrypt, and Digitally Sign Excel Files](https://docs.aspose.cloud/cells/protect/)** – Apply password protection, encryption, or digital signatures. `POST /cells/{file}/encrypt`.
- **[File Info](https://docs.aspose.cloud/cells/file-info/)** – Retrieve metadata such as size, format, and creation date. `GET /cells/{file}/info`.
- **[Merge and Split Excel Files](https://docs.aspose.cloud/cells/merge-and-split/)** – Combine multiple workbooks into one or split a workbook into separate files. `POST /cells/merge` / `POST /cells/split`.
- **[Search and Replace text content within Excel Files](https://docs.aspose.cloud/cells/search-and-replace/)** – Find and replace strings across worksheets. `POST /cells/{file}/searchReplace`.
- **[Excel Text Processing: Add Text, Remove Characters, Trim Text, Update Word Case, and More](https://docs.aspose.cloud/cells/text-processing/)** – Perform advanced text manipulations on cell values. `POST /cells/{file}/textProcessing`.
- **[Insert Watermarks or Set Backgrounds in Excel Files](https://docs.aspose.cloud/cells/watermark-and-background/)** – Add image or text watermarks and set worksheet backgrounds. `POST /cells/{file}/watermark`.
- **[Working with Excel Files: Formula Calculation, Auto‑Fit, Clear Objects, etc.](https://docs.aspose.cloud/cells/workbook/)** – Execute common workbook tasks like calculating formulas, clearing objects, and auto‑fitting. `POST /cells/{file}/workbookOperations`.