---
title: "Aspose.Cells Cloud Web API – Transform Spreadsheet: Delete Empty Rows, Columns, Worksheets, Swap Ranges"
second_title: "Document"
ArticleTitle: "Transform Spreadsheet: Delete Empty Rows, Columns, Worksheets, and Swap Ranges"
linktitle: "Transform"
type: docs
url: /transform/
keywords: "Aspose, Cells, API, delete blank rows, delete blank columns, delete blank worksheets, swap range, spreadsheet cleanup"
description: "Use Aspose.Cells Cloud APIs to delete empty rows, columns, worksheets, and swap Excel ranges. Fast, cloud‑based data cleanup for automation."
weight: 40
---

Robust Excel data‑manipulation APIs for professional spreadsheet management. They delete blank columns, rows, and worksheets automatically and swap data between ranges seamlessly. Use them to prepare spreadsheets for analysis, reporting, or integration without installing Excel.

## Excel Data Cleanup & Optimization APIs

**Prerequisites** – Before calling any transformation API, obtain a valid authentication token and ensure the workbook is stored in a supported location (e.g., Aspose Cloud storage or a public URL). The token must be passed in the `Authorization` header of each request.

### Blank Content Cleanup

- **[Delete Blank Columns](https://docs.aspose.cloud/cells/delete-spreadsheet-blank-columns/)** – Automatically identify and remove columns that contain no data, formulas, or objects.  
- **[Delete Blank Rows](https://docs.aspose.cloud/cells/delete-spreadsheet-blank-rows/)** – Remove all empty rows while preserving worksheet structure.  
- **[Delete Blank Worksheets](https://docs.aspose.cloud/cells/delete-spreadsheet-blank-worksheets/)** – Clean up empty worksheets to reduce file size and improve organization.

### Data Manipulation & Reorganization

- **[Swap Range Data](https://docs.aspose.cloud/cells/swap-range/)** – Exchange data between any two ranges, columns, rows, or individual cells within an Excel file.

#### Quick Reference

| API | HTTP Method | Endpoint | Key Parameters | Sample Request |
|-----|--------------|----------|----------------|----------------|
| Delete Blank Columns | DELETE | `/cells/{fileName}/worksheets/{sheetName}/columns/blank` | `fileName`, `sheetName`, optional `storage` | `DELETE https://api.aspose.cloud/v3.0/cells/MyBook.xlsx/worksheets/Sheet1/columns/blank` |
| Delete Blank Rows | DELETE | `/cells/{fileName}/worksheets/{sheetName}/rows/blank` | `fileName`, `sheetName`, optional `storage` | `DELETE https://api.aspose.cloud/v3.0/cells/MyBook.xlsx/worksheets/Sheet1/rows/blank` |
| Delete Blank Worksheets | DELETE | `/cells/{fileName}/worksheets/blank` | `fileName`, optional `storage` | `DELETE https://api.aspose.cloud/v3.0/cells/MyBook.xlsx/worksheets/blank` |
| Swap Range Data | POST | `/cells/{fileName}/worksheets/{sheetName}/ranges/swap` | `fileName`, `sheetName`, `range1`, `range2`, optional `storage` | `POST https://api.aspose.cloud/v3.0/cells/MyBook.xlsx/worksheets/Sheet1/ranges/swap` (body: `{ "range1":"A1:B2", "range2":"C3:D4" }`) |

These concise snippets give developers immediate insight into how to call each transformation API without navigating away from the hub page.