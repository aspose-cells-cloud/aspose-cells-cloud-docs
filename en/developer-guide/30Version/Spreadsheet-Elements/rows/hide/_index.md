---
title: "Hide rows on an Excel worksheet"
second_title: "Developer Guide"
linktitle: "Hide"
type: docs
url: /rows/hide/
aliases: [/hide-rows-in-excel-worksheet/]
keywords: "hide rows, Aspose.Cells Cloud, Excel API, REST, SDK"
description: "Hide Excel worksheet rows via Aspose.Cells Cloud REST API using cURL or SDKs. Specify startrow and totalRows parameters."
weight: 40
ArticleTitle: "Hide Rows in Excel Worksheet using Aspose.Cells Cloud API"
---
The **PostHideWorksheetRows** API (`POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/hide`) enables programmatic hiding of rows in an Excel worksheet via Aspose.Cells Cloud, supporting operations like specifying the starting row index and number of rows to hide through required query parameters `startrow` and `totalRows`, while allowing optional folder and storage context for cloud-based file management.

## The Post Hide Worksheet Rows Web API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/hide
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| name | String | Path | The file name. |
| sheetName | String | Path | The worksheet name. |
| startrow | Integer | Query | The begin row index to be operated. |
| totalRows | Integer | Query | Number of rows to be operated. |
| folder | String | Query | The folder where the file is situated. |
| storageName | String | Query | The storage name where the file is situated. |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Cells/PostHideWorksheetRows) provides a publicly accessible programming interface that lets you perform REST interactions directly from a web browser.

You can use the **cURL** command‑line tool to call Aspose.Cells web services. The API requires a JWT Bearer token obtained from the Aspose Cloud OAuth endpoint; include it in the `Authorization` header. The example below demonstrates how to hide a row using cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/hide?startrow=1&totalRows=1" \
  -X POST \
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

**Response status codes**


A successful call returns a JSON object that contains the fields `Code` and `Status`. In case of an error, the response includes additional fields such as `Message` and appropriate HTTP status codes (e.g., 400, 401, 404, 500).

**Notes:** Ensure that the `startrow` value is within the worksheet’s row range; otherwise the API will return a 400 error. Row indices are zero‑based, so `startrow=0` refers to the first row.

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
| 500 | Internal Server Error | The server encountered an unexpected error while processing the request. |

## Cloud SDK Family

Using an SDK is the fastest way to integrate this functionality into your application. SDKs handle low‑level details so you can focus on business logic. See the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to hide rows using various SDKs. (The example filenames reference “Unhide” due to legacy naming; the code inside each gist performs the **Hide** operation.)

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUnhideWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUnhideWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUnhideWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUnhideWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUnhideWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUnhideWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUnhideWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUnhideWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}
