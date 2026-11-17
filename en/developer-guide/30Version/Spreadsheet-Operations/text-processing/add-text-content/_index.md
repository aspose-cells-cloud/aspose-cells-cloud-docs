---
title: "Add Text to Excel: Efficiently Insert Data with Spreadsheet Web API"
second_title: "Developer Guide"
linktitle: "Add Text"
type: docs
url: /excel-add-text/
keywords: "Excel, Aspose.Cells, Add Text, Spreadsheet API, REST API, Office Cloud, Text Insertion, Excel API"
description: "Adds text to a specified location in an Excel spreadsheet via the Aspose.Cells Cloud API."
weight: 100
ArticleTitle: "Aspose.Cells Cloud: Add Text to Excel Cells via PostAddTextContent API"
---

The **PostAddTextContent** API (`POST https://api.aspose.cloud/v3.0/cells/addtext`) in Aspose.Cells Cloud v3.0 adds text content to a specified location within a spreadsheet document by accepting an `addTextOptions` object in the request body that defines both the text to insert and its insertion position, safely appending new text to specified cells with support for multiple insertion modes and format handling: it can prepend text to the beginning of selected cells to add common identifiers or labels such as product codes, categories, or prefixes while ensuring consistent data entry; insert characters before or after specific text to create structured and organized content; append identical text to the end of every selected cell in a single operation to simplify data entry and guarantee a uniform appearance; or insert text before or after a specified number of characters from the beginning or the end of each cell in the target range, which is typically useful for formatting codes, timestamps, or custom delimiters.

## The Post Add Text Content Web API

```http
POST https://api.aspose.cloud/v3.0/cells/addtext
```

### Security and Authentication

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type                 | Path/Query String/HTTPBody | Description                                                                      |
| -------------- | -------------------- | -------------------------- | -------------------------------------------------------------------------------- |
| addTextOptions | class:addtextoptions | HTTPBody                   | that specifies the text content and the position where the text should be added. |

### Response

```json
[
  {
    "Name": "FileInfo",
    "DataType": {
      "Identifier": "Class",
      "Reference": "FileInfo"
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
| 413  | Payload Too Large     | The uploaded file exceeds the allowed size limit.                        |
| 500  | Internal Server Error | The server encountered an unexpected error while processing the request. |

## How to Use the Post Add Text Content API with SDKs?

### Post Add Text Content API Specification

The <a href="https://reference.aspose.cloud/cells/#/TextProcessing/PostAddTextContent" rel="noopener noreferrer">Post Add Text Content API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

Using an SDK is the most efficient way to accelerate development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.
