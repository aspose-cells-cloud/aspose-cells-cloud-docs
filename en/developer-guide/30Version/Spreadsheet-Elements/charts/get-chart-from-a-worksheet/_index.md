---
title: "Get Chart from a Worksheet"
type: docs
url: /charts/get/
aliases: [/get-chart-from-a-worksheet/]
weight: 10
keywords: "Aspose.Cells Cloud, Get Chart, Worksheet, REST API, Excel, Chart API, chart retrieval, Excel chart"
description: "Retrieve chart information, including metadata and export format, from a worksheet using the Aspose.Cells Cloud REST API."
ArticleTitle: "Get Chart from a Worksheet – Aspose.Cells Cloud API"
---

## REST API

This REST API retrieves chart information.

**Prerequisites** – To call this endpoint you must have a valid Aspose.Cells Cloud account, an active storage location, and a JWT access token. Obtain the token following the instructions in the authentication guide before making any API requests.

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartNumber}
```


### Security and Authentication

The Aspose.Cells Cloud APIs are secure and require [JWT token-based authentication](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/). See the “How to obtain a JWT token” section in the authentication guide for details on generating a token.

### Request parameters

| Parameter Name | Type    | Location | Description                                 |
| -------------- | ------- | -------- | ------------------------------------------- |
| name           | string  | path     | Name of the Excel file.                     |
| sheetName      | string  | path     | Name of the worksheet containing the chart. |
| chartNumber    | integer | path     | Zero‑based index of the chart to retrieve.  |
| format         | string  | query    | Desired export format (e.g., png, jpeg).    |
| folder         | string  | query    | Folder path where the document is stored.   |
| storageName    | string  | query    | Name of the storage service.                |


### **Response**

```json
{
  "Code": 200,
  "Status": "OK",
  "Chart": {
    "Name": "Chart 1",
    "Type": "Bar",
    "Top": 50,
    "Left": 100,
    "Width": 400,
    "Height": 300,
    "DataRange": "A1:B5",
    "ShowLegend": true,
    "Format": "png"
  }
}
```

**Response Status Codes**

| Code | Meaning                     | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Request succeeded; response contains chart details, including metadata and optional image format. |
| 400  | Bad Request                 | Missing or invalid parameters (e.g., unsupported file type). |
| 401  | Unauthorized                | Invalid or missing JWT token. |
| 413  | Payload Too Large           | Uploaded file exceeds size limit. |
| 500  | Internal Server Error       | Unexpected server error. |


## How to Use the GetWorksheetChart API with SDKs

### GetWorksheetChart API Specification


The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Charts/GetWorksheetChart) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Chart": {
    "Name": "Chart 1",
    "Type": "Bar",
    "Top": 50,
    "Left": 100,
    "Width": 400,
    "Height": 300,
    "DataRange": "A1:B5",
    "ShowLegend": true,
    "Format": "png"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Use Aspose.Cells Cloud SDKs

Using an SDK is the best way to speed up development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-GetChart-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-GetChart-get-chart-from-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-GetWorksheetChart-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-get_worksheet_charts_info-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetChartAreaFromWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-GetChart-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-GetChart-get-chart-from-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-GetChart-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "6fbcaeac3bd9fe1d22319418799757bd" >}}

{{< /tab >}}

{{< /tabs >}}