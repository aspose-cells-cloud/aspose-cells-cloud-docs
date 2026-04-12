---
title: "Add Hyperlink to Worksheet"
type: docs
url: /hyperlinks/add/
aliases: [/add-hyperlinks-to-excel-worksheet/]
keywords: "Aspose.Cells, add hyperlink, Excel REST API, cloud SDK"
description: "Learn how to add a hyperlink to an Excel worksheet using the Aspose.Cells Cloud v3.0 REST API. Includes endpoint, full parameter guide, cURL example, and SDK snippets for C#, Java, Python, and more."
weight: 20
---

This REST API adds a hyperlink to an Excel worksheet.

## REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks
```

### Request Parameters

| Parameter Name | Type    | Location | Description                                                                               |
| -------------- | ------- | -------- | ----------------------------------------------------------------------------------------- |
| name           | string  | path     | Document name.                                                                            |
| sheetName      | string  | path     | Worksheet name.                                                                           |
| firstRow       | integer | query    | Zero‑based index of the first row of the range to which the hyperlink will be applied.    |
| firstColumn    | integer | query    | Zero‑based index of the first column of the range to which the hyperlink will be applied. |
| totalRows      | integer | query    | Number of rows that the hyperlink range spans.                                            |
| totalColumns   | integer | query    | Number of columns that the hyperlink range spans.                                         |
| address        | string  | query    | The target URL that the hyperlink points to (URL‑encoded).                                |
| folder         | string  | query    | The document folder.                                                                      |
| storageName    | string  | query    | Storage name.                                                                             |

The request can also include a JSON body containing the same fields (`Address`, `FirstRow`, `FirstColumn`, `TotalRows`, `TotalColumns`). Supplying the body is useful when you prefer a payload over query‑string parameters.

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
