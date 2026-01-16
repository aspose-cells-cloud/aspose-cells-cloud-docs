---
title: "Update Word Case"
second_title: "Document"
linktitle: "Word Case"
type: docs
url: /post-update-word-case/
keywords: "Excel, Google Sheets, CSV, Text Case Conversion, REST API, Aspose.Cells Cloud"
description: "Automate text case conversion in Excel, Google Sheets, and CSV files using the Aspose.Cells Cloud PostUpdateWordCase API for clean, standardized data."
weight: 100
---

# **Excel API : PostUpdateWordCase**

Managing inconsistent text case in spreadsheets (Excel, Google Sheets, CSV) can be frustrating, especially with large datasets. The PostUpdateWordCase WEB API solves this by automating text‑case conversions, ensuring clean and standardized data with minimal effort.

## **Interface Details**

### **Endpoint**

```
POST http://api.aspose.cloud/v3.0/cells/updatewordcase
```

### **Function Description**

The PostUpdateWordCase WEB API is a powerful tool designed to address the common issue of inconsistent text case in spreadsheets, which can significantly impact data analysis and processing. This API automates case conversion, ensuring that your data is clean, standardized, and ready for further manipulation or analysis.

- **Automated Text‑Case Conversion**  
  - **Uppercase to Lowercase** – Convert all uppercase letters to lowercase.  
  - **Lowercase to Uppercase** – Convert all lowercase letters to uppercase.  
  - **Capitalize First Letter** – Capitalize the first letter of each word.  
  - **Title Case** – Convert text to title case, where the first letter of each major word is capitalized.

- **Support for Multiple Formats** – The API works with a wide range of spreadsheet formats, including Excel, OpenOffice, JSON, CSV, and others. This versatility makes it suitable for various data‑processing needs.

### Request Parameters of **postUpdateWordCase** API

| Parameter Name   | Type   | Location      | Description |
|------------------|--------|---------------|-------------|
| `wordCaseOptions`| object | Request body  | Options that define the desired case transformation, such as the source range, target case type, and additional settings. |

### **Response Description**

```json
{
  "Filename": "xxxxxx.pdf",
  "FileSize": xxxx,
  "FileContent": "File Content: base64_encoded_string"
}
```

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/TextProcessingController/PostUpdateWordCase) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

## Excel API SDK

Using an SDK is the best way to speed up development. An SDK handles low‑level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
 {{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_PostUpdateWordCase.cs" >}}
{{</ tab>}}
{{< tab tabNum="2" >}}
 {{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_PostUpdateWordCase.java" >}}
{{</ tab>}}
{{< tab tabNum="3" >}}
 {{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_PostUpdateWordCase.php" >}}
{{</ tab>}}
{{< tab tabNum="4" >}}
 {{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_PostUpdateWordCase.rb" >}}
{{</ tab>}}
{{< tab tabNum="5" >}}
 {{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_PostUpdateWordCase.ts" >}}
{{</ tab>}}
{{< tab tabNum="6" >}}
 {{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_PostUpdateWordCase.py" >}}
{{</ tab>}}
{{< tab tabNum="7" >}}
 {{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_PostUpdateWordCase.pl" >}}
{{</ tab>}}
{{< tab tabNum="8" >}}
 {{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_PostUpdateWordCase.go" >}}
{{</ tab>}}
{{</ tabs >}}
