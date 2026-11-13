---
title: "Get Chart Title from a Worksheet"
type: docs
url: /charts/title/get/
aliases: [/get-chart-title-from-a-worksheet/]
weight: 120
keywords:
  - "Aspose.Cells Cloud"
  - "Chart Title"
  - "Excel"
  - "REST API"
  - "Get Chart Title"
  - "cURL"
  - "SDK"
  - "Excel chart automation"
  - "GET chart title"
description: "Retrieve a chart title from an Excel worksheet using Aspose.Cells Cloud REST API with cURL or SDKs."
ArticleTitle: "Get Chart Title from a Worksheet"
linktitle: "Get Chart Title"
---
The **GetWorksheetChartTitle** API (`GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/title`) retrieves the title description of a specific chart stored in a worksheet of an Excel workbook via Aspose.Cells Cloud, requiring the file name, worksheet name, and chart index as path parameters, and optionally supporting folder and storage name query parameters to locate the source file.

## The Get Worksheet Chart Title Web API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/title
```

### Security and Authentication

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| name | String | Path | The file name. |
| sheetName | String | Path | The worksheet name. |
| chartIndex | Integer | Path | The chart index. |
| folder | String | Query | The folder where the file is situated. |
| storageName | String | Query | The storage name where the file is situated. |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Charts/GetWorksheetChartTitle) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the **cURL** command‑line tool to access Aspose.Cells web services easily. The following example shows how to make a call to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/charts/0/title" \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Title": {
    "Text": "Sales Q1",
    "Font": {
      "Name": "Arial",
      "Size": 12,
      "IsBold": true
    }
  }
}
```

{{< /tab >}}

{{< /tabs >}}

**Response fields**

| Field               | Description                                     |
| ------------------- | ----------------------------------------------- |
| `Title.Text`        | The actual text displayed as the chart title.   |
| `Title.Font.Name`   | Font family used for the title (e.g., _Arial_). |
| `Title.Font.Size`   | Font size in points.                            |
| `Title.Font.IsBold` | Indicates whether the title text is bold.       |

**Response status codes**


**Notes**: The chart index is zero‑based; ensure the chart exists. If the workbook has not been uploaded, upload it first using the appropriate API.

**How to extract the title in a script (using `jq`)**

```bash
# Assuming the JSON response is saved in response.json
title=$(jq -r '.Title.Text' response.json)
echo "Chart title: $title"
```

### Response

```json
[
  {
    "Name": "TitleResponse",
    "DataType": {
      "Identifier": "Class",
      "Reference": "TitleResponse"
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

## How to Use the Get Worksheet Chart Title API with SDKs?

### Get Worksheet Chart Title API Specification

The <a href="https://reference.aspose.cloud/cells/#/Charts/GetWorksheetChartTitle" rel="noopener noreferrer">Get Worksheet Chart Title API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

You can also refer to the individual SDK documentation for more advanced scenarios, such as updating or deleting a chart title.  

**See also**: [Update Chart Title](/charts/title/put/), [Delete Chart Title](/charts/title/delete/).

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetChartTitle.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetChartTitle.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetChartTitle.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetChartTitle.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetChartTitle.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetChartTitle.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetChartTitle.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetChartTitle.go" >}}
{{</tab>}}
{{< /tabs >}}
