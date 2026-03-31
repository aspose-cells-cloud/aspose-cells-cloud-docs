---
title: "Update Worksheet Properties – Aspose.Cells Cloud API Reference (v3.0)"
second_title: "Document"
linktitle: "Update"
type: docs
url: /worksheets/update-properties/
aliases: [/update-excel-worksheet-properties/]
weight: 20
keywords: ["Aspose.Cells", "Excel", "worksheet", "update properties", "REST API", "cloud", "v3.0"]
description: "Learn how to update base properties (e.g., display zeros, ruler visibility) of an Excel worksheet using Aspose.Cells Cloud REST API v3.0. Includes cURL request, SDK samples, parameters, and error handling."
---

This REST API updates worksheet base properties.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}
```

**Authentication** – The endpoint requires an OAuth 2.0 JWT bearer token. Obtain a token from the `/connect/token` endpoint using your Aspose Cloud client ID and secret, then include it in the `Authorization` header (`Bearer <jwt token>`).

The request parameters are:

| Parameter Name | Type   | Path/Query String/HTTPBody | Description |
|----------------|--------|----------------------------|-------------|
| name           | string | path                       | Workbook filename (including extension). |
| sheetName      | string | path                       | Name of the worksheet to be updated. |
| sheet          | object | body                       | JSON object containing worksheet property key/value pairs (e.g., `DisplayZeros`, `IsRulerVisible`). |
| folder         | string | query                      | Folder path in storage where the workbook is located. |
| storageName    | string | query                      | Name of the storage to use. |

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

## Cloud SDK Family

Using an SDK is the fastest way to accelerate development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Objective C" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorksheetsPostUpdateWorksheetProperty.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-UpdateWorksheetProperties-update-worksheet-properties.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PostUpdateWorksheetProperty-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-update_worksheet_property-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-UpdateWorksheetProperties-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-UpdateWorksheetProperties-update-worksheet-properties.java" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-UpdateWorksheetProperties-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "ce38cb4feb118132fada7801c7f5cd43" >}}

{{< /tab >}}

{{< /tabs >}}