---
title: "Delete Worksheet Comment API – Aspose.Cells Cloud"
type: docs
url: /comments/delete/
description: "Delete Excel worksheet comments via Aspose.Cells Cloud REST API v3.0 with JWT auth and SDK examples."
keywords: "delete cell comment, Excel API, Aspose.Cells Cloud, REST API, worksheet comment removal"
date: "2024-05-15"
lastModified: "2024-05-15"
canonical: "https://docs.aspose.cloud/cells/comments/delete/"
draft: false
weight: 100
linktitle: "Delete Comment"
ArticleTitle: "Delete Worksheet Comment via Aspose.Cells Cloud REST API"
---

The **DeleteWorksheetComment** API (`DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}`) removes a cell comment from a specified worksheet in an Excel file stored in the cloud, preserving the cell's content. Aspose.Cells Cloud provides robust support for this operation, enabling developers to programmatically clean up annotations using its REST API or SDKs for .NET, Java, Python, Node.js, and Go.

> **Page last updated:** May 15, 2024

## Overview

A **comment** is a text note attached to a specific cell in an Excel worksheet. The **Delete Worksheet Comment** operation removes the comment from the specified cell, leaving the cell content intact.

![Diagram: Excel cell with comment bubble being deleted via API call](/cells/images/Aspose-image-for-open-graph.jpg "Delete a worksheet comment using Aspose.Cells Cloud REST API")

For step-by-step instructions on obtaining and using a JWT token, see the [Authentication Guide](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## The Delete Worksheet Comment Web API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}
```

### Security and Authentication

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer" target="_blank">JWT token-based authentication</a>.

### Path Parameters

| Parameter Name | Type   | Path/Query String/HTTPBody | Description                                  |
| -------------- | ------ | -------------------------- | -------------------------------------------- |
| name           | String | Path                       | The file name.                               |
| sheetName      | String | Path                       | The worksheet name.                          |
| cellName       | String | Path                       | The cell name.                               |
| folder         | String | Query                      | The folder where the file is situated.       |
| storageName    | String | Query                      | The storage name where the file is situated. |

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

## How to Use the Delete Worksheet Comment API with SDKs?

### Delete Worksheet Comment API Specification

The <a href="https://reference.aspose.cloud/cells/#/Worksheets/DeleteWorksheetComment" rel="noopener noreferrer">Delete Worksheet Comment API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

### Request Example

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/SalesData.xlsx/worksheets/Q3_Results/comments/B5?folder=Docs&storageName=MyStorage" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9..."
```

**Success Response (200)**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetComment.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetComment.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetComment.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetComment.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetComment.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetComment.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetComment.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetComment.go" >}}
{{</tab>}}
{{< /tabs >}}
