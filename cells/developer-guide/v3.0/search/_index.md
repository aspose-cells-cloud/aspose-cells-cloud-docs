---
title: "Search"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /search/
keywords: "REST API, spreadsheets, excel, Search Excel file ."
description: "Cells.Cloud API for Excel files Search."
weight: 100
---

This REST API indicates  `search` text on Excel files.

**Query Parameter**

|Parameter Name|Type|Description|
| :- | :- | :- |
| text | string |  search context. |
| sheetname | string | point to worksheet.|

**Request Body Parameter**

|Parameter Name|Type|Description|
| :- | :- | :- |
|excel file|data file | The data file save into the first part of the multipart content.|

**Response**

```bash
{
    "Files":
    [
        { 
            "Filename":"xxxxx",
            "FileSize":274022,
            "FileContent":"-----Base64String--------"
        },
        { 
            "Filename":"xxxxx",
            "FileSize":274022,
            "FileContent":"-----Base64String--------"
        }
    ]
}
```
