---
title: "How to update range content from an Excel worksheet"
second_title: "Document"
linktitle: "Update"
type: docs
url: /ranges/update/
keywords: "Excel, range update, Aspose.Cells Cloud, REST API, spreadsheet, range style, range values, row height, column width"
description: "Update range content in an Excel worksheet using Aspose.Cells Cloud REST API. Modify styles, values, row heights, and column widths via supported SDKs."
weight: 20
ArticleTitle: "How to update range content from an Excel worksheet – Aspose.Cells Cloud Documentation"
---

## Working with updating range content on an Excel worksheet

Before using the update operations, ensure you have a valid Aspose.Cells Cloud API token and that the target workbook is stored in your cloud storage. The API is available through SDKs for Android, .NET, Go, Java, Node.js, Perl, PHP, Python, Ruby, and Swift.

A concise summary of the four primary update actions is provided below. This table gives developers a quick reference to the HTTP method, endpoint pattern, key parameters, and typical success response for each operation.

| Action          | HTTP Method | Endpoint Pattern                                                                                     | Key Parameters                | 200‑OK Response               |
|-----------------|-------------|------------------------------------------------------------------------------------------------------|-------------------------------|------------------------------|
| Set style       | PUT         | `/cells/{fileName}/worksheets/{sheetName}/ranges/{range}/style`                                      | `style` object                | Updated range style          |
| Set values      | POST        | `/cells/{fileName}/worksheets/{sheetName}/ranges/{range}/values`                                    | `values` array                | Updated range values         |
| Row height      | PUT         | `/cells/{fileName}/worksheets/{sheetName}/ranges/{range}/rowheight`                                 | `height` number               | Updated row height           |
| Column width    | PUT         | `/cells/{fileName}/worksheets/{sheetName}/ranges/{range}/columnwidth`                               | `width` number                | Updated column width         |

This page provides quick access to the four main update actions: setting the style of a range, setting the values of a range, adjusting row heights, and adjusting column widths.

- [How to set the style of a range on an Excel worksheet.](/cells/ranges/update/style/) 
- [How to set the values of a range on an Excel worksheet.](/cells/ranges/update/values/) 
- [How to set the row heights of a range on an Excel worksheet.](/cells/ranges/update/row-height/) 
- [How to set the column widths of a range on an Excel worksheet.](/cells/ranges/update/column-width/)