---
title: "Delete All Charts from a Worksheet"
type: docs
url: /charts/clear/
aliases: [/delete-all-charts-from-a-worksheet/]
weight: 30
keywords: "Aspose.Cells, Cloud, delete, all charts, worksheet, REST API, DELETE, SDK"
description: "Delete all charts from a worksheet via Aspose.Cells Cloud REST API v3.0: DELETE endpoint, auth, cURL, and SDK examples."
ArticleTitle: "Delete All Charts from a Worksheet using Aspose.Cells Cloud API"
linktitle: "Clear All Charts"
---
The **DeleteWorksheetCharts** API (`DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts`) is a REST endpoint provided by Aspose.Cells Cloud that removes all charts from a specified worksheet within a spreadsheet file, enabling developers to programmatically clean or reset chart content without manual intervention; it requires the file name and worksheet name as path parameters, with optional query parameters for folder and storage name to support flexible cloud-based file management.

**Background** – Removing all charts from a worksheet is useful when you need to reset a sheet’s visual layout, replace outdated visualizations, or prepare a workbook for reuse without retaining previous chart data.

## The Delete Worksheet Charts Web API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts
```

### Security and Authentication

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| name | String | Path | The file name. |
| sheetName | String | Path | The worksheet name. |
| folder | String | Query | The folder where the file is situated. |
| storageName | String | Query | The storage name where the file is situated. |

**Request Headers**

| Header        | Description                     |
|---------------|---------------------------------|
| Authorization | Bearer `<jwt token>`            |
| Accept        | `application/json`              |
| Content-Type  | `application/json` (no body)   |

**Request Body**

The DELETE operation does **not** require a request body.

**Response**

```json
{
    "Status":"OK",
    "Code":200
}
```


*Example error responses*

```json
// 400 Bad Request
{
    "Code": 400,
    "Message": "Invalid parameter: 'sheetName' is required."
}

// 401 Unauthorized
{
    "Code": 401,
    "Message": "Authentication failed. Invalid JWT token."
}

// 413 Payload Too Large
{
    "Code": 413,
    "Message": "The request payload exceeds the maximum allowed size."
}

// 500 Internal Server Error
{
    "Code": 500,
    "Message": "An unexpected error occurred on the server."
}
```

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

| Code | Meaning | Description |
|---|---|---|
| 200 | OK | The request completed successfully. |
| 400 | Bad Request | The request is malformed or one or more parameters are invalid. |
| 401 | Unauthorized | Authentication failed, or the JWT token is missing or expired. |
| 404 | Not Found | The requested workbook, worksheet, or resource was not found. |
| 500 | Internal Server Error | The server encountered an unexpected error while processing the request. |

## How to Use the Delete Worksheet Charts API with SDKs?

### Delete Worksheet Charts API Specification

The <a href="https://reference.aspose.cloud/cells/#/Charts/DeleteWorksheetCharts" rel="noopener noreferrer">Delete Worksheet Charts API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/charts" \
-X DELETE \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetCharts.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetCharts.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetCharts.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetCharts.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetCharts.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetCharts.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetCharts.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetCharts.go" >}}
{{</tab>}}
{{< /tabs >}}
