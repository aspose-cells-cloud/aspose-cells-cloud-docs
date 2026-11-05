---
title: "Convert table to pivot table"
second_title: "Developer Guide"
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
The **PostWorksheetListObjectSummarizeWithPivotTable** API (`POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/SummarizeWithPivotTable`) enables developers to programmatically convert an existing list object in a worksheet into a pivot table using Aspose.Cells Cloud, requiring parameters such as the workbook name, worksheet name, list object index, destination worksheet name, and a `CreatePivotTableRequest` body to define the pivot table structure and data fields.

A pivot table summarizes data from a list object, allowing you to analyze and report on large data sets directly within the workbook.

## The Post Worksheet List Object Summarize with Pivot Table Web API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/SummarizeWithPivotTable
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### **Request parameters**

| Parameter Name          | Type                          | Path/Query String/HTTPBody | Description                                  |
| ----------------------- | ----------------------------- | -------------------------- | -------------------------------------------- |
| name                    | String                        | Path                       | The file name.                               |
| sheetName               | String                        | Path                       | The worksheet name.                          |
| listObjectIndex         | Integer                       | Path                       | The list object index.                       |
| destsheetName           | String                        | Query                      | The target worksheet name.                   |
| createPivotTableRequest | class:createpivottablerequest | HTTPBody                   | Create pivot table request.                  |
| folder                  | String                        | Query                      | The folder where the file is situated.       |
| storageName             | String                        | Query                      | The storage name where the file is situated. |

The request body must follow the JSON schema defined below:

```json
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "type": "object",
  "properties": {
    "Name": { "type": "string", "description": "Name of the new pivot table." },
    "DestCellName": {
      "type": "string",
      "description": "Top‑left cell of the pivot table (e.g., \"C1\")."
    },
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
  "required": [
    "Name",
    "DestCellName",
    "PivotFieldRows",
    "PivotFieldColumns",
    "PivotFieldData"
  ]
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

_Note: Use the production endpoint (`api.aspose.cloud`) for live environments. The QA endpoint (`api-qa.aspose.cloud`) is intended for testing only. HTTPS is required for all production calls._

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

### **Response**

```json
[
  {
    "Name": "CellsCloudResponse",
    "DataType": {
      "Identifier": "Class",
      "Reference": "CellsCloudResponse"
    }
  }
]
```

**Sample response headers**

```http
HTTP/1.1 200 OK
Content-Type: application/json
```

**HTTP Status Codes**

| Code | Meaning               | Description                                                              |
| ---- | --------------------- | ------------------------------------------------------------------------ |
| 200  | OK                    | The request completed successfully.                                      |
| 400  | Bad Request           | The request is malformed or one or more parameters are invalid.          |
| 401  | Unauthorized          | Authentication failed, or the JWT token is missing or expired.           |
| 404  | Not Found             | The requested workbook, worksheet, or resource was not found.            |
| 413  | Payload Too Large     | The uploaded file exceeds the allowed size limit.                        |
| 500  | Internal Server Error | The server encountered an unexpected error while processing the request. |

## How to Use the Post Worksheet List Object Summarize with Pivot Table API with SDKs?

### Post Worksheet List Object Summarize with Pivot Table API Specification

The <a href="https://reference.aspose.cloud/cells/#/ListObjects/PostWorksheetListObjectSummarizeWithPivotTable" rel="noopener noreferrer">Post Worksheet List Object Summarize with Pivot Table API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObjectSummarizeWithPivotTable.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObjectSummarizeWithPivotTable.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObjectSummarizeWithPivotTable.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObjectSummarizeWithPivotTable.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObjectSummarizeWithPivotTable.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObjectSummarizeWithPivotTable.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObjectSummarizeWithPivotTable.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObjectSummarizeWithPivotTable.go" >}}
{{</tab>}}
{{< /tabs >}}
