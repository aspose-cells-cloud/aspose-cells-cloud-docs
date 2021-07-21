---
title: "Assembly"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /assembly/
keywords: "REST API, convert, spreadsheets, excel, Assembly."
description: "Cells.Cloud API for Excel files Assembly."
weight: 100
---

This REST API indicates `assembly` data in an Excel file.

**Query Parameter**

|Parameter Name|Type|Description|
| :- | :- | :- |
| datasource | string |  Data source name. |
| format | string | Out file format. Default value is xlsx. |


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
