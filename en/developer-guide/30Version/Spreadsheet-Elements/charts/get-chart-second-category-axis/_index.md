---
title: "Get Chart Second Category Axis"
type: docs
url: /charts/second-category-axis/get/
weight: 60
keywords: "Get Chart Second Category Axis, Aspose.Cells Cloud API, Excel chart axis, REST API, second-category axis, Aspose.Cells"
description: "Retrieve the second‑category axis of a chart in an Excel worksheet using the Aspose.Cells Cloud REST API. Includes request format, parameters, sample cURL, response schema, status codes, and usage notes."
ArticleTitle: "Get Chart Second Category Axis – Aspose.Cells Cloud API"
---

This REST API retrieves the **second‑category axis** of a chart.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondcategoryaxis
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.


### Request parameters

| Parameter Name | Type    | Parameter Location (path/query) | Description                                            |
| -------------- | ------- | ------------------------------- | ------------------------------------------------------ |
| name           | string  | path                            | Name of the Excel file stored in the cloud.            |
| sheetName      | string  | path                            | Name of the worksheet that contains the chart.         |
| chartIndex     | integer | path                            | Zero‑based index of the chart whose axis is requested. |
| folder         | string  | query                           | Folder path in the storage where the file is located.  |
| storageName    | string  | query                           | Name of the Aspose Cloud storage to use (optional).    |


### **Response**

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

**Response Status Codes**

| Code | Meaning                     | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Compression succeeded; response contains compressed file details. |
| 400  | Bad Request                 | Missing or invalid parameters (e.g., unsupported file type). |
| 401  | Unauthorized                | Invalid or missing JWT token. |
| 413  | Payload Too Large           | Uploaded file exceeds size limit. |
| 500  | Internal Server Error       | Unexpected server error. |


## How to Use the GetChartSecondCategoryAxis API with SDKs

### GetChartSecondCategoryAxis API Specification

The **Get‑Chart‑Second‑Category‑Axis** operation is defined in the [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Charts/GetChartSecondCategoryAxis) and enables direct REST interactions from a web browser or any HTTP client.

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

Using an SDK is the fastest way to integrate this API into your project. SDKs handle low‑level details such as authentication, request building, and response parsing, letting you focus on business logic. See the full list of Aspose.Cells Cloud SDKs in the [GitHub repository](https://github.com/aspose-cells-cloud).

The following code examples demonstrate how to call the **Get Chart Second Category Axis** operation with various SDKs:

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

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Get-ChartSecondCategoryAxis.js" >}}

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