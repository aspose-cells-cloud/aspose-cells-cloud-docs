---
title: "Import JSON data into Excel"
second_title: "Document"
linktitle: "Import Json"
type: docs
url: /import-json-data-into-excel/
aliases: [ /import/json/]
keywords: "Import JSON, Excel, Aspose.Cells Cloud, REST API, SDK, Spreadsheet"
description: "Use Aspose.Cells Cloud REST API to import JSON data into Excel worksheets. Supports multiple SDKs (Android, .NET, Go, Java, Node.js, Perl, PHP, Python, Ruby, Swift) for easy integration."
weight: 40
---

This REST API **imports JSON data** into an Excel worksheet.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/importjson
```

The important parameters are described in the table below.

**ImportStringArrayOption**

| Parameter Name          | Location                     | Type   | Description                                            |
|-------------------------|------------------------------|--------|--------------------------------------------------------|
| name                    | Path                         | string | The name of the workbook file.                         |
| importJsonRequest       | HTTP body                    | class  | The request payload that contains JSON import details. |
| password                | Query string                 | string | Password for opening the workbook (if protected).     |
| folder                  | Query string                 | string | The folder that contains the original workbook.        |
| storageName             | Query string                 | string | The name of the storage where the workbook resides.    |
| outPath                 | Query string                 | string | Path for the output file after import.                 |
| outStorageName          | Query string                 | string | Storage name for the output file.                      |
| checkExcelRestriction  | Query string                 | string | Flag to check Excel‑specific restrictions (true/false).|

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