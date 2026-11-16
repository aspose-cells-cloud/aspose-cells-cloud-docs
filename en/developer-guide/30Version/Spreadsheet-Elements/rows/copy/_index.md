---
title: "Copy Rows on an Excel Worksheet"
second_title: "Aspose.Cells Cloud Document"
linktitle: "Copy"
type: docs
url: /rows/copy/
aliases: [/copy-rows-in-excel-worksheet/]
description: "Copy Excel rows via Aspose.Cells Cloud REST API v3.0 using source/destination indices and row count."
api_version: "v3.0"
method: "POST"
weight: 30
ArticleTitle: "Copy Rows in Excel with Aspose.Cells Cloud REST API v3.0"
keywords: "Aspose.Cells Cloud, copy rows Excel, worksheet row copy, REST API copy rows, copy rows programmatically, Excel automation, copy entire rows, row copy API, Aspose.Cells Cloud SDK, copy rows between worksheets"
---

The **PostCopyWorksheetRows** API (`POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/copy`) enables copying data and formats from specific entire rows in a worksheet by specifying source and destination row indices along with the number of rows to copy. Aspose.Cells Cloud supports this operation to automate row duplication tasks programmatically, preserving cell values, styles, and formulas. Developers can integrate this capability using REST calls or SDKs for languages including .NET, Java, Python, and Node.js.

## The Post Copy Worksheet Rows Web API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/copy
```

### Security and Authentication

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer" target="_blank">JWT token-based authentication</a>.

### Path Parameters

| Parameter Name      | Type    | Path/Query String/HTTPBody | Description                                  |
| ------------------- | ------- | -------------------------- | -------------------------------------------- |
| name                | String  | Path                       | The file name.                               |
| sheetName           | String  | Path                       | The worksheet name.                          |
| sourceRowIndex      | Integer | Query                      | Source row index                             |
| destinationRowIndex | Integer | Query                      | Destination row index                        |
| rowNumber           | Integer | Query                      | The copied row number                        |
| worksheet           | String  | Query                      | The worksheet name.                          |
| folder              | String  | Query                      | The folder where the file is situated.       |
| storageName         | String  | Query                      | The storage name where the file is situated. |

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

## Successful Response

| Code    | Description               |
| ------- | ------------------------- |
| **200** | Rows copied successfully. |

```json
{
  "Code": 200,
  "Status": "OK"
}
```

The response body is an instance of `CellsCloudResponse`.

## How to Use the Post Copy Worksheet Rows API with SDKs?

### Post Copy Worksheet Rows API Specification

The <a href="https://reference.aspose.cloud/cells/#/Cells/PostCopyWorksheetRows" rel="noopener noreferrer">Post Copy Worksheet Rows API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

**cURL Example**

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/copy?sourceRowIndex=1&destinationRowIndex=12&rowNumber=10" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

> **Note**  
> Replace `<jwt token>` with a valid JWT token obtained from the authentication service.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCopyWorksheetRows.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCopyWorksheetRows.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCopyWorksheetRows.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCopyWorksheetRows.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCopyWorksheetRows.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCopyWorksheetRows.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCopyWorksheetRows.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCopyWorksheetRows.go" >}}
{{</tab>}}
{{< /tabs >}}
