---
title: "Get All Pivot Tables in an Excel Worksheet"
second_title: "Developer Guide"
linktitle: Get all
type: docs
url: /pivot-tables/get-all/
aliases: [/get-worksheet-pivot-tables-information/]
keywords: "get all pivot tables, Aspose.Cells Cloud API, Excel PivotTable, REST API"
description: "Get all PivotTables from an Excel worksheet via Aspose.Cells Cloud REST API with cURL and SDK examples"
weight: 100
ArticleTitle: "Get All Pivot Tables in an Excel Worksheet – Aspose.Cells Cloud API"
---
The **GetWorksheetPivotTables** API (`GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables`) retrieves descriptions of all PivotTables in a specified worksheet using Aspose.Cells Cloud, enabling developers to programmatically inspect PivotTable structure and metadata without local Excel installation.

## The Get Worksheet Pivot Tables Web API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer" target="_blank">JWT token-based authentication</a>.

### **Request parameters**

| Parameter Name | Type   | Path/Query String/HTTPBody | Description                                  |
| -------------- | ------ | -------------------------- | -------------------------------------------- |
| name           | String | Path                       | The file name.                               |
| sheetName      | String | Path                       | The worksheet name.                          |
| folder         | String | Query                      | The folder where the file is situated.       |
| storageName    | String | Query                      | The storage name where the file is situated. |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/PivotTables/GetWorksheetPivotTables) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

### Response

```json
[
  {
    "Name": "PivotTablesResponse",
    "DataType": {
      "Identifier": "Class",
      "Reference": "PivotTablesResponse"
    }
  }
]
```

**Sample response headers**

```http
HTTP/1.1 200 OK
Content-Type: application/json
```

### Error Responses

| HTTP Code | Description                                                     | Sample JSON Payload                                           |
| --------- | --------------------------------------------------------------- | ------------------------------------------------------------- |
| 400       | Bad request – required parameter missing.                       | `{ "Code": "400", "Message": "Missing required parameter." }` |
| 401       | Unauthorized – invalid or missing token.                        | `{ "Code": "401", "Message": "Authentication failed." }`      |
| 404       | Not found – workbook, worksheet, or pivot table does not exist. | `{ "Code": "404", "Message": "Resource not found." }`         |
| 500       | Internal server error – unexpected condition on the server.     | `{ "Code": "500", "Message": "Server error." }`               |

### Request

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

## How to Use the Get Worksheet Pivot Tables API with SDKs?

### Get Worksheet Pivot Tables API Specification

The <a href="https://reference.aspose.cloud/cells/#/PivotTables/GetWorksheetPivotTables" rel="noopener noreferrer">Get Worksheet Pivot Tables API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetPivotTables.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetPivotTables.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetPivotTables.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetPivotTables.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetPivotTables.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetPivotTables.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetPivotTables.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetPivotTables.go" >}}
{{</tab>}}
{{< /tabs >}}
