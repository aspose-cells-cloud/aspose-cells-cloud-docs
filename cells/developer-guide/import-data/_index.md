---
title: "Import Data"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /import-data/
aliases: [/import-data-into-excel-worksheet/, /import-data-into-worksheet/ , /import-data-in-excel-worksheet/]
description: "Cells.Cloud API for Excel operate: Import Data into Excel Worksheet."
weight: 100
---

This REST API indicates `import data` into Excel file.
 
## RSET API
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/importdata
 
```
The request parameters are: 
 
| Parameter Name | Type | Path/Query String/HTTPBody | Description| 
| :- | :- | :- |:- | 
| name | string | path |   |
| folder | string | query |   |
| storageName | string | query | storage name. |
| importData |  | body |   |
 
The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.
 
You can use cURL command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL.
 
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
 
```bash
{
"Code": 200,
"Status": "OK"
}
 
```
 
{{< /tab >}}
 
{{< /tabs >}}
 
 
The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

- [Import Batch Data into Excel Worksheet](/cells/import-batch-data-into-worksheet/)
- [Import Double Array into Excel Worksheet](/cells/import-double-array-into-worksheet/)
- [Import Integer Array into Excel Worksheet](/cells/import-integer-array-into-worksheet/)
- [Import String Array into Excel Worksheet](/cells/import-string-array-into-worksheet/)
- [Import CSV Data into Excel Worksheet](/cells/import-csv-data-into-worksheet/)
- [Import 2 Dimension Double Array into Excel Worksheet](/cells/import-2dimension-double-array-into-worksheet/)
- [Import 2 Dimension Integer Array into Excel Worksheet](/cells/import-2dimension-integer-array-into-worksheet/)
- [Import 2 Dimension String Array into Excel Worksheet](/cells/import-2dimension-string-array-into-worksheet/)