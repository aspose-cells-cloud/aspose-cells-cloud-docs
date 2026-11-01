---
title: "Add Hyperlink to Worksheet"
type: docs
url: /hyperlinks/add/
aliases: [/add-hyperlinks-to-excel-worksheet/]
keywords: "Aspose.Cells, add hyperlink, Excel REST API, cloud SDK"
description: "Add hyperlinks to Excel worksheets using Aspose.Cells Cloud API PUT /cells/{name}/worksheets/{sheetName}/hyperlinks"
weight: 100
linktitle: "Add Hyperlink"
ArticleTitle: "Add Hyperlink to Excel Worksheet via Aspose.Cells Cloud REST API"
---
The **PutWorksheetHyperlink** API (`PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks`) enables programmatic addition of hyperlinks to Excel worksheets via Aspose.Cells Cloud, supporting range-based linking by specifying first row/column, total rows/columns, and the target address; this RESTful operation allows developers to automate hyperlink insertion across supported cloud-based Excel workflows using SDKs for .NET, Java, Python, and other languages.

## The Put Worksheet Hyperlink Web API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer" target="_blank">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| name | String | Path | The file name. |
| sheetName | String | Path | The worksheet name. |
| firstRow | Integer | Query | First row of the hyperlink range. |
| firstColumn | Integer | Query | First column of the hyperlink range. |
| totalRows | Integer | Query | Number of rows in this hyperlink range. |
| totalColumns | Integer | Query | Number of columns of this hyperlink range. |
| address | String | Query | Address of the hyperlink. |
| folder | String | Query | The folder where the file is situated. |
| storageName | String | Query | The storage name where the file is situated. |

The request can also include a JSON body containing the same fields (`Address`, `FirstRow`, `FirstColumn`, `TotalRows`, `TotalColumns`). Supplying the body is useful when you prefer a payload over query‑string parameters.

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

### Error Responses

| HTTP Code | Reason                                             | Example Body                                                        |
| --------- | -------------------------------------------------- | ------------------------------------------------------------------- |
| **400**   | Bad Request – missing or invalid parameters.       | `{ "Code":"400", "Message":"Invalid parameter value." }`            |
| **401**   | Unauthorized – missing or invalid JWT token.       | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404**   | Not Found – workbook or worksheet does not exist.  | `{ "Code":"404", "Message":"File not found." }`                     |
| **500**   | Internal Server Error – unexpected server failure. | `{ "Code":"500", "Message":"An unexpected error occurred." }`       |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Hypelinks/PutWorksheetHyperlink) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/hyperlinks?firstRow=1&firstColumn=6&totalRows=1&totalColumns=1&address=https%3A%2F%2Fwww.msnbc.com%2F" \
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

If the request fails, the API returns standard HTTP error codes (e.g., 400 Bad Request, 401 Unauthorized, 404 Not Found, 500 Internal Server Error) together with a JSON payload that contains an error message and code.

## Cloud SDK Family

Using an SDK is the fastest way to develop. An SDK handles low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetHyperlink.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetHyperlink.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetHyperlink.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetHyperlink.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetHyperlink.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetHyperlink.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetHyperlink.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetHyperlink.go" >}}

{{< /tab >}}

{{< /tabs >}}
