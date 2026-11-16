---
title: "Delete Vertical Page Break | Aspose.Cells Cloud REST API"
date: 2024-03-15
lastmod: 2024-03-15
description: "Learn how to delete a vertical page break from an Excel worksheet using the Aspose.Cells Cloud REST API v3.0. Includes cURL examples, error codes, and SDK snippets in C#, Java, Python, Node.js, and Go."
tags:
  - "page-break"
  - "excel-api"
  - "rest-api"
categories:
  - "cells"
  - "api-reference"
weight: 100
draft: false
slug: delete-vertical-page-break
api_version: v3.0
---

The **DeleteVerticalPageBreak** API (`DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/verticalpagebreaks/{index}`) enables developers to remove a specific vertical page break from a worksheet in an Excel workbook via the Aspose.Cells Cloud REST API, using the workbook name, worksheet name, and zero-based index of the page break as required path parameters.

> 💡 **Tip**: Replace `client_id` and `client_secret` with valid credentials from your [Aspose Cloud Dashboard](https://dashboard.aspose.cloud/). For JWT token generation, see our [Authentication Guide]（https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/）.

---

## The Delete Vertical Page Break Web API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/verticalpagebreaks/{index}
```

### Security and Authentication

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer" target="_blank">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type    | Path/Query String/HTTPBody | Description                                                                             |
| -------------- | ------- | -------------------------- | --------------------------------------------------------------------------------------- |
| name           | String  | Path                       | The workbook name.                                                                      |
| sheetName      | String  | Path                       | The worksheet name.                                                                     |
| index          | Integer | Path                       | Removes the vertical page break element at a specified name. Element index, zero based. |
| folder         | String  | Query                      | The folder where the file is situated.                                                  |
| storageName    | String  | Query                      | The storage name where the file is situated.                                            |

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

### Success Response

| Code    | Description                                       |
| ------- | ------------------------------------------------- |
| **200** | The vertical page break was deleted successfully. |

**Example payload**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### Error Responses

| HTTP Code | Description                                                                    |
| --------- | ------------------------------------------------------------------------------ |
| **401**   | Unauthorized – missing or invalid token.                                       |
| **404**   | Not Found – the specified file, worksheet, or page‑break index does not exist. |
| **400**   | Bad Request – malformed request syntax or invalid parameters.                  |
| **500**   | Internal Server Error – an unexpected condition was encountered.               |

**Sample error payloads**

_401 – Unauthorized_

```json
{
  "Code": 401,
  "Message": "Invalid authentication token."
}
```

_404 – Not Found_

```json
{
  "Code": 404,
  "Message": "The specified file, worksheet, or page‑break index was not found."
}
```

_400 – Bad Request_

```json
{
  "Code": 400,
  "Message": "The request parameters are invalid or malformed."
}
```

_500 – Internal Server Error_

```json
{
  "Code": 500,
  "Message": "An unexpected server error occurred."
}
```

## How to Use the Delete Vertical Page Break API with SDKs?

### Delete Vertical Page Break API Specification

The <a href="https://reference.aspose.cloud/cells/#/PageBreaks/DeleteVerticalPageBreak" rel="noopener noreferrer">Delete Vertical Page Break API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

**cUrl Example**

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/verticalpagebreaks/0?folder=Docs&storageName=MyStorage" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt_token>"
```

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteVerticalPageBreak.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteVerticalPageBreak.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteVerticalPageBreak.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteVerticalPageBreak.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteVerticalPageBreak.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteVerticalPageBreak.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteVerticalPageBreak.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteVerticalPageBreak.go" >}}
{{</tab>}}
{{< /tabs >}}
