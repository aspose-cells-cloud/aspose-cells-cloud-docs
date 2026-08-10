---
title: "Convert table to pivot table"
second_title: "Document"
linktitle: Convert
type: docs
url: /pivot-tables/convert-table-to-pivottable/
aliases:
  [
    /create-a-pivottable-with-table/,
    /create-new-pivot-table-with-list-object-as-source-data/,
  ]
keywords: "pivot table, list object, Aspose.Cells Cloud, REST API, convert table to pivot table"
description: "Learn how to create a pivot table from a list object using Aspose.Cells Cloud REST API. Includes request details, cURL example, and SDK references."
weight: 60
ArticleTitle: "Convert Table to Pivot Table – Aspose.Cells Cloud Documentation"
---

This REST API creates a **pivot table** from a list object.

A pivot table summarizes data from a list object, allowing you to analyze and report on large data sets directly within the workbook.

**Prerequisites:**  
- A valid JWT bearer token for authentication.  
- The workbook must exist in the specified storage location.  
- The target worksheet must contain the list object you want to summarize.

## PostWorksheetListObjectSummarizeWithPivotTable API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/SummarizeWithPivotTable
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### **Request parameters**

| Parameter Name  | Type    | Location | Description                                |
| --------------- | ------- | -------- | ------------------------------------------ |
| name            | string  | path     | Workbook file name.                        |
| sheetName       | string  | path     | Worksheet that contains the list object.   |
| listObjectIndex | integer | path     | Index of the list object in the worksheet. |
| destsheetName   | string  | query    | Name of the destination worksheet.         |
| request         | object  | body     | JSON payload that defines the pivot table. |
| folder          | string  | query    | Folder path where the workbook resides.    |
| storageName     | string  | query    | Name of the storage.                       |

The request body must follow the JSON schema defined below:

```json
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "type": "object",
  "properties": {
    "Name": { "type": "string", "description": "Name of the new pivot table." },
    "DestCellName": { "type": "string", "description": "Top‑left cell of the pivot table (e.g., \"C1\")." },
    "PivotFieldRows": {
      "type": "array",
      "items": { "type": "integer" },
      "description": "Zero‑based indices of fields to place in rows."
    },
    "PivotFieldColumns": {
      "type": "array",
      "items": { "type": "integer" },
      "description": "Zero‑based indices of fields to place in columns."
    },
    "PivotFieldData": {
      "type": "array",
      "items": { "type": "integer" },
      "description": "Zero‑based indices of fields to use as data fields."
    }
  },
  "required": ["Name", "DestCellName", "PivotFieldRows", "PivotFieldColumns", "PivotFieldData"]
}
```

The <a href="https://apireference.aspose.cloud/cells/#/ListObjects/PostWorksheetListObjectSummarizeWithPivotTable" rel="noopener noreferrer">OpenAPI Specification</a> defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the **cURL** command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/TestCase.xlsx/worksheets/Sheet2/listobjects/0/SummarizeWithPivotTable?folder=CellsTests&destsheetName=Sheet4" \
-X POST \
-d '{"Name":"TestPivot","DestCellName":"C1","PivotFieldRows":[0,1],"PivotFieldColumns":[2],"PivotFieldData":[3,4]}' \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

*Note: Use the production endpoint (`api.aspose.cloud`) for live environments. The QA endpoint (`api-qa.aspose.cloud`) is intended for testing only. HTTPS is required for all production calls.*

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

**HTTP Status Codes**

| Code | Meaning                     | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filter applied successfully; response contains operation details. |
| 400  | Bad Request                 | Missing or invalid parameters (e.g., unsupported file type). |
| 401  | Unauthorized                | Invalid or missing JWT token. |
| 413  | Payload Too Large           | Uploaded file exceeds size limit. |
| 500  | Internal Server Error       | Unexpected server error. |
## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK handles low‑level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs: