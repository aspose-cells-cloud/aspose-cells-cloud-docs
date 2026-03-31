---
title: "Add Date Filter to an Excel Worksheet"
second_title: "Document"
linktitle: "Add date filter"
type: docs
url: /autofilter/add-date-filter/
aliases:
  - /add-date-filter-in-a-worksheet/
  - /autofilter/add-a-date-filter/
keywords: "Aspose.Cells, Excel date filter, AutoFilter API, REST API, cloud SDK, cURL, spreadsheet automation"
description: "Learn how to add a date filter to an Excel worksheet using Aspose.Cells Cloud REST API (v3.0). Includes cURL example, SDK snippets (C#, Java, Python, etc.), parameters, and error handling."
weight: 65
---

This REST API adds a **date filter** to an Excel worksheet.

## REST API

### Prerequisites
- **Authentication** – Obtain a JWT token via the Aspose Cloud OAuth flow and include it in the `Authorization` header as `Bearer <jwt token>`.  
- **API version** – The endpoint used below targets **v3.0** of the Aspose.Cells Cloud API.  
- **Supported SDKs** – You may also call the operation through any of the Aspose.Cells Cloud SDKs (C#, Java, Python, etc.).

### Endpoint
```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/dateFilter
```

### Request parameters

The request parameters are listed below:

| Parameter Name          | Type    | Location | Description |
|-------------------------|---------|----------|-------------|
| **name**                | string  | Path     | The workbook name. |
| **sheetName**           | string  | Path     | The worksheet name. |
| **range**               | string  | Query    | Excel range to which the filter is applied (e.g., `A1:B1`). |
| **fieldIndex**          | integer | Query    | Zero‑based index of the column to filter. |
| **dateTimeGroupingType**| string  | Query    | Grouping type for the date/time filter. Allowed values are `Day`, `Hour`, `Minute`, `Month`, `Second`, `Year`. Values are case‑sensitive; the default is `Day`. |
| **year**                | integer | Query    | Year component of the filter value. |
| **month**               | integer | Query    | Month component of the filter value. |
| **day**                 | integer | Query    | Day component of the filter value. |
| **hour**                | integer | Query    | Hour component of the filter value. |
| **minute**              | integer | Query    | Minute component of the filter value. |
| **second**              | integer | Query    | Second component of the filter value. |
| **matchBlanks**         | boolean | Query    | Include blank cells (`true` or `false`). |
| **refresh**             | boolean | Query    | Refresh the filter after applying (`true` or `false`). |
| **folder**              | string  | Query    | Folder path of the original workbook. |
| **storageName**         | string  | Query    | Name of the storage service. |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetDateFilter) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the **cURL** command‑line tool to access Aspose.Cells web services easily. The following example shows how to make a call to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/dateFilter?range=A1:B1&fieldIndex=0&dateTimeGroupingType=Year&year=1920&refresh=true" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Error responses
| HTTP Status | Code | Message | Description |
|-------------|------|---------|-------------|
| 400 Bad Request | 400 | Invalid range format. Expected A1:B1. | The `range` query parameter is malformed or missing. |
| 401 Unauthorized | 401 | Access token is missing or invalid. | Authentication failed; obtain a valid JWT token. |
| 404 Not Found | 404 | Workbook or worksheet not found. | The specified `name` or `sheetName` does not exist. |
| 500 Internal Server Error | 500 | Unexpected server error. | An unhandled exception occurred on the server. |

The successful response contains two fields:

- **Code** – HTTP status code returned by the API (200 for success).  
- **Status** – Textual description of the result.

## Cloud SDK Family

Using an SDK is the fastest way to develop. An SDK handles low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetDateFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetDateFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetDateFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetDateFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetDateFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetDateFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetDateFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetDateFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}