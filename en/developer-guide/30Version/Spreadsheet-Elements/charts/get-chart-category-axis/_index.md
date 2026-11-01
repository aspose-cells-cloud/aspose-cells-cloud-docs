---
title: "Get Chart Category Axis"
type: docs
url: /charts/category-axis/get/
weight: 60
keywords: "Aspose.Cells, Chart Category Axis, Excel, REST API, Cloud Storage, OAuth2, API Documentation"
description: "Retrieves the category axis of a chart in an Excel worksheet using the Aspose.Cells Cloud REST API."
ArticleTitle: "Get Chart Category Axis – Aspose.Cells Cloud API Documentation"
linktitle: "Get Chart Category Axis"
---

The **GetChartCategoryAxis** API (`GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/categoryaxis`) retrieves the category axis description of a specific chart in a worksheet using Aspose.Cells Cloud, requiring the workbook filename, worksheet name, and chart index as path parameters; it supports optional `folder` and `storageName` query parameters to locate the file in Aspose Cloud storage and returns a structured `AxisResponse` containing axis metadata.

**Prerequisites**  
Before using this endpoint, ensure that:  

- An OAuth 2.0 token has been obtained and is valid for the Aspose Cloud services.  
- The workbook file is uploaded to Aspose Cloud storage (default or a specified folder).  
- You are using API version **v3.0** as shown in the request URL.  
- The calling application has permission to read the workbook and access its worksheets.

## GetChartCategoryAxis API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/categoryaxis
```

**Background** – Removing all charts from a worksheet is useful when you need to reset a sheet’s visual layout, replace outdated visualizations, or prepare a workbook for reuse without retaining previous chart data.

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request parameters

| Parameter Name | Type    | Location | Description                                            |
| -------------- | ------- | -------- | ------------------------------------------------------ |
| name           | string  | path     | The name of the workbook file.                         |
| sheetName      | string  | path     | The name of the worksheet containing the chart.        |
| chartIndex     | integer | path     | Zero‑based index of the chart whose axis is requested. |
| folder         | string  | query    | The folder path in storage where the workbook resides. |
| storageName    | string  | query    | The name of the storage service (if not the default).  |

### **Response**

```json
{
  "Code": 200,
  "Status": "OK",
  "CategoryAxis": {
    "AxisBetweenCategories": true,
    "AxisLine": {
      "IsVisible": true,
      "Weight": 1.0
    },
    "MajorTickMark": "Cross",
    "MinorTickMark": "None",
    "Title": {
      "Text": "Category Axis",
      "IsVisible": true
    },
    "Labels": {
      "IsAutoRotation": false,
      "RotationAngle": 0,
      "IsVisible": true
    }
  }
}
```

**HTTP Status Codes**

| Code | Meaning                     | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filter applied successfully; response contains operation details. |
| 400  | Bad Request                 | Missing or invalid parameters (e.g., unsupported file type). |
| 401  | Unauthorized                | Invalid or missing JWT token. |
| 413  | Payload Too Large           | Uploaded file exceeds size limit. |
| 500  | Internal Server Error       | Unexpected server error. |
## How to Use the GetChartCategoryAxis API with SDKs

### GetChartCategoryAxis API Specification


The <a href="https://apireference.aspose.cloud/cells/#/Charts/GetChartCategoryAxis" rel="noopener noreferrer">OpenAPI Specification</a> defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make a call to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/categoryaxis" \
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
  "CategoryAxis": {
    "AxisBetweenCategories": true,
    "AxisLine": {
      "IsVisible": true,
      "Weight": 1.0
    },
    "MajorTickMark": "Cross",
    "MinorTickMark": "None",
    "Title": {
      "Text": "Category Axis",
      "IsVisible": true
    },
    "Labels": {
      "IsAutoRotation": false,
      "RotationAngle": 0,
      "IsVisible": true
    }
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Use Aspose.Cells Cloud SDKs

Using an SDK is the best way to speed up development. An SDK handles low‑level details and lets you focus on your project tasks. Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

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
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Get-ChartCategoryAxis.js" >}}
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