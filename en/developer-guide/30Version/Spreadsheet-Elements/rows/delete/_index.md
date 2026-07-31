---
title: "Working with Deleting Rows on an Excel Worksheet"
second_title: "Document"
linktitle: "Delete"
type: docs
url: /rows/delete/
keywords: "Aspose.Cells, delete row, Excel API, REST, cloud, spreadsheet, Excel, SDK"
description: "Learn how to delete single or multiple rows in an Excel worksheet using the Aspose.Cells Cloud REST API. Includes code examples for Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby, and Swift."
weight: 20
ArticleTitle: "Working with Deleting Rows on an Excel Worksheet – Aspose.Cells Cloud API Guide"
---

## Available Deletion Operations

The following examples demonstrate how to delete a single empty row or multiple rows from an Excel worksheet using the Aspose.Cells Cloud REST API.

- [How to delete an empty row on an Excel worksheet](/cells/rows/delete/row/)
- [How to delete multiple rows on an Excel worksheet](/cells/rows/delete/rows/)

**API Reference**

| Item                | Details |
|---------------------|---------------------------------------------------------------|
| **HTTP Method**     | DELETE |
| **Endpoint**        | `/cells/{fileName}/worksheets/{sheetName}/rows` |
| **Path Parameters**| `fileName` – name of the Excel file (required)<br>`sheetName` – name of the worksheet (required) |
| **Query Parameters**| `startrow` – index of the first row to delete (required)<br>`totalRows` – number of rows to delete (required)<br>`storage` – cloud storage name (optional)<br>`folder` – folder path in storage (optional) |
| **Request Body**    | *None* |
| **Response Example**| ```json<br>{<br>  "Code": 200,<br>  "Status": "OK",<br>  "RowsDeleted": 1<br>}<br>``` |
| **Possible Status Codes**| 200 OK – rows deleted successfully<br>400 Bad Request – invalid parameters<br>401 Unauthorized – authentication failure<br>404 Not Found – file or worksheet not found<br>500 Internal Server Error – server‑side issue |

**See also**

- [Add Row](/cells/rows/add/)
- [Get Row](/cells/rows/get/)
- [Copy Row](/cells/rows/copy/)
- [Hide Row](/cells/rows/hide/)
- [Rows Overview](/cells/rows/)