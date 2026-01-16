---
title: "Import Data with using storage"
second_title: "Document"
linktitle: "Import data with storage"
type: docs
url: /import-data-with-using-storage/
aliases:
  - /import-data-into-excel-worksheet/
  - /import-data-into-worksheet/
  - /import-data-in-excel-worksheet/
  - /import-data/
  - /import/with-using-storage/
description: "Use Aspose.Cells Cloud API to import data into an Excel worksheet from various storage sources."
keywords: "Excel, Aspose.Cells, REST API, Import Data, Cloud Storage, JSON, CSV, PDF, Markdown"
weight: 10
---

This REST API imports data into an Excel file.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/importdata
```

The request parameters are:

| Parameter Name | Type   | Location                     | Description                                                |
|----------------|--------|------------------------------|------------------------------------------------------------|
| name           | string | path                         | The name of the Excel file.                                |
| folder         | string | query                        | The folder path in the storage where the file resides.    |
| storageName    | string | query                        | The name of the storage service.                           |
| importData     | object | body                         | JSON object that contains the data to be imported.        |

**The import‑data options parameters** are described in [the reference link](/cells/import/#import-data-option-parameter).

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to call the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/Book1.xlsx/importdata" \
-X POST \
-D "{\"Data\":[1,2,4],\"DestinationWorksheet\":\"Sheet1\",\"FirstRow\":1,\"FirstColumn\":2,\"IsVertical\":true,\"IsInsert\":true,\"importDataType\":\"IntArray\"}" \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs: