---
title: "Trim content: Fix Excel Spaces & Line Breaks"
second_title: "Aspose.Cells Cloud Document"
linktitle: "Trim Content"
type: docs
url: /spreadsheet-trim-content/ 
keywords: ""
description: "The PostTrimContent API is designed to process and trim content within a specified range in a spreadsheet. This API allows users to remove extra spaces, line breaks, or other unnecessary characters from the content of selected cells. It is particularly useful for cleaning up data entries and ensuring consistency in spreadsheet formatting "
weight: 100
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdown, Match all blank cells in an Excel worksheet
---

# **Excel API : PostTrimContent**

The PostTrimContent API is designed to process and trim content within a specified range in a spreadsheet. This API allows users to remove extra spaces, line breaks, or other unnecessary characters from the content of selected cells. It is particularly useful for cleaning up data entries and ensuring consistency in spreadsheet formatting

## **Interface Details**

### **Endpoint**

```
POST http://api.aspose.cloud/v3.0/cells/trimcontent
```

### **Function Description**

Efficiency: The API efficiently trims content within the specified range, ensuring that only the designated cells are processed. This targeted approach saves time and resources by avoiding unnecessary operations on the entire worksheet.Flexibility: Users can define the exact range of cells to be processed, providing flexibility in handling different data sets and requirements.Data Integrity: By removing extra spaces and line breaks, the API helps maintain data integrity and consistency, which is crucial for accurate data analysis and reporting.Ease of Use: The API is easy to integrate into existing workflows and can be used with minimal setup, making it accessible for both developers and end-users

### The request parameters of **postTrimContent** API are

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
| :- | :- | :- |:- |
|trimContentOptions|Class|Body||

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

Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_PostTrimContent.cs" >}}
{{</ tab>}}
{{<tab tabNum="2" >}}
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
