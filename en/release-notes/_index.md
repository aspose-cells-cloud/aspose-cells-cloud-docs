---
title: "Release Notes"
description: "Release notes for Aspose.Cells Cloud (2016–2024) — new features, API updates, bug fixes, and performance improvements for Excel, PDF, and CSV."
date: 2024-06-15T00:00:00Z
lastmod: 2024-06-15T00:00:00Z
draft: false
tags: ["release-notes", "api", "cloud", "excel"]
categories: ["documentation"]
weight: 40
ArticleTitle: "Aspose.Cells Cloud – Release Notes (2016–2024)"
keywords: "Aspose.Cells Cloud, release notes, 2024, 2023, 2022, 2021, 2020, 2019, 2018, 2017, 2016, API changes, bug fixes, new features, Excel, PDF, CSV"
---

## 2024

### Aspose.Cells Cloud 24.6
**Release Date:** June 15, 2024  
- Added support for Excel 2021 chart types and formatting enhancements  
- Improved handling of large pivot tables in memory-constrained environments  
- Fixed issue where `POST CellsWorkbookGetWorksheets` returned inconsistent ordering  
- Updated SDKs for Java, Python, Node.js, and .NET with improved async support  

### Aspose.Cells Cloud 24.3  
**Release Date:** March 12, 2024  
- Introduced new `POST CellsRangePutRangeValue` API for bulk cell value updates  
- Enhanced PDF export accuracy for complex formulas and conditional formatting  
- Resolved bug causing `429 Too Many Requests` errors during high-volume batch operations  
- Added deprecation notice for legacy `/v3.0` API endpoints (scheduled for removal in 2025)  

## 2023

### Aspose.Cells Cloud 23.12  
**Release Date:** December 14, 2023  
- Added support for Excel table styles (e.g., `TableStyleMedium9`)  
- Improved CSV import/export fidelity for scientific notation and date formats  
- Fixed race condition in concurrent `PUT CellsWorkbookSaveAs` requests  
- Updated documentation with new code samples for TypeScript and Go  

### Aspose.Cells Cloud 23.6  
**Release Date:** June 22, 2023  
- Added `POST CellsHtmlSuitableCompatibilityChecking` to validate HTML import compatibility  
- Fixed issue where `XLSX` files with embedded OLE objects corrupted on save  
- Optimized memory usage for large workbooks (>500MB) by up to 30%  
- Added `XLSB` format support for read operations  

## 2022

### Aspose.Cells Cloud 22.12  
**Release Date:** December 15, 2022  
- Introduced `POST CellsWorkbookConvert` for lightweight format conversion (XLSX ↔ PDF, XLSX ↔ HTML)  
- Added support for Excel sparklines in export to PDF/HTML  
- Fixed bug where `GET CellsWorkbookGetWorksheetCells` missed hidden rows  
- Improved error messaging for malformed JSON payloads  

## 2021–2016

*For earlier release notes (2016–2021), please see the archived documentation at:*  
[Aspose.Cells Cloud – Historical Release Notes (2016–2021)](/release-notes/historical/)