---
title: "Add Text to Excel: Efficiently Insert Data with Spreadsheet WEB API"
second_title: "Aspose.Cells Cloud Document"
linktitle: "Add Text"
type: docs
url: /excel-add-text/
keywords: ""
description: "Adds text content to a specified location within a spreadsheet. It requires an object that defines the text to be added and the insertion location. "
weight: 100
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdown, Match all blank cells in an Excel worksheet
---

# **Excel API : PostAddTextContent**

Adds text content to a specified location within a spreadsheet. It requires an object that defines the text to be added and the insertion location.

## **Interface Details**

### **Endpoint**

```
POST http://api.aspose.cloud/v3.0/cells/addtext
```

### **Function Description**

This method safely appends new text to specified content, supporting multiple insertion modes and format handling.Supports multiple insertion modes:

- **Add text to the beginning of selected cells**:
  Prepend text to all selected cells, ensuring consistency in your data entry.This option is perfect for adding common identifiers or labels to a column of data, such as product codes, categories, or prefixes.
- **Insert characters before or after specific text**:
  Tailor your data presentation by placing characters before or after specified text in the selected cells. This allows you to create structured and organized content with ease.
- **Append same text to the end of every selected cell**:
  Add the same text to the end of multiple cells in one go. This simplifies data entry and ensures a uniform appearance throughout your document.
- **Insert text before or after a specified number of characters**:
  Precision meets convenience as you add certain text after a specified number of characters from the beginning or from the end of every cell in the target range.Typical use cases include:

### The request parameters of **postAddTextContent** API are

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
| :- | :- | :- |:- |
|addTextOptions|Class|Body|that specifies the text content and the position where the text should be added.|

### **Response Description**

```json
{
  "Filename": "xxxxxx.pdf",
  "FileSize": xxxx,
  "FileContent": "File Content: base64_encoded_string"
}
```

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/TextProcessingController/PostAddTextContent) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

## Excel API SDK

Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

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
