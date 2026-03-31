---
title: "Import JSON Data into Excel"
second_title: "Document"
linktitle: "Import JSON"
type: docs
url: /import-json-data-into-excel/
aliases: [ /import/json/]
keywords: "Aspose.Cells Cloud, JSON import, Excel API, REST import JSON, SDK examples"
description: "Learn how to import JSON data into an Excel worksheet using Aspose.Cells Cloud REST API. Includes endpoint details, request/response examples, and SDK code for .NET, Java, and Python."
weight: 40
---

This REST API **imports JSON data** into an Excel worksheet.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/importjson
```

The important parameters are described in the table below.

**Import JSON**

| Parameter Name          | Location        | Type   | Description                                                                                     |
|-------------------------|-----------------|--------|-------------------------------------------------------------------------------------------------|
| name                    | Path            | string | The name of the workbook file.                                                                  |
| importJsonRequest       | HTTP body       | class  | The request payload that contains JSON import details.                                         |
| password                | Query string    | string | Password for opening the workbook (if protected).                                              |
| folder                  | Query string    | string | The folder that contains the original workbook.                                                |
| storageName             | Query string    | string | The name of the storage where the workbook resides.                                            |
| outPath                 | Query string    | string | Path for the output file after import. If omitted, the updated workbook is returned in the response. |
| outStorageName          | Query string    | string | Storage name for the output file.                                                               |
| checkExcelRestriction  | Query string    | string | Flag indicating whether to enforce Excel‑specific restrictions (true/false).                  |

**Example Request Body**

```json
{
  "JsonFileSource": {
    "FilePath": "string"
  },
  "ImportPosition": {
    "SheetName": "string",
    "RowIndex": 0,
    "ColumnIndex": 0
  },
  "JsonContent": "string"
}
```

## Cloud SDK Family

Using an SDK is the most efficient way to accelerate development. SDKs handle low‑level details, allowing you to focus on your business logic. For a complete list of Aspose.Cells Cloud SDKs, please visit the [GitHub repository](https://github.com/aspose-cells-cloud).

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

```
// (Insert SDK-specific example code here)
```