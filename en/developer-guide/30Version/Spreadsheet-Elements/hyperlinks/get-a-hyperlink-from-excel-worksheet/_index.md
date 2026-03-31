---
title: "Get Worksheet Hyperlink"
type: docs
url: /hyperlinks/get/
keywords: "Aspose.Cells Cloud, Get Worksheet Hyperlink, Excel hyperlink API, REST, JWT authentication"
description: "Retrieve a specific hyperlink from an Excel worksheet using Aspose.Cells Cloud API (v3.0). Includes endpoint, parameters, cURL example, authentication steps, error handling, and SDK snippets."
weight: 10
---

This REST API retrieves a worksheet **hyperlink** using the **Aspose.Cells Get Hyperlink API**.

## Prerequisites

Before calling the endpoint, ensure that:

* The Excel file is already uploaded to the chosen storage.
* You know the **storage name** (if a custom storage is used) and the **folder** path where the file resides.
* The worksheet name and the zero‑based **hyperlink index** you want to read are known.

## Authentication

The API requires a JWT token in the `Authorization` header.

1. Request a token from the Aspose Cloud OAuth endpoint:

   ```bash
   curl -X POST "https://api.aspose.cloud/connect/token" \
        -H "Content-Type: application/x-www-form-urlencoded" \
        -d "grant_type=client_credentials&client_id=<your_client_id>&client_secret=<your_client_secret>"
   ```

2. The response contains an `access_token`. Use it as follows:

   ```bash
   -H "Authorization: Bearer <access_token>"
   ```

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks/{hyperlinkIndex}
```

The request parameters include:

| Parameter Name | Type    | Location | Description                                   |
|----------------|---------|----------|-----------------------------------------------|
| name           | string  | path     | The name of the Excel file.                   |
| sheetName      | string  | path     | The name of the worksheet containing the link.|
| hyperlinkIndex | integer | path     | Zero‑based index of the hyperlink to retrieve.|
| folder         | string  | query    | The folder where the document is stored.      |
| storageName    | string  | query    | The name of the storage service.              |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Hyperlinks/GetWorksheetHyperlink) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make a call to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/hyperlinks/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Hyperlink": {
    "Address": "https://docs.aspose.cloud/display/cellscloud/Get+Hyperlink+from+Excel+Worksheet",
    "Area": {
      "EndColumn": 0,
      "EndRow": 1,
      "StartColumn": 0,
      "StartRow": 1
    },
    "ScreenTip": null,
    "TextToDisplay": "https://docs.aspose.cloud/display/cellscloud/Get+Hyperlink+from+Excel+Worksheet",
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet1/hyperlinks/1",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Error Responses

| HTTP Status | Description                              | Recommended Action                              |
|-------------|------------------------------------------|-------------------------------------------------|
| 400         | Bad request – missing or invalid parameters. | Verify that all required path and query parameters are correct. |
| 401         | Unauthorized – token missing or expired. | Obtain a fresh JWT token using the authentication steps above. |
| 404         | Not found – file, worksheet, or hyperlink index does not exist. | Check the file name, worksheet name, folder, storage name, and hyperlink index. |
| 500         | Internal server error – unexpected condition on the server. | Retry later or contact Aspose support if the problem persists. |

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK handles low‑level details, allowing you to focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetHyperlink.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetHyperlink.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetHyperlink.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetHyperlink.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetHyperlink.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetHyperlink.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetHyperlink.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetHyperlink.go" >}}

{{< /tab >}}

{{< /tabs >}}

---

*Written by the Aspose Cloud Documentation Team*

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "WebAPI",
  "name": "Aspose.Cells Get Worksheet Hyperlink",
  "description": "Retrieves a specific hyperlink from an Excel worksheet.",
  "url": "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks/{hyperlinkIndex}",
  "documentation": "https://docs.aspose.cloud/cells/hyperlinks/get/",
  "version": "3.0",
  "endpoint": {
    "@type": "EntryPoint",
    "urlTemplate": "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks/{hyperlinkIndex}",
    "httpMethod": "GET",
    "parameter": [
      {
        "name": "name",
        "description": "Excel file name",
        "required": true,
        "valueRequired": true,
        "in": "path"
      },
      {
        "name": "sheetName",
        "description": "Worksheet name",
        "required": true,
        "valueRequired": true,
        "in": "path"
      },
      {
        "name": "hyperlinkIndex",
        "description": "Zero‑based hyperlink index",
        "required": true,
        "valueRequired": true,
        "in": "path"
      },
      {
        "name": "folder",
        "description": "Folder where the file is stored",
        "required": false,
        "in": "query"
      },
      {
        "name": "storageName",
        "description": "Name of the storage service",
        "required": false,
        "in": "query"
      }
    ]
  },
  "potentialAction": {
    "@type": "SearchAction",
    "target": "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks/{hyperlinkIndex}",
    "query-input": "required name=param1, required sheetName=param2, required hyperlinkIndex=param3"
  }
}
</script>