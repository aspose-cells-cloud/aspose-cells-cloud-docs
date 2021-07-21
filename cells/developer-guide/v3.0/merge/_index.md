---
title: "Merge"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /merge/
keywords: "REST API, convert, spreadsheets, excel, Merge  Excel file ."
description: "Cells.Cloud API for Excel files Merge."
weight: 100
---

This REST API add  `merge` on an Excel file.

**Query Parameter**

|Parameter Name|Type|Description|
| :- | :- | :- |
| format | string |  Out file format. The default value is xlsx. |
| mergeToOneSheet | boolean |  When the parameter is true, all worksheets import into a worksheet.  When the parameter is false, all worksheets import into a workbook.|


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
