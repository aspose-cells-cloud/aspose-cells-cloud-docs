---
title: "Update Worksheet Properties – Aspose.Cells Cloud API Reference (v3.0)"
second_title: "Developer Guide"
linktitle: "Update"
type: docs
url: /worksheets/update-properties/
aliases: [/update-excel-worksheet-properties/]
weight: 100
keywords:
  [
    "Aspose.Cells",
    "Excel",
    "worksheet",
    "update properties",
    "REST API",
    "cloud",
    "v3.0",
  ]
description: "Update Excel worksheet properties like DisplayZeros and IsRulerVisible using Aspose.Cells Cloud REST API v3.0"
ArticleTitle: "Update Worksheet Properties – Aspose.Cells Cloud API Reference (v3.0)"
---
The **PostUpdateWorksheetProperty** API (`POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}`) updates core properties of a specific worksheet within a workbook stored in the cloud, using Aspose.Cells Cloud’s REST interface. Developers supply the workbook name, worksheet name, and a JSON-serialized worksheet object in the request body to modify properties such as visibility, tab color, or protection settings—enabling programmatic control over worksheet behavior without manual Excel interaction.

## The Post Update Worksheet Property Web API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer" target="_blank">JWT token-based authentication</a>.

### **Request parameters**

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| name | String | Path | The file name. |
| sheetName | String | Path | The worksheet name. |
| sheet | class:worksheet | HTTPBody | The worksheet description. |
| folder | String | Query | The folder where the file is situated. |
| storageName | String | Query | The storage name where the file is situated. |

The **sheet** object is sent in the request body as JSON. Example properties that can be modified include `DisplayZeros`, `IsRulerVisible`, `IsGridlinesVisible`, and others defined in the API specification.

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/PostUpdateWorksheetProperty) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1" \
-X POST \
-d '{"DisplayZeros":"true","IsRulerVisible":"true"}' \
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

Typical response codes:

- **200** – Success. The worksheet properties were updated.
- **400** – Invalid request (e.g., malformed JSON or missing required parameter).
- **401** – Unauthorized – missing or invalid JWT token.
- **404** – Workbook or worksheet not found.
- **500** – Internal server error.

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

**Prerequisites:** You must have a valid Aspose Cloud account, obtain a JWT access token, and ensure the target workbook is stored in a supported storage location. All requests should be made over **HTTPS**.

## How to Use the Post Update Worksheet Property API with SDKs?

### Post Update Worksheet Property API Specification

The <a href="https://reference.aspose.cloud/cells/#/Worksheets/PostUpdateWorksheetProperty" rel="noopener noreferrer">Post Update Worksheet Property API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUpdateWorksheetProperty.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUpdateWorksheetProperty.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUpdateWorksheetProperty.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUpdateWorksheetProperty.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUpdateWorksheetProperty.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUpdateWorksheetProperty.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUpdateWorksheetProperty.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUpdateWorksheetProperty.go" >}}
{{</tab>}}
{{< /tabs >}}
