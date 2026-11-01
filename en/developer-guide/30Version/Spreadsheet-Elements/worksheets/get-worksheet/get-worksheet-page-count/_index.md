---
title: "Get Page Count for an Excel Worksheet"
second_title: "Developer Guide"
linktitle: "PageCount"
type: docs
url: /worksheets/page-count/
keywords: "Aspose.Cells, Excel API, worksheet page count, REST, cloud SDK, Excel pagination"
description: "Get Excel worksheet printable page count via Aspose.Cells Cloud REST API v3.0 with cURL and SDK examples."
weight: 100
ArticleTitle: "Get Page Count for an Excel Worksheet – Aspose.Cells Cloud API"
---
The **GetWorksheetPageCount** API (`GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pagecount`) retrieves the total number of pages a worksheet will produce when printed, using Aspose.Cells Cloud’s robust rendering engine to accurately calculate pagination based on page setup, print area, and paper size; the operation requires the file name and worksheet name as path parameters and optionally supports folder and storageName query parameters to locate the source workbook.

**Authentication:** All Aspose.Cells Cloud endpoints require a Bearer token obtained via the OAuth2 flow. Include the token in the `Authorization` header as shown in the cURL example below.

## The Get Worksheet Page Count Web API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pagecount
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer" target="_blank">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| name | String | Path | The file name. |
| sheetName | String | Path | The worksheet name. |
| folder | String | Query | The folder where the file is situated. |
| storageName | String | Query | The storage name where the file is situated. |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/GetPageCount) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the **cURL** command‑line tool to access Aspose.Cells web services easily. The example below shows how to call the API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/worksheets/Sheet1/pagecount" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <access_token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "PageCount": 3
}
```

{{< /tab >}}

{{< /tabs >}}

### Response Details

```json
[
  {
    "Name": "Int32",
    "DataType": {
      "Identifier": "Integer"
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

| HTTP Status | Meaning                                              |
| ----------- | ---------------------------------------------------- |
| **200**     | Success – returns the JSON payload shown above.      |
| **401**     | Unauthorized – missing or invalid token.             |
| **404**     | Not Found – the file or worksheet does not exist.    |
| **500**     | Internal Server Error – unexpected server condition. |

### Version History

_API version **v3.0** (released 2025). If you are using a newer version, refer to the updated endpoint documentation._

## Cloud SDK Family

Using an SDK is the fastest way to develop. An SDK abstracts low‑level details so you can focus on your business logic. See the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetPageCount.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetPageCount.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetPageCount.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetPageCount.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetPageCount.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetPageCount.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetPageCount.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetPageCount.go" >}}

{{< /tab >}}

{{< /tabs >}}

### Notes

- The page count reflects the printable layout, taking page breaks, margins, and scaling into account. Hidden rows or columns may affect the result.
- Ensure the target worksheet exists and the file is stored in the specified `folder` and `storageName` before making the request.
