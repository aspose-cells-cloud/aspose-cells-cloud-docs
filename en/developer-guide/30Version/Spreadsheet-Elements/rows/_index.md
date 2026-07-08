---
title: "Working with Excel rows"
ArticleTitle: "Working with Excel Rows – Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "Rows"
type: docs
url: /rows/
aliases: [/working-with-rows/]
keywords: "Excel rows, Aspose.Cells Cloud, REST API, spreadsheet, row manipulation"
description: "Aspose.Cells Cloud REST API enables manipulation of rows in Excel files. The SDK provides support for multiple programming languages, including Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby, and Swift."
weight: 100
---

## Working with rows on an Excel file

- [How to get row information on an Excel worksheet.](/cells/rows/get/row/)
- [How to add an empty row on an Excel worksheet.](/cells/rows/add/row/)
- [How to copy rows on an Excel worksheet.](/cells/rows/copy/)
- [How to hide rows in an Excel worksheet.](/cells/rows/hide/)
- [How to unhide rows in an Excel worksheet.](/cells/rows/unhide/)
- [How to group rows in an Excel worksheet.](/cells/rows/group/)
- [How to ungroup rows in an Excel worksheet.](/cells/rows/ungroup/)
- [How to delete a row from a worksheet](/cells/rows/delete/)

Quick API reference for common row operations:

| Operation   | HTTP Method | Endpoint                                                               | Key Parameters                         |
|-------------|-------------|------------------------------------------------------------------------|----------------------------------------|
| Get Row     | GET         | `/cells/{fileName}/worksheets/{sheetName}/rows/{rowIndex}`            | `fileName`, `sheetName`, `rowIndex`    |
| Add Row     | POST        | `/cells/{fileName}/worksheets/{sheetName}/rows`                       | `rowIndex`, `height`                   |
| Copy Rows   | POST        | `/cells/{fileName}/worksheets/{sheetName}/rows/copy`                  | `sourceIndex`, `destinationIndex`, `rowCount` |
| Delete Row  | DELETE      | `/cells/{fileName}/worksheets/{sheetName}/rows/{rowIndex}`            | `fileName`, `sheetName`, `rowIndex`    |
| Hide Rows   | POST        | `/cells/{fileName}/worksheets/{sheetName}/rows/hide`                  | `startIndex`, `endIndex`               |
| Unhide Rows | POST        | `/cells/{fileName}/worksheets/{sheetName}/rows/unhide`                | `startIndex`, `endIndex`               |
| Group Rows  | POST        | `/cells/{fileName}/worksheets/{sheetName}/rows/group`                 | `startIndex`, `endIndex`               |
| Ungroup Rows| POST        | `/cells/{fileName}/worksheets/{sheetName}/rows/ungroup`               | `startIndex`, `endIndex`               |