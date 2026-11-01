---
title: "Get All Worksheets"
second_title: "Developer Guide"
linktitle: "All"
type: docs
url: /worksheets/get-all/
aliases: [/get-worksheet-count/]
keywords: "Aspose.Cells, Cloud API, Get Worksheets, Excel, REST, SDK"
description: "Retrieve all worksheets from an Excel workbook using Aspose.Cells Cloud REST API with cURL or SDK examples."
weight: 100
ArticleTitle: "Get All Worksheets from Excel Workbook via Aspose.Cells Cloud REST API"
---
The **GetWorksheets** API (`GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets`) retrieves a list of worksheet descriptions from a specified workbook file in Aspose.Cells Cloud, supporting optional `folder` and `storageName` query parameters to locate the file.

## The Get Worksheets Web API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer" target="_blank">JWT token-based authentication</a>.

### **Request parameters**

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| name | String | Path | The file name. |
| folder | String | Query | The folder where the file is situated. |
| storageName | String | Query | The storage name where the file is situated. |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheets) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells Cloud services. The example below demonstrates a GET request to retrieve the worksheets.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Worksheets": {
    "WorksheetList": [
      {
        "link": {
          "Href": "/Sheet1",
          "Rel": "self"
        }
      },
      {
        "link": {
          "Href": "/Sheet2",
          "Rel": "self"
        }
      }
    ],
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets",
      "Rel": "self"
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### **Response**

```json
[
  {
    "Name": "WorksheetsResponse",
    "DataType": {
      "Identifier": "Class",
      "Reference": "WorksheetsResponse"
    }
  }
]
```

**Sample response headers**

```http
HTTP/1.1 200 OK
Content-Type: application/json
```

### Error Handling

Typical HTTP status codes returned by this endpoint:

| Code | Meaning               | Description                                |
| ---- | --------------------- | ------------------------------------------ |
| 400  | Bad Request           | Missing required parameter (e.g., `name`). |
| 401  | Unauthorized          | Invalid or missing JWT token.              |
| 404  | Not Found             | Specified workbook does not exist.         |
| 500  | Internal Server Error | Unexpected server condition.               |

Error responses are returned in JSON format, for example:

```json
{
  "Code": "401",
  "Message": "Invalid access token."
}
```

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheets.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheets.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheets.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheets.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheets.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheets.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheets.go" >}}

{{< /tab >}}

{{< /tabs >}}
