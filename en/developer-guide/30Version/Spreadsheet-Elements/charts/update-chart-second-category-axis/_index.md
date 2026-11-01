---
title: "Update Chart Second Category Axis"
type: docs
url: /charts/second-category-axis/update/
weight: 160
keywords: "Aspose.Cells, Chart, Second Category Axis, REST API, Update Chart, Excel, Cloud API"
description: "Learn how to update the second category axis of a chart in an Excel worksheet using the Aspose.Cells Cloud REST API."
ArticleTitle: "Update Chart Second Category Axis – Aspose.Cells Cloud API"
linktitle: "Update Second Category Axis"
---
The **PostChartSecondCategoryAxis** API (`POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondcategoryaxis`) updates the second category axis of a chart in Aspose.Cells Cloud, enabling precise control over axis formatting and scale by sending an axis configuration object in the request body.

## The Post Chart Second Category Axis Web API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondcategoryaxis
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| name | String | Path | The file name. |
| sheetName | String | Path | The worksheet name. |
| chartIndex | Integer | Path | The chart index. |
| axis | class:axis | HTTPBody | Axis |
| folder | String | Query | The folder where the file is situated. |
| storageName | String | Query | The storage name where the file is situated. |

**Authentication** – The API requires a valid OAuth 2.0 access token. Generate a JWT token by following the [Authentication Guide]（https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/）. Include the token in the `Authorization` header as shown in the cURL example below.

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Charts/PostChartSecondCategoryAxis) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondcategoryaxis?folder={folder}&storageName={storageName}" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "axis": {
          /* axis settings, e.g., "Title": "New Axis Title", "IsVisible": true */
        }
      }'
```

_Replace `{name}`, `{sheetName}`, `{chartIndex}`, `{folder}`, and `{storageName}` with your actual values. The request body must contain the `axis` object with the desired settings._

{{< /tab >}}

{{< tab tabNum="2" >}}

**Successful response (200)**

```json
{
  "Code": 200,
  "Status": "OK",
  "Chart": {
    "Id": "chart_1",
    "SecondCategoryAxis": {
      "Title": "New Axis Title",
      "IsVisible": true
      /* additional axis properties */
    }
  }
}
```

**Error responses**


```json
{
  "Code": 400,
  "Message": "Invalid request payload."
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

## Cloud SDK Family

SDKs simplify development by handling low‑level details and allowing you to focus on your business logic. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

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
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Post-ChartSecondCategoryAxis.js" >}}
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

**Notes & Best Practices**

- The `chartIndex` parameter is zero‑based; the first chart in a worksheet is index 0.
- The API supports both `.xlsx` and `.xls` workbook formats.
- Include only the properties you need in the `axis` object; unspecified properties retain their existing values.
- Respect rate‑limit guidelines (typically 100 requests per minute per account) to avoid throttling.
