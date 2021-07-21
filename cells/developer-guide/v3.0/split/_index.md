---
title: "Split"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /split/
keywords: "REST API, convert, spreadsheets, excel, Split Excel file ."
description: "Cells.Cloud API for Excel files Split."
weight: 100
---

This REST API add  `split` on an Excel file.

**Query Parameter**

|Parameter Name|Type|Description|
| :- | :- | :- |
| format | string |  Out file format. The default value is xlsx. |
| from | int | The default value is zero.|
| to | int | The default value is worksheets.count - 1. |


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
