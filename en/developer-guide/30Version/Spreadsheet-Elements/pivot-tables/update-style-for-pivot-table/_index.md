---
title: "Update style for pivot table"
second_title: "Developer Guide"
linktitle: "Format all"
type: docs
url: /pivot-tables/format-all/
aliases: [/update-style-for-pivot-table/]
keywords: "pivot table, update style, Aspose.Cells Cloud, REST API, Excel, spreadsheet, API, pivot table style, format all"
description: "Update pivot table style via Aspose.Cells Cloud REST API using PostPivotTableStyle endpoint with cURL and SDK examples."
weight: 100
ArticleTitle: "Update style for pivot table - Aspose.Cells Cloud API"
---
The **PostPivotTableStyle** API (`POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/FormatAll`) enables developers to update the style of a specific pivot table within a worksheet using Aspose.Cells Cloud, allowing programmatic application of formatting such as cell borders, fonts, and colors to all cells in the pivot table structure in a single request.

## The Post Pivot Table Style Web API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/FormatAll
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### **Request parameters**

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| name | String | Path | The file name. |
| sheetName | String | Path | The worksheet name. |
| pivotTableIndex | Integer | Path | The PivotTable index. |
| style | class:style | HTTPBody | StyleStyle description in request body. |
| needReCalculate | Boolean | Query | Whether the specific PivotTable calculate(true/false). |
| folder | String | Query | The folder where the file is situated. |
| storageName | String | Query | The storage name where the file is situated. |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/PivotTables/PostPivotTableStyle) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make a call to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0/FormatAll" \
  -X POST \
  -d '{"Font":{"Name":"Arial","Size":10}}' \
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

| Code | Meaning | Description |
|---|---|---|
| 200 | OK | The request completed successfully. |
| 400 | Bad Request | The request is malformed or one or more parameters are invalid. |
| 401 | Unauthorized | Authentication failed, or the JWT token is missing or expired. |
| 404 | Not Found | The requested workbook, worksheet, or resource was not found. |
| 413 | Payload Too Large | The uploaded file exceeds the allowed size limit. |
| 500 | Internal Server Error | The server encountered an unexpected error while processing the request. |

**Prerequisites / Authentication**  
A valid JWT access token must be supplied in the `Authorization` header (e.g., `Bearer <jwt token>`). Ensure the token has permission to access the specified workbook and worksheet.

## Cloud SDK Family

Using an SDK is the fastest way to develop against the API. The SDK abstracts low‑level details so you can focus on your business logic. See the <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code example demonstrates how to call the API using the Go SDK:

{{< tabs tabTotal="1" tabID="4" tabName1="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "0b2caae7acfa3e947b856c07b6e8633a" >}}

{{< /tab >}}

{{< /tabs >}}
