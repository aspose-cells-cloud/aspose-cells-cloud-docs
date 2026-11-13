---
title: "Export Excel Chart – Aspose.Cells Cloud API"
subtitle: "Convert a chart from a cloud-stored Excel workbook to PDF, PNG, SVG, or other formats"
description: "Learn how to export Excel charts to PDF, PNG, or SVG using the Aspose.Cells Cloud API — secure, server-side conversion without local dependencies or file downloads."
linktitle: "Export Chart as Format"
date: 2024-06-15
lastmod: 2024-06-15
type: docs
url: /export-chart-as-format/
keywords: "Aspose.Cells Cloud, chart export, Excel API, REST API, PDF conversion"
weight: 100
ArticleTitle: "Export Excel Chart to PDF, PNG, SVG with Aspose.Cells Cloud API"
---
The **ExportChartAsFormat** API (`GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/charts/{chartIndex}`) in Aspose.Cells Cloud converts a chart from a spreadsheet stored in cloud storage directly to a target format—such as PDF, PNG, or SVG—without downloading the source file, enabling efficient, server-side conversion with reduced bandwidth and improved performance for large workbooks.

## Overview

Export a chart from a workbook stored in Aspose Cloud Storage to a target format (PDF, PNG, SVG, etc.) in a single API call — **without downloading the source file**. This cloud-native operation improves performance, reduces bandwidth usage, and enables server-side conversion at scale.

## The Export Chart as Format Web API

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/charts/{chartIndex}
```

### Security and Authentication

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer" target="_blank">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| name | String | Path | (Required) The name of the workbook file to be retrieved. |
| worksheet | String | Path | worksheet name |
| chartIndex | Integer | Path | chart index |
| format | String | Query | (Required) The desired pdf or image format  (e.g., "png", "Pdf", "svg"). |
| folder | String | Query | (Optional) The folder path where the workbook is stored. The default is null. |
| storageName | String | Query | (Optional) The name of the storage if using custom cloud storage. Use default storage if omitted. |
| outPath | String | Query | (Optional) The folder path where the workbook is stored. The default is null. |
| outStorageName | String | Query | Output file Storage Name. |
| fontsLocation | String | Query | Use Custom fonts. |
| region | String | Query | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior. |
| password | String | Query | The password for opening spreadsheet file. |

---

### Response

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**Sample response headers**

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="result"
```

**HTTP Status Codes**

| Code | Meaning | Description |
|---|---|---|
| 200 | OK | The request completed successfully. |
| 400 | Bad Request | Invalid url. |
| 401 | Unauthorized | Authentication has failed, or no credentials were provided. |
| 404 | Not Found | Source file not accessible. |
| 500 | Server Error | The spreadsheet has encountered an anomaly in obtaining conversion data. |

> 🔒 **Authentication Required**  
> All requests must include a valid JWT token. See [Authentication Overview](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) for details.

---

## Example Request (cURL)

```bash
# Step 1: Obtain a JWT access token
curl -v "https://api.aspose.cloud/connect/token" \
  -X POST \
  -d "grant_type=client_credentials&client_id=YOUR_CLIENT_ID&client_secret=YOUR_CLIENT_SECRET" \
  -H "Content-Type: application/x-www-form-urlencoded" \
  -H "Accept: application/json"

# Step 2: Export chart (replace placeholders with your values)
curl -X GET "https://api.aspose.cloud/v4.0/cells/input.xlsx/worksheets/Sheet1/charts/0?format=png" \
  -H "Authorization: Bearer {access_token}" \
  -o "chart_output.png"
```

> 💡 **Tip**: Replace `{access_token}` with the `access_token` returned from the token request. See the [Authentication Guide](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) for step-by-step instructions.

---

## Response

The API returns the chart as a binary file stream in the specified format.

### Success Response (HTTP 200)

| Field  | Type | Description                          |
| ------ | ---- | ------------------------------------ |
| `file` | file | Binary content of the exported chart |

### HTTP Status Codes

| Code | Meaning               | Description                                                                     |
| ---- | --------------------- | ------------------------------------------------------------------------------- |
| 200  | OK                    | Chart exported successfully; response contains binary file content.             |
| 400  | Bad Request           | Invalid path/query parameters (e.g., missing `format`, invalid `chartIndex`).   |
| 401  | Unauthorized          | Invalid or missing JWT token.                                                   |
| 404  | Not Found             | Workbook or worksheet not found in storage.                                     |
| 500  | Internal Server Error | Unexpected error during conversion (e.g., corrupted chart, unsupported format). |

## How to Use the Export Chart as Format API with SDKs?

### Export Chart as Format API Specification

The <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportChartAsFormat" rel="noopener noreferrer">Export Chart as Format API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

Using an SDK simplifies authentication, request formatting, and response handling. Below are complete, copy-pasteable examples:

### Python (Aspose.Cells Cloud SDK for Python)

```python
import asposecellscloud
from asposecellscloud.api import CellsApi
from asposecellscloud.models import ExportRequest

# Initialize API
client_id = "YOUR_CLIENT_ID"
client_secret = "YOUR_CLIENT_SECRET"
api = CellsApi(client_id, client_secret)

# Prepare request
request = ExportRequest(
    format="png",
    out_path="output/chart.png"
)

# Export chart
response = api.cells_export(
    "input.xlsx",
    "Sheet1",
    0,
    request
)

# Save file
with open("chart_output.png", "wb") as f:
    f.write(response.file_contents)
```

### Node.js (Aspose.Cells Cloud SDK for Node.js)

```javascript
const { CellsApi } = require("asposecellscloud");

const clientId = "YOUR_CLIENT_ID";
const clientSecret = "YOUR_CLIENT_SECRET";
const api = new CellsApi(clientId, clientSecret);

// Export chart
api
  .cellsExport("input.xlsx", "Sheet1", 0, "png", {
    outPath: "output/chart.png",
  })
  .then((response) => {
    require("fs").writeFileSync("chart_output.png", Buffer.from(response.body));
    console.log("✅ Chart exported successfully!");
  });
```

> 📦 **All SDKs**: Python, Node.js, Java, PHP, Ruby, Go, and more are available on [GitHub](https://github.com/aspose-cells-cloud).

---

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportChartAsFormat.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportChartAsFormat.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportChartAsFormat.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportChartAsFormat.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportChartAsFormat.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportChartAsFormat.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportChartAsFormat.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportChartAsFormat.go" >}}
{{</tab>}}
{{< /tabs >}}
