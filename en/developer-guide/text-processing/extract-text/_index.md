---
title: "Aspose.Cells Cloud Web API – Extract Text"
second_title: "Aspose.Cells Cloud – Online Short‑Code"
linktitle: "Extract Text"
type: docs
url: /extract-text/
keywords: "Aspose.Cells Cloud, Extract Text, Excel API, cell text extraction, REST API"
description: "Extract substrings, numbers or characters from Excel cells using Aspose.Cells Cloud API. Supports before/after text, position‑based extraction, and direct output to a new range."
weight: 100
---

Extracts substrings, characters, or numbers from a spreadsheet cell into another cell, eliminating the need for complex FIND, MIN, LEFT, or RIGHT formulas.

## **ExtractText API**

```http
PUT http://api.aspose.cloud/v4.0/cells/content/extract/text
```

### The request parameters of **extractText** API are

| Parameter Name   | Type    | Location           | Description                                                                                                                     |
| ---------------- | ------- | ------------------ | ------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet      | File    | FormData           | Upload the spreadsheet file.                                                                                                    |
| extractTextType  | String  | Query              | Enum indicating the extraction mode. Allowed values: `Before`, `After`, `BeforePosition`, `AfterPosition`.                      |
| beforeText       | String  | Query              | Text that must appear **before** the extracted substring. Used when `extractTextType=Before`.                                   |
| afterText        | String  | Query              | Text that must appear **after** the extracted substring. Used when `extractTextType=After`.                                     |
| beforePosition   | Integer | Query              | Number of characters to return from the left side of the cell. Used when `extractTextType=BeforePosition`.                      |
| afterPosition    | Integer | Query              | Number of characters to return from the right side of the cell. Used when `extractTextType=AfterPosition`.                      |
| outPositionRange | String  | Query              | The target range (e.g., `Sheet1!A1`) where the extracted text will be written.                                                  |
| worksheet        | String  | Query              | Name of the worksheet that contains the source cell.                                                                            |
| range            | String  | Query              | The source cell or range (e.g., `A1`).                                                                                          |
| outPath          | String  | Query _(Optional)_ | Folder path in the storage where the resulting workbook will be saved. If omitted, the result is returned in the response body. |
| outStorageName   | String  | Query              | Name of the storage to use for the output file.                                                                                 |
| region           | String  | Query              | Spreadsheet region setting (e.g., `US`, `EU`).                                                                                  |
| password         | String  | Query              | Password for opening a protected workbook.                                                                                      |

### **Response**

When the request succeeds, the API returns a JSON payload containing the extracted text and the address of the cell where it was written:

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

If the `outPath` parameter is provided, the response contains only a status message; the workbook is written to the specified location.

### Error Codes

- **400 Bad Request** – Invalid Aspose.Cells Cloud API URI or missing required parameters.
- **401 Unauthorized** – Invalid access token, client ID, or client secret.
- **404 Not Found** – The specified spreadsheet file cannot be accessed.
- **500 Server Error** – An unexpected error occurred while processing the workbook.

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/TextProcessingController/ExtractText) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the best way to accelerate development. The SDK handles the underlying details, allowing you to simply implement **Extract Text** for cells with minimal code. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples illustrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{<tab tabNum="1" >}}

```csharp
// C# example – extract text (code omitted for brevity)
```

{{</tab>}}

{{<tab tabNum="2" >}}

```java
// Java example – extract text (code omitted for brevity)
```

{{</tab>}}

{{<tab tabNum="3" >}}

```php
// PHP example – extract text (code omitted for brevity)
```

{{</tab>}}

{{<tab tabNum="4" >}}

```ruby
# Ruby example – extract text (code omitted for brevity)
```

{{</tab>}}

{{<tab tabNum="5" >}}

```javascript
// Node.js example – extract text (code omitted for brevity)
```

{{</tab>}}

{{<tab tabNum="6" >}}

```python
# Python example – extract text (code omitted for brevity)
```

{{</tab>}}

{{<tab tabNum="7" >}}

```perl
# Perl example – extract text (code omitted for brevity)
```

{{</tab>}}

{{<tab tabNum="8" >}}

```go
// Go example – extract text (code omitted for brevity)
```

{{</tab>}}

{{< /tabs >}}
