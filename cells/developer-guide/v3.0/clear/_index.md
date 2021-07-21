---
title: "Clear"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /clear/
keywords: "REST API, convert, spreadsheets, excel, Clean object."
description: "Cells.Cloud API for Excel files Clear Object."
weight: 100
---

This REST API indicates `clear` excel object on Excel files.

**Query Parameter**

|Parameter Name|Type|Description|
| :- | :- | :- |
| objecttype | string |  Object type of cleaning object. Object type is include of chart, comment, picture and shape. |



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
