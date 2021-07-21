---
title: "Watermark"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /watermark/
keywords: "REST API, convert, spreadsheets, excel, Text Watermark."
description: "Cells.Cloud API for Excel file adding text watermark."
weight: 100
---

This REST API indicates add  `watermark` on Excel files.

**Query Parameter**

|Parameter Name|Type|Description|
| :- | :- | :- |
| text | string |  water mark content |
| color | string | water mark color |


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
