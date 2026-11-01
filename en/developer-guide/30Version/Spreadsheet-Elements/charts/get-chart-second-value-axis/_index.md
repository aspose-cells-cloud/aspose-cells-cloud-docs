---
title: "Get Chart Second Value Axis"
type: docs
url: /charts/second-value-axis/get/
weight: 60
keywords: Aspose.Cells, chart second value axis, Excel, REST API, cloud, API, Excel chart axis
description: Retrieves the second value axis of a specified chart in an Excel worksheet using the Aspose.Cells Cloud REST API.
ArticleTitle: "Get Chart Second Value Axis – Aspose.Cells Cloud API"
linktitle: "Get Second Value Axis"
---
The **GetChartSecondValueAxis** API (`GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondvalueaxis`) retrieves the second value axis of a chart in Aspose.Cells Cloud, enabling developers to programmatically access axis properties such as scale, format, and title for advanced chart analysis and customization using standard REST conventions and supported SDKs for .NET, Java, Python, and other languages.

## The Get Chart Second Value Axis Web API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondvalueaxis
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| name | String | Path | The file name. |
| sheetName | String | Path | The worksheet name. |
| chartIndex | Integer | Path | The chart index. |
| folder | String | Query | The folder where the file is situated. |
| storageName | String | Query | The storage name where the file is situated. |

**Prerequisites**: A valid JWT access token obtained via the Aspose Cloud OAuth2 flow must be supplied in the `Authorization` header of each request.

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Charts/GetChartSecondValueAxis) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make a call to the Cloud API with cURL. All Aspose Cloud endpoints require HTTPS.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/" \
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
    "AxisId": 1,
    "IsVisible": true,
    "MinimumScale": 0,
    "MaximumScale": 100,
    "MajorUnit": 10,
    "MinorUnit": 5,
    "Title": "Second Value Axis"
  }
}
```

**Response fields**

- **Code** – HTTP status code of the operation (e.g., `200` for success).  
- **Status** – Textual description of the status (`"OK"` for success).  
- **Axis** – Object containing details of the second value axis:  
  - **AxisId** – Identifier of the axis.  
  - **IsVisible** – Boolean indicating whether the axis is displayed.  
  - **MinimumScale** – Minimum value displayed on the axis.  
  - **MaximumScale** – Maximum value displayed on the axis.  
  - **MajorUnit** – Interval between major tick marks.  
  - **MinorUnit** – Interval between minor tick marks.  
  - **Title** – Title text of the axis.

**Error responses** (non‑200)

- `400 Bad Request` – Invalid parameters or malformed request.  
- `401 Unauthorized` – Missing or invalid JWT token.  
- `404 Not Found` – Specified file, worksheet, or chart does not exist.  
- `500 Internal Server Error` – Unexpected server error.

{{< /tab >}}

{{< /tabs >}}

### **Response**

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

| Code | Meaning | Description |
|---|---|---|
| 200 | OK | The request completed successfully. |
| 400 | Bad Request | The request is malformed or one or more parameters are invalid. |
| 401 | Unauthorized | Authentication failed, or the JWT token is missing or expired. |
| 404 | Not Found | The requested workbook, worksheet, or resource was not found. |
| 500 | Internal Server Error | The server encountered an unexpected error while processing the request. |

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK takes care of low‑level details and lets you focus on your project tasks. Please check out the <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

<!-- C# example placeholder -->

{{< /tab >}}

{{< tab tabNum="2" >}}

<!-- Java example placeholder -->

{{< /tab >}}

{{< tab tabNum="3" >}}

<!-- PHP example placeholder -->

{{< /tab >}}

{{< tab tabNum="4" >}}

<!-- Ruby example placeholder -->

{{< /tab >}}

{{< tab tabNum="5" >}}

<!-- Python example placeholder -->

{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Get-ChartSecondValueAxis.js" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}

<!-- Android example placeholder -->

{{< /tab >}}

{{< tab tabNum="8" >}}

<!-- Swift example placeholder -->

{{< /tab >}}

{{< tab tabNum="9" >}}

<!-- Perl example placeholder -->

{{< /tab >}}

{{< tab tabNum="10" >}}

<!-- Go example placeholder -->

{{< /tab >}}

{{< /tabs >}}