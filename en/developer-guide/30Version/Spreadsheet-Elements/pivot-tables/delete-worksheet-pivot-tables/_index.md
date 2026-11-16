---
title: "Delete All Pivot Tables in Excel Using Aspose.Cells Cloud REST API"
second_title: "Aspose.Cells Cloud Document"
linktitle: Clear
type: docs
url: /pivot-tables/clear/
aliases: [/delete-worksheet-pivot-tables/]
description: "Learn how to delete all pivot tables from an Excel worksheet using the Aspose.Cells Cloud REST API. Includes cURL, C#, Java, Python, and Node.js examples with best practices and security guidance."
keywords:
  - "Aspose.Cells"
  - "pivot table"
  - "delete"
  - "REST API"
  - "Excel"
date: 2024-06-15
api_version: "v3.0"
weight: 100
ArticleTitle: "Delete All Pivot Tables in Excel Worksheet via Aspose.Cells Cloud REST API"
---

The **DeleteWorksheetPivotTables** API (`DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables`) removes all PivotTables from a specified worksheet in an Excel file using Aspose.Cells Cloud, enabling users to reset analysis layouts, clean up unused pivot tables, or prepare templates for reuse without deleting the worksheet itself; the operation requires the file name and worksheet name as path parameters and supports optional folder and storageName query parameters for cloud storage organization.

## Overview

This operation removes **all** pivot tables from a specified worksheet in an Excel file. It is especially useful for resetting analysis layouts, cleaning up unused pivot tables, or preparing templates for reuse—without deleting the worksheet itself.

## The Delete Worksheet Pivot Tables Web API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables
```

### Security and Authentication

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer" target="_blank">JWT token-based authentication</a>.

### Path Parameters

| Parameter Name | Type   | Path/Query String/HTTPBody | Description                                  |
| -------------- | ------ | -------------------------- | -------------------------------------------- |
| name           | String | Path                       | The file name.                               |
| sheetName      | String | Path                       | The worksheet name.                          |
| folder         | String | Query                      | The folder where the file is situated.       |
| storageName    | String | Query                      | The storage name where the file is situated. |

### Response

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
| 500  | Internal Server Error | The server encountered an unexpected error while processing the request. |

### Query Parameters

| Name          | Type   | Required | Description                                                             |
| ------------- | ------ | -------- | ----------------------------------------------------------------------- |
| `folder`      | string | No       | The folder that contains the file (e.g., `input/`).                     |
| `storageName` | string | No       | The storage name to use (if the file resides in a non-default storage). |

### Successful Response

The service returns a standard `CellsCloudResponse` object indicating the operation status.

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**HTTP Status Codes**

| Code | Meaning               | Description                                                              |
| ---- | --------------------- | ------------------------------------------------------------------------ |
| 200  | OK                    | The request completed successfully.                                      |
| 400  | Bad Request           | The request is malformed or one or more parameters are invalid.          |
| 401  | Unauthorized          | Authentication failed, or the JWT token is missing or expired.           |
| 404  | Not Found             | The requested workbook, worksheet, or resource was not found.            |
| 500  | Internal Server Error | The server encountered an unexpected error while processing the request. |

## How to Use the Delete Worksheet Pivot Tables API with SDKs?

### Delete Worksheet Pivot Tables API Specification

The <a href="https://reference.aspose.cloud/cells/#/PivotTables/DeleteWorksheetPivotTables" rel="noopener noreferrer">Delete Worksheet Pivot Tables API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

**cURL Example**

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables?folder=input&storageName=MyStorage" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your-jwt-token>"
```

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetPivotTables.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetPivotTables.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetPivotTables.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetPivotTables.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetPivotTables.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetPivotTables.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetPivotTables.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetPivotTables.go" >}}
{{</tab>}}
{{< /tabs >}}
