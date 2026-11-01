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
The **PostAddTextContent** API (`POST https://api.aspose.cloud/v3.0/cells/addtext`) in Aspose.Cells Cloud v3.0 adds text content to a specified location within a spreadsheet document by accepting an `addTextOptions` object in the request body that defines both the text to insert and its insertion position, supporting flexible modes such as prepending labels to cells, appending uniform suffixes, or inserting text before/after a fixed character count.

## The Post Add Text Content Web API

```http
POST https://api.aspose.cloud/v3.0/cells/addtext
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### **Request Parameter**

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| addTextOptions | class:addtextoptions | HTTPBody | that specifies the text content and the position where the text should be added. |

### **Response**

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

| Code | Meaning | Description |
|---|---|---|
| 200 | OK | The request completed successfully. |
| 400 | Bad Request | The request is malformed or one or more parameters are invalid. |
| 401 | Unauthorized | Authentication failed, or the JWT token is missing or expired. |
| 404 | Not Found | The requested workbook, worksheet, or resource was not found. |
| 413 | Payload Too Large | The uploaded file exceeds the allowed size limit. |
| 500 | Internal Server Error | The server encountered an unexpected error while processing the request. |

### **Function Description**

This method safely appends new text to specified cells, supporting multiple insertion modes and format handling.

- **Add text to the beginning of selected cells**  
  Prepends text to all selected cells, ensuring consistency in your data entry. Ideal for adding common identifiers or labels such as product codes, categories, or prefixes.

- **Insert characters before or after specific text**  
  Places characters before or after the target text in the selected cells, allowing you to create structured and organized content easily.

- **Append the same text to the end of every selected cell**  
  Adds identical text to the end of multiple cells in one operation, simplifying data entry and guaranteeing a uniform appearance.

- **Insert text before or after a specified number of characters**  
  Inserts text after a defined number of characters from the beginning or the end of each cell in the target range. Typical use cases include formatting codes, timestamps, or custom delimiters.

## How to Use the PostAddTextContent API with SDKs

### PostAddTextContent API Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/TextProcessingController/PostAddTextContent) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using an SDK is the most efficient way to accelerate development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_PostAddTextContent.cs" >}}
{{</ tab>}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_PostAddTextContent.java" >}}
{{</ tab>}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_PostAddTextContent.php" >}}
{{</ tab>}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_PostAddTextContent.rb" >}}
{{</ tab>}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_PostAddTextContent.ts" >}}
{{</ tab>}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_PostAddTextContent.py" >}}
{{</ tab>}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_PostAddTextContent.pl" >}}
{{</ tab>}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_PostAddTextContent.go" >}}
{{</ tab>}}
{{< /tabs >}}
