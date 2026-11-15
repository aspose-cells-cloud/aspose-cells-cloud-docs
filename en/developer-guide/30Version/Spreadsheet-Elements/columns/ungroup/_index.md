---
title: Ungroup Columns in Excel – Aspose.Cells Cloud API
second_title: "Aspose.Cells Cloud Documentation"
linktitle: "Ungroup Columns"
type: docs
url: /columns/ungroup/
aliases:
  [
    "/ungroup-columns-in-an-excel-worksheet/",
    "/ungroup-columns-in-excel-worksheet/",
  ]
description: "Ungroup Excel columns via Aspose.Cells Cloud REST API: POST request, parameters, cURL, and SDK examples"
keywords: "ungroup columns, Excel API, Aspose.Cells Cloud, REST API, column grouping, worksheet operations"
slug: columns/ungroup
date: 2024-06-15
weight: 70
draft: false
ArticleTitle: "Ungroup Columns in Excel with Aspose.Cells Cloud REST API"
---

The **PostUngroupWorksheetColumns** API (`POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/ungroup`) in Aspose.Cells Cloud enables developers to remove column grouping from a specified worksheet by providing the workbook name, worksheet name, and the first and last column indices to ungroup. This REST operation supports ungrouping contiguous or non-contiguous column ranges, restoring individual column visibility and editability as defined in Excel’s grouping behavior.

## The Post Ungroup Worksheet Columns Web API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/ungroup
```

### Security and Authentication

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer" target="_blank">JWT token-based authentication</a>.

### Path Parameters

| Parameter Name | Type    | Path/Query String/HTTPBody | Description                                  |
| -------------- | ------- | -------------------------- | -------------------------------------------- |
| name           | String  | Path                       | The file name.                               |
| sheetName      | String  | Path                       | The worksheet name.                          |
| firstIndex     | Integer | Query                      | The first column index to be operated.       |
| lastIndex      | Integer | Query                      | The last column index to be operated.        |
| folder         | String  | Query                      | The folder where the file is situated.       |
| storageName    | String  | Query                      | The storage name where the file is situated. |

### Response

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

| Code | Meaning               | Description                                                              |
| ---- | --------------------- | ------------------------------------------------------------------------ |
| 200  | OK                    | The request completed successfully.                                      |
| 400  | Bad Request           | The request is malformed or one or more parameters are invalid.          |
| 401  | Unauthorized          | Authentication failed, or the JWT token is missing or expired.           |
| 404  | Not Found             | The requested workbook, worksheet, or resource was not found.            |
| 500  | Internal Server Error | The server encountered an unexpected error while processing the request. |

## How to Use the Post Ungroup Worksheet Columns API with SDKs?

### Post Ungroup Worksheet Columns API Specification

The <a href="https://reference.aspose.cloud/cells/#/Cells/PostUngroupWorksheetColumns" rel="noopener noreferrer">Post Ungroup Worksheet Columns API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

### ReqcURLuest Example

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/ungroup?firstIndex=1&lastIndex=5" \
     -H "Authorization: Bearer <YOUR_ACCESS_TOKEN>" \
     -H "Accept: application/json"
```

Replace `<YOUR_ACCESS_TOKEN>` with your valid JWT token.

**Success Response (200 OK)**

```json
{
  "Code": 200,
  "Status": "OK",
  "Columns": {
    "FirstIndex": 1,
    "LastIndex": 5
  }
}
```

The `Columns` object confirms the range of columns that were successfully ungrouped.

**Error Response**

| Field          | Type    | Description                                      |
| -------------- | ------- | ------------------------------------------------ |
| `Code`         | integer | HTTP status code (e.g., `400`, `401`).           |
| `Status`       | string  | Short error description (e.g., `"Bad Request"`). |
| `ErrorMessage` | string  | Detailed error message.                          |

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUngroupWorksheetColumns.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUngroupWorksheetColumns.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUngroupWorksheetColumns.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUngroupWorksheetColumns.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUngroupWorksheetColumns.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUngroupWorksheetColumns.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUngroupWorksheetColumns.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUngroupWorksheetColumns.go" >}}
{{</tab>}}
{{< /tabs >}}
