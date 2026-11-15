---
title: "Get Chart Second Category Axis"
type: docs
url: /charts/second-category-axis/get/
weight: 60
keywords: "Get Chart Second Category Axis, Aspose.Cells Cloud API, Excel chart axis, REST API, second-category axis, Aspose.Cells"
description: "Get the second-category axis of an Excel chart via Aspose.Cells Cloud REST API's GetChartSecondCategoryAxis endpoint"
ArticleTitle: "Get Chart Second Category Axis – Aspose.Cells Cloud API"
linktitle: "Get Second Category Axis"
---

The **GetChartSecondCategoryAxis** API (`GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondcategoryaxis`) retrieves the second category axis of a chart in a spreadsheet via Aspose.Cells Cloud, enabling developers to programmatically access axis properties—such as scale, formatting, and title—without modifying the source file, supporting tasks like dynamic chart analysis and reporting across .NET, Java, Python, and other supported SDKs.

## The Get Chart Second Category Axis Web API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondcategoryaxis
```

### Security and Authentication

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type    | Path/Query String/HTTPBody | Description                                  |
| -------------- | ------- | -------------------------- | -------------------------------------------- |
| name           | String  | Path                       | The file name.                               |
| sheetName      | String  | Path                       | The worksheet name.                          |
| chartIndex     | Integer | Path                       | The chart index.                             |
| folder         | String  | Query                      | The folder where the file is situated.       |
| storageName    | String  | Query                      | The storage name where the file is situated. |

### Response

```json
[
  {
    "Name": "AxisResponse",
    "DataType": {
      "Identifier": "Class",
      "Reference": "AxisResponse"
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

## How to Use the Get Chart Second Category Axis API with SDKs?

### Get Chart Second Category Axis API Specification

The <a href="https://reference.aspose.cloud/cells/#/Charts/GetChartSecondCategoryAxis" rel="noopener noreferrer">Get Chart Second Category Axis API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

You can use the `cURL` command‑line tool to access Aspose.Cells web services easily. The following example shows how to call the API with `cURL`.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondcategoryaxis?folder={folder}&storageName={storageName}" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Axis": {
    "Name": "Second Category Axis",
    "IsVisible": true,
    "AxisLine": { "Style": "Solid", "Weight": 1 },
    "TickMarks": "Inside",
    "Label": {
      "Font": { "Size": 10, "Color": "#000000" },
      "Format": "General"
    }
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="1" tabID="1" tabName1="Node.js" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Get-ChartSecondCategoryAxis.js" >}}
{{</tab>}}
{{< /tabs >}}
