---
title: "Working with Excel Rows – Aspose.Cells Cloud API"
ArticleTitle: "Working with Excel Rows – Aspose.Cells Cloud API"
second_title: "Developer Guide"
linktitle: "Rows"
type: docs
url: /rows/
aliases: [/working-with-rows/]
keywords:
  [
    "Excel row API",
    "cloud spreadsheet manipulation",
    "REST API rows",
    "Aspose.Cells row operations",
    "programmatically hide rows",
  ]
description: "Use Aspose.Cells Cloud REST API to programmatically manage Excel rows—get, add, copy, hide, group, ungroup, and delete rows in worksheets."
weight: 100
lastmod: 2024-06-15
---

## Working with rows on an Excel file

**Last updated: June 2024**

- Get row information
- Add an empty row
- Copy rows
- Hide rows
- Unhide rows
- Group rows
- Ungroup rows
- Delete a row

Quick API reference for common row operations:

| Operation                            | HTTP Method | Endpoint                                                   | Key Parameters                                |
| ------------------------------------ | ----------- | ---------------------------------------------------------- | --------------------------------------------- |
| [Get Row](/cells/rows/get/row/)      | GET         | `/cells/{fileName}/worksheets/{sheetName}/rows/{rowIndex}` | `fileName`, `sheetName`, `rowIndex`           |
| [Add Row](/cells/rows/add/row/)      | POST        | `/cells/{fileName}/worksheets/{sheetName}/rows`            | `rowIndex`, `height`                          |
| [Copy Rows](/cells/rows/copy/)       | POST        | `/cells/{fileName}/worksheets/{sheetName}/rows/copy`       | `sourceIndex`, `destinationIndex`, `rowCount` |
| [Delete Row](/cells/rows/delete/)    | DELETE      | `/cells/{fileName}/worksheets/{sheetName}/rows/{rowIndex}` | `fileName`, `sheetName`, `rowIndex`           |
| [Hide Rows](/cells/rows/hide/)       | POST        | `/cells/{fileName}/worksheets/{sheetName}/rows/hide`       | `startIndex`, `endIndex`                      |
| [Unhide Rows](/cells/rows/unhide/)   | POST        | `/cells/{fileName}/worksheets/{sheetName}/rows/unhide`     | `startIndex`, `endIndex`                      |
| [Group Rows](/cells/rows/group/)     | POST        | `/cells/{fileName}/worksheets/{sheetName}/rows/group`      | `startIndex`, `endIndex`                      |
| [Ungroup Rows](/cells/rows/ungroup/) | POST        | `/cells/{fileName}/worksheets/{sheetName}/rows/ungroup`    | `startIndex`, `endIndex`                      |

**Request / Response details**

- **Get Row**  
  _Request_: No body required.  
  _Response (200)_:

  ```json
  {
    "RowIndex": 5,
    "Height": 15.0,
    "IsHidden": false,
    "Style": { ... }
  }
  ```

  _Errors_: 400 Bad Request (invalid index), 404 Not Found (file or sheet missing).

- **Add Row**  
  _Request body (JSON)_:

  ```json
  {
    "RowIndex": 10,
    "Height": 20.0
  }
  ```

  _Response (201)_:

  ```json
  { "Code": "Success", "Status": "Row added", "RowIndex": 10 }
  ```

  _Errors_: 400 Bad Request (missing/invalid parameters), 401 Unauthorized.

- **Copy Rows**  
  _Request body (JSON)_:

  ```json
  {
    "SourceIndex": 2,
    "DestinationIndex": 8,
    "RowCount": 3
  }
  ```

  _Response (200)_:

  ```json
  { "Code": "Success", "Status": "Rows copied" }
  ```

  _Errors_: 400 Bad Request, 404 Not Found.

- **Delete Row**  
  _Request_: No body.  
  _Response (200)_:

  ```json
  { "Code": "Success", "Status": "Row deleted", "RowIndex": 7 }
  ```

  _Errors_: 400 Bad Request, 404 Not Found.

- **Hide Rows**  
  _Request body (JSON)_:

  ```json
  { "StartIndex": 3, "EndIndex": 5 }
  ```

  _Response (200)_: `{ "Code": "Success", "Status": "Rows hidden" }`  
  _Errors_: 400 Bad Request.

- **Unhide Rows** – same payload as _Hide Rows_; response identical, status “Rows unhidden”.

- **Group Rows** – same payload as _Hide Rows_; response status “Rows grouped”.

- **Ungroup Rows** – same payload as _Hide Rows_; response status “Rows ungrouped”.

All operations require a valid OAuth 2.0/JWT access token and appropriate SDK version.
