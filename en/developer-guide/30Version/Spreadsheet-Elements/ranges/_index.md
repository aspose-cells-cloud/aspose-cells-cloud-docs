---
title: "Working with Excel Ranges"
second_title: "Document"
linktitle: "Range"
type: docs
url: /ranges/
aliases: [/working-with-ranges/]
keywords: "Aspose.Cells, Excel range, REST API, SDK, .NET, Java, Python, merge cells, copy range, set range value"
description: "Learn how to retrieve, modify, style, merge, move, and copy Excel ranges using the Aspose.Cells Cloud REST API. Includes SDK code samples for .NET, Java, Python, and more."
date: 2023-11-15
robots: index, follow
canonical: /ranges/
weight: 100
ArticleTitle: "Working with Excel Ranges – Aspose.Cells Cloud Documentation"
---

A **range** represents a single cell, an entire row, a whole column, a contiguous block of cells, or a three‑dimensional (3‑D) range that spans multiple worksheets.

## Overview of Range Operations

The Aspose.Cells Cloud REST API provides dedicated endpoints for each range operation. The following list links to detailed usage examples and includes the corresponding HTTP method and endpoint for quick reference.

- [Get Named Ranges inside the Workbook](/cells/get-named-ranges-inside-the-workbook/) – Retrieves all named ranges defined in a workbook, returning their addresses and scope. **API**: `GET /cells/{fileName}/worksheets/{sheetName}/namedranges`.
- [Get Cells Data Based on Named Range](/cells/get-cells-data-based-on-named-range/) – Returns cell values in the specified named range. **API**: `GET /cells/{fileName}/worksheets/{sheetName}/namedranges/{rangeName}/cells`.
- [Update Row Heights in Range](/cells/update-row-heights-in-range/) – Adjusts the height of each row that falls within the given range. **API**: `PUT /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/rows/height`.
- [Update Column Widths in Range](/cells/update-column-widths-in-range/) – Modifies the column width for all columns intersecting the range. **API**: `PUT /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/columns/width`.
- [Merge Cells in Range](/cells/merge-cells-in-range/) – Merges the selected cells into one cell, preserving the top‑left value. **API**: `POST /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/merge`.
- [Copy Range in a Worksheet with Paste Options](/cells/copy-range-in-a-worksheet-with-paste-options/) – Copies a source range to a destination range with optional paste types (values, formats, formulas, etc.). **API**: `POST /cells/{fileName}/worksheets/{sheetName}/ranges/{sourceRange}/copy?destCell={destRange}&pasteType={type}`.
- [Set the Style of the Range](/cells/set-the-style-of-the-range/) – Applies font, fill, border, and alignment styles to every cell in the range. **API**: `PUT /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/style`.
- [Unmerge Merged Cells in Range](/cells/unmerge-merged-cells-in-range/) – Reverses a previous merge operation, restoring the original individual cells. **API**: `POST /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/unmerge`.
- [Move a Named Range with an Excel Worksheet](/cells/move-a-named-range-with-an-excel-worksheet/) – Relocates a named range to a new address within the same worksheet or to another worksheet. **API**: `PUT /cells/{fileName}/worksheets/{sheetName}/namedranges/{rangeName}/move`.
- [Set Range Value in Excel Worksheet](/cells/ranges/set-value/) – Writes a single value or an array of values to the specified range. **API**: `PUT /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/value`.

All requests and responses are in JSON format. Include the `Authorization` header with your access token for authentication.

> **Prerequisites**  
> Requires a valid Aspose.Cells Cloud API key. See [Authentication Guide]（https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/） for setup instructions.
