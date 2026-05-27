---
title: "Get Page Count from an Excel Workbook – Aspose.Cells Cloud API (v3.0)"
second_title: "Document"
linktitle: "Pages"
type: docs
url: /get-page-count-from-an-excel-file/
aliases: [/workbook/page-count/, /workbook/get/page-count/]
keywords: "Aspose.Cells, page count, Excel API, REST, v3.0"
description: "Learn how to retrieve the printable page count of an Excel workbook using Aspose.Cells Cloud REST API v3.0. Includes request format, required parameters, cURL example, SDK code snippets, and error handling."
weight: 10
version: "v3.0"
---

This REST API returns the **page count** for a workbook.

## REST API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/pagecount
```

### The request parameters

| Parameter Name | Type   | Location | Required | Description                            |
| -------------- | ------ | -------- | -------- | -------------------------------------- |
| name           | string | path     | Yes      | The name of the Excel document.        |
| folder         | string | query    | No       | The folder that contains the document. |
| storageName    | string | query    | No       | The name of the storage to use.        |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Workbook/GetPageCount) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells REST API easily. The following example shows how to call the endpoint with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Report.xlsx/pagecount?folder=Docs&storageName=MyStorage" \
  -X GET \
  -H "Authorization: Bearer <jwt token>" \
  -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
13
```

{{< /tab >}}

{{< /tabs >}}

### Response Schema

| HTTP Status | Data Type | Description                                                       |
| ----------- | --------- | ----------------------------------------------------------------- |
| 200         | integer   | The total number of printable pages in the workbook (e.g., `13`). |
| 4xx-5xx     | JSON      | Error object (see _Error Handling_ section).                      |

## Cloud SDK Family

Using an SDK is the best way to speed up the development. An SDK takes care of low‑level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetPageCount.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetPageCount.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetPageCount.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetPageCount.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetPageCount.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetPageCount.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetPageCount.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetPageCount.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Error Handling

| HTTP Status | Description                                | Example JSON Body                                                                            |
| ----------- | ------------------------------------------ | -------------------------------------------------------------------------------------------- |
| 401         | Invalid or missing JWT token.              | `{ "Code": "InvalidAuthenticationToken", "Message": "Access token is missing or invalid." }` |
| 404         | The specified workbook could not be found. | `{ "Code": "FileNotFound", "Message": "The requested file does not exist." }`                |
| 400         | Bad request – missing required parameters. | `{ "Code": "BadRequest", "Message": "Required parameter 'name' is missing." }`               |
| 500         | Internal server error.                     | `{ "Code": "InternalError", "Message": "An unexpected error occurred." }`                    |