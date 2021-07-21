---
title: "Protect"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /protect/
keywords: "REST API, convert, spreadsheets, excel, Protect Excel file ."
description: "Cells.Cloud API for Excel files Split."
weight: 100
---

This REST API add  `protect` on an Excel file.

**Query Parameter**

|Parameter Name|Type|Description|
| :- | :- | :- |
| password | string |  Set protect password. |



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
