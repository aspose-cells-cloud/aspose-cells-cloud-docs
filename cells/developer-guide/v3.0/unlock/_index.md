---
title: "Unlock"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /unlock/
keywords: "REST API, spreadsheets, excel, Unlock Excel file ."
description: "Cells.Cloud API for Excel files Unlock."
weight: 100
---

This REST API indicates  `unlock` Excel files.

**Query Parameter**

|Parameter Name|Type|Description|
| :- | :- | :- |
| password | string |  unlock password. |


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
