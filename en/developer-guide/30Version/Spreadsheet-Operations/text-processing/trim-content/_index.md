---
title: "Trim content: Fix Excel Spaces & Line Breaks"
second_title: "Document"
linktitle: "Trim Content"
type: docs
url: /spreadsheet-trim-content/
keywords: "Excel, PostTrimContent, Trim Content, Aspose.Cells Cloud, REST API, Spreadsheet Data Cleaning"
description: "The PostTrimContent API trims extra spaces, line breaks, and other unnecessary characters from cells within a specified range in an Excel worksheet, helping to clean and standardize spreadsheet data."
weight: 100
---

# **Excel API : PostTrimContent**

The **PostTrimContent** API processes and trims content within a specified range in a spreadsheet. It removes extra spaces, line breaks, and other unnecessary characters from the content of selected cells, making it useful for cleaning data entries and ensuring consistent spreadsheet formatting.

## **Interface Details**

### **Endpoint**

```
POST http://api.aspose.cloud/v3.0/cells/trimcontent
```

### **Function Description**

- **Efficiency** – Trims content only within the designated range, saving time and resources by avoiding unnecessary operations on the entire worksheet.  
- **Flexibility** – Allows users to define the exact cell range to be processed, accommodating various data sets and requirements.  
- **Data Integrity** – Removes extra spaces and line breaks, helping maintain consistent and reliable data for analysis and reporting.  
- **Ease of Use** – Simple integration with minimal setup, suitable for both developers and end‑users.

### Request Parameters of **postTrimContent** API

| Parameter Name      | Type  | Location | Description                                   |
|---------------------|-------|----------|-----------------------------------------------|
| trimContentOptions  | Class | Body     | Options that specify how the content should be trimmed (e.g., target range, trim mode). |

### **Response Description**

```json
{
  "Filename": "xxxxxx.pdf",
  "FileSize": xxxx,
  "FileContent": "File Content: base64_encoded_string"
}
```

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/TextProcessingController/PostTrimContent) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

## Excel API SDK

Using an SDK is the best way to speed up development. An SDK handles low‑level details, allowing you to focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_PostTrimContent.cs" >}}
{{</ tab>}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_PostTrimContent.java" >}}
{{</ tab>}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_PostTrimContent.php" >}}
{{</ tab>}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_PostTrimContent.rb" >}}
{{</ tab>}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_PostTrimContent.ts" >}}
{{</ tab>}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_PostTrimContent.py" >}}
{{</ tab>}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_PostTrimContent.pl" >}}
{{</ tab>}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_PostTrimContent.go" >}}
{{</ tab>}}
{{< /tabs >}}