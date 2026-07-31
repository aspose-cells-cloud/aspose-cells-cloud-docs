---
title: "Working with Excel Rows – Aspose.Cells Cloud API"
ArticleTitle: "Working with Excel Rows – Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "Rows"
type: docs
url: /rows/
aliases: [/working-with-rows/]
keywords: "Aspose.Cells, Excel rows, REST API, spreadsheet manipulation"
description: "Manipulate rows in Excel files using Aspose.Cells Cloud REST API. Supports Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby, and Swift."
weight: 100
---

## Working with rows on an Excel file

**Last updated: July 2026**

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
| [Get Row](https://docs.aspose.cloud/cells/rows/get/row/)     | GET         | `/cells/{fileName}/worksheets/{sheetName}/rows/{rowIndex}`            | `fileName`, `sheetName`, `rowIndex`    |
| [Add Row](https://docs.aspose.cloud/cells/rows/add/row/)     | POST        | `/cells/{fileName}/worksheets/{sheetName}/rows`                       | `rowIndex`, `height`                   |
| [Copy Rows](https://docs.aspose.cloud/cells/rows/copy/)      | POST        | `/cells/{fileName}/worksheets/{sheetName}/rows/copy`                  | `sourceIndex`, `destinationIndex`, `rowCount` |
| [Delete Row](https://docs.aspose.cloud/cells/rows/delete/)   | DELETE      | `/cells/{fileName}/worksheets/{sheetName}/rows/{rowIndex}`            | `fileName`, `sheetName`, `rowIndex`    |
| [Hide Rows](https://docs.aspose.cloud/cells/rows/hide/)      | POST        | `/cells/{fileName}/worksheets/{sheetName}/rows/hide`                  | `startIndex`, `endIndex`               |
| [Unhide Rows](https://docs.aspose.cloud/cells/rows/unhide/)  | POST        | `/cells/{fileName}/worksheets/{sheetName}/rows/unhide`                | `startIndex`, `endIndex`               |
| [Group Rows](https://docs.aspose.cloud/cells/rows/group/)    | POST        | `/cells/{fileName}/worksheets/{sheetName}/rows/group`                 | `startIndex`, `endIndex`               |
| [Ungroup Rows](https://docs.aspose.cloud/cells/rows/ungroup/)| POST        | `/cells/{fileName}/worksheets/{sheetName}/rows/ungroup`               | `startIndex`, `endIndex`               |

**Request / Response details**

- **Get Row**  
  *Request*: No body required.  
  *Response (200)*:  
  ```json
  {
    "RowIndex": 5,
    "Height": 15.0,
    "IsHidden": false,
    "Style": { ... }
  }
  ```  
  *Errors*: 400 Bad Request (invalid index), 404 Not Found (file or sheet missing).

- **Add Row**  
  *Request body (JSON)*:  
  ```json
  {
    "RowIndex": 10,
    "Height": 20.0
  }
  ```  
  *Response (201)*:  
  ```json
  { "Code": "Success", "Status": "Row added", "RowIndex": 10 }
  ```  
  *Errors*: 400 Bad Request (missing/invalid parameters), 401 Unauthorized.

- **Copy Rows**  
  *Request body (JSON)*:  
  ```json
  {
    "SourceIndex": 2,
    "DestinationIndex": 8,
    "RowCount": 3
  }
  ```  
  *Response (200)*:  
  ```json
  { "Code": "Success", "Status": "Rows copied" }
  ```  
  *Errors*: 400 Bad Request, 404 Not Found.

- **Delete Row**  
  *Request*: No body.  
  *Response (200)*:  
  ```json
  { "Code": "Success", "Status": "Row deleted", "RowIndex": 7 }
  ```  
  *Errors*: 400 Bad Request, 404 Not Found.

- **Hide Rows**  
  *Request body (JSON)*:  
  ```json
  { "StartIndex": 3, "EndIndex": 5 }
  ```  
  *Response (200)*: `{ "Code": "Success", "Status": "Rows hidden" }`  
  *Errors*: 400 Bad Request.

- **Unhide Rows** – same payload as *Hide Rows*; response identical, status “Rows unhidden”.

- **Group Rows** – same payload as *Hide Rows*; response status “Rows grouped”.

- **Ungroup Rows** – same payload as *Hide Rows*; response status “Rows ungrouped”.

All operations require a valid OAuth 2.0/JWT access token and appropriate SDK version.  

---