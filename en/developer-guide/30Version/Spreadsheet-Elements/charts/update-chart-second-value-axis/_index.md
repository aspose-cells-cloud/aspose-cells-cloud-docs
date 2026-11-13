---
title: "Update Chart Second Value Axis"
ArticleTitle: "Update Chart Second Value Axis – Aspose.Cells Cloud REST API"
type: docs
url: /charts/second-value-axis/update/
weight: 160
keywords: "Aspose.Cells, Chart API, Second Value Axis, Excel, REST, Cloud SDK"
description: "Update Excel chart's second value axis via Aspose.Cells Cloud REST API using POST /charts/{chartIndex}/secondvalueaxis"
linktitle: "Update Second Value Axis"
---
The **PostChartSecondValueAxis** API (`POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondvalueaxis`) updates the second value axis of a chart in a spreadsheet via Aspose.Cells Cloud, allowing developers to programmatically modify axis properties such as scale, format, and title by sending an Axis object in the request body.

## The Post Chart Second Value Axis Web API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondvalueaxis
```

### Security and Authentication

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| name | String | Path | The file name. |
| sheetName | String | Path | The worksheet name. |
| chartIndex | Integer | Path | The chart index. |
| axis | class:axis | HTTPBody | Axis |
| folder | String | Query | The folder where the file is situated. |
| storageName | String | Query | The storage name where the file is situated. |

**Example request body (JSON):**

```json
{
  "IsAutomaticMajorUnit": true,
  "Maximum": 100,
  "Minimum": 0,
  "MajorUnit": 10,
  "MinorUnit": 2,
  "Title": {
    "Text": "Secondary Axis"
  }
}
```

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Charts/PostChartSecondValueAxis) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondvalueaxis" \
-X POST \
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


**See also:**

- [Get Chart Second Value Axis](https://docs.aspose.cloud/cells/charts/second-value-axis/get/)
- [Update Chart Value Axis](https://docs.aspose.cloud/cells/charts/value-axis/update/)

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
| 413 | Payload Too Large | The uploaded file exceeds the allowed size limit. |
| 500 | Internal Server Error | The server encountered an unexpected error while processing the request. |

## How to Use the Post Chart Second Value Axis API with SDKs?

### Post Chart Second Value Axis API Specification

The <a href="https://reference.aspose.cloud/cells/#/Charts/PostChartSecondValueAxis" rel="noopener noreferrer">Post Chart Second Value Axis API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="1" tabID="4" tabName1="Node.js" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Post-ChartSecondValueAxis.js" >}}
{{</tab>}}
{{< /tabs >}}
