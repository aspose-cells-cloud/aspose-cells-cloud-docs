---
title: "Get Chart Area from a Worksheet"
type: docs
url: /charts/area/get/
aliases: [/get-chart-area-from-a-worksheet/]
weight: 60
keywords:
  - "Aspose.Cells"
  - "REST API"
  - "ChartArea"
  - "Worksheet"
  - "cURL"
  - "SDK"
  - "GetChartArea"
description: "Learn how to retrieve chart‑area information from a worksheet using the Aspose.Cells Cloud REST API, with examples for cURL and multiple SDKs."
ArticleTitle: "Get Chart Area from a Worksheet - Aspose.Cells Cloud API"
---

This REST API returns chart‑area information.

**Prerequisites:** To call this endpoint you must have a valid JWT access token, the target workbook must be uploaded to Aspose Cloud storage, and the file format must be supported by Aspose.Cells.

**Background:** A chart area defines the outermost bounding box of an Excel chart, including titles, legends, and the plot area. Retrieving its properties allows you to adjust layout and styling programmatically.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/chartArea
```

### Security and Authentication

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" target="_blank" rel="noopener noreferrer">JWT token‑based authentication</a>.

### Request parameters

| Parameter Name | Type    | Location | Description                                    |
| -------------- | ------- | -------- | ---------------------------------------------- |
| name           | string  | path     | Name of the workbook file.                     |
| sheetName      | string  | path     | Name of the worksheet that contains the chart. |
| chartIndex     | integer | path     | Zero‑based index of the chart.                 |
| folder         | string  | query    | Folder where the workbook is stored.           |
| storageName    | string  | query    | Name of the storage service.                   |

### **Response**

```json
{
  "ChartArea": {
    "Area": {
      "BackgroundColor": { "A": "0", "R": "0", "G": "0", "B": "0" },
      "FillFormat": { "Type": "Automatic" },
      "ForegroundColor": { "A": "0", "R": "0", "G": "0", "B": "0" },
      "Formatting": "Automatic",
      "InvertIfNegative": false,
      "Transparency": 0.0
    },
    "AutoScaleFont": false,
    "BackgroundMode": "Automatic",
    "Border": {
      "BeginArrowLength": "Medium",
      "BeginArrowWidth": "Medium",
      "BeginType": "None",
      "CapType": "Flat",
      "Color": { "A": "0", "R": "0", "G": "0", "B": "0" },
      "CompoundType": "Single",
      "DashType": "Solid",
      "EndArrowLength": "Medium",
      "EndArrowWidth": "Medium",
      "EndType": "None",
      "IsAuto": false,
      "IsAutomaticColor": false,
      "IsVisible": false,
      "JoinType": "Round",
      "Style": "Solid",
      "Transparency": 0.0,
      "Weight": "HairLine",
      "WeightPt": 0.0
    },
    "Font": {
      "Color": { "A": "255", "R": "0", "G": "0", "B": "0" },
      "DoubleSize": 10.0,
      "IsBold": false,
      "IsItalic": false,
      "IsStrikeout": false,
      "IsSubscript": false,
      "IsSuperscript": false,
      "Name": "Arial",
      "Size": 10,
      "Underline": "None"
    },
    "IsAutomaticSize": false,
    "IsInnerMode": false,
    "Shadow": false,
    "Width": 0,
    "Height": 0,
    "X": 0,
    "Y": 0,
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/chartArea",
      "Rel": "self"
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

**Response Status Codes**

| Code | Meaning                     | Description                                                                 |
|------|-----------------------------|-----------------------------------------------------------------------------|
| 200  | OK                          | Successful retrieval of chart‑area details; response contains the ChartArea object. |
| 400  | Bad Request                 | Missing or invalid parameters (e.g., unsupported file type).               |
| 401  | Unauthorized                | Invalid or missing JWT token.                                               |
| 413  | Payload Too Large           | Uploaded file exceeds size limit.                                           |
| 500  | Internal Server Error       | Unexpected server error.                                                    |

## How to Use the GetChartArea API with SDKs

### GetChartArea API Specification

The <a href="https://apireference.aspose.cloud/cells/#/ChartArea/GetChartArea" target="_blank" rel="noopener noreferrer">OpenAPI Specification</a> defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make a call to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/chartArea" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "ChartArea": {
    "Area": {
      "BackgroundColor": { "A": "0", "R": "0", "G": "0", "B": "0" },
      "FillFormat": { "Type": "Automatic" },
      "ForegroundColor": { "A": "0", "R": "0", "G": "0", "B": "0" },
      "Formatting": "Automatic",
      "InvertIfNegative": false,
      "Transparency": 0.0
    },
    "AutoScaleFont": false,
    "BackgroundMode": "Automatic",
    "Border": {
      "BeginArrowLength": "Medium",
      "BeginArrowWidth": "Medium",
      "BeginType": "None",
      "CapType": "Flat",
      "Color": { "A": "0", "R": "0", "G": "0", "B": "0" },
      "CompoundType": "Single",
      "DashType": "Solid",
      "EndArrowLength": "Medium",
      "EndArrowWidth": "Medium",
      "EndType": "None",
      "IsAuto": false,
      "IsAutomaticColor": false,
      "IsVisible": false,
      "JoinType": "Round",
      "Style": "Solid",
      "Transparency": 0.0,
      "Weight": "HairLine",
      "WeightPt": 0.0
    },
    "Font": {
      "Color": { "A": "255", "R": "0", "G": "0", "B": "0" },
      "DoubleSize": 10.0,
      "IsBold": false,
      "IsItalic": false,
      "IsStrikeout": false,
      "IsSubscript": false,
      "IsSuperscript": false,
      "Name": "Arial",
      "Size": 10,
      "Underline": "None"
    },
    "IsAutomaticSize": false,
    "IsInnerMode": false,
    "Shadow": false,
    "Width": 0,
    "Height": 0,
    "X": 0,
    "Y": 0,
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/chartArea",
      "Rel": "self"
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Use Aspose.Cells Cloud SDKs

Using an SDK is the best way to speed up development. An SDK handles low‑level details and lets you focus on your project tasks. Please check out the <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-GetChartArea-1.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-GetChartArea-get-chart-area.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-GetChartArea-.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-get_chart_area_info-.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetChartAreaFromWorksheet.py" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-GetChartArea-1.js" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-GetChartArea-get-chart-area.java" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-GetChartArea-1.pl" >}}
{{< /tab >}}

{{< tab tabNum="10" >}}
{{< gist "aspose-cells-cloud-gists" "e00e3bbfdf94f400244f1974c3488036" >}}
{{< /tab >}}

{{< /tabs >}}

**Generic HTTP request (e.g., using fetch):**

```javascript
fetch('https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/chartArea', {
  method: 'GET',
  headers: {
    'Content-Type': 'application/json',
    'Accept': 'application/json',
    'Authorization': 'Bearer <jwt token>'
  }
})
  .then(response => response.json())
  .then(data => console.log(data));
```