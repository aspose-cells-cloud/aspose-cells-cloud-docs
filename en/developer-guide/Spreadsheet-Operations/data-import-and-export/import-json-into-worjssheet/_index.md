---
title: "Import Json data into Excel"
second_title: "Aspose.Cells Cloud Document"
linktitle: "Import Json"
type: docs
url: /import-json-data-into-excel/
aliases: [ /import/json/]
keywords: "Import Json data into Excel."
description: "Aspose.Cells Cloud REST API support importing string array data into Excel files. SDK support kinds of development languages. They include Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby, and swift."
weight: 40
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdown, Import Json data into Excel
---

This REST API `import json data` into Excel work sheet.

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/{name}/importjson

```

The important parameters are described in the following table:

**ImportStringArrayOption**

| Parameter Name| Path/Query String/HTTPBody |Type|Description|
| :- | :- | :- |
| name | Path | string | The workbook name |
| importJsonRequest  | HTTPBody | class |  Import json request. |
| password | Query String | string |  The password of workbook. |
| folder | Query String |  string | Original workbook folder. |
| storageName | Query String | string | Storage name. |
| outPath | Query String | string | Output file path. |
| outStorageName | Query String | string | Storage name for output file. |
| checkExcelRestriction | Query String | string | Check Excel restriction. |

**Example**

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

Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:
