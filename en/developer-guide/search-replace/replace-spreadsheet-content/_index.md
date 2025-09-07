---
title: "Replace Spreadsheet Content - Excel API"
second_title: "Aspose.Cells Cloud"
linktitle: "Replace Spreadsheet Content"
type: docs
url: /replace-spreadsheet-content/
keywords: "Excel API, Spreadsheet manipulation, Replace text, Office Cloud integration, REST API"
description: "Efficiently replace text in local spreadsheet files using Aspose.Cells API."
weight: 100
kwords: "Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, JSON, Markdown, Replace text in Excel, Match blank cells in Excel worksheet"
---

# **Excel API: ReplaceSpreadsheetContent**

Efficiently replace specified text within local spreadsheet files.

## **Interface Details**

### **Endpoint**

```
PUT http://api.aspose.cloud/v4.0/cells/replace/content
```

### **Function Description**

This method allows users to replace specified text within a local spreadsheet file across all sheets and cells of the workbook. The operation is performed in the cloud without requiring cloud storage. Ensure you have the necessary permissions to read from and write to the source file. If the source file cannot be accessed, writing to the file fails, or an error occurs during the replacement process (such as an unsupported file format), an appropriate exception will be thrown. Depending on the implementation, the method may return the number of replacements made or the locations of the replaced texts (e.g., sheet name, cell coordinates). Users should specify the exact text to replace and its replacement to ensure accurate modifications.

### The request parameters of **replaceSpreadsheetContent** API are

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
| :- | :- | :- |:- |
| Spreadsheet | File | FormData | Upload the spreadsheet file. |
| searchText | String | Query | The text to search for. |
| replaceText | String | Query | The text to replace with. |
| worksheet | String | Query | Specify the worksheet for the replacement. |
| cellArea | String | Query | Specify the cell area for the replacement. |
| region | String | Query | The spreadsheet region setting. |
| password | String | Query | The password for opening the spreadsheet file. |

### **Response Description**

```json
[
    {
        "Name": "ResponseFile",
        "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
        }
    }
]
```

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/SearchControllor/ReplaceSpreadsheetContent) defines a publicly accessible programming interface, allowing you to perform REST interactions directly from a web browser.

## Excel API SDK

Using an SDK is the best way to accelerate development. An SDK manages low-level details, allowing you to focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to interact with Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ReplaceTextInLocalFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ReplaceTextInLocalFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ReplaceTextInLocalFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ReplaceTextInLocalFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ReplaceTextInLocalFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ReplaceTextInLocalFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ReplaceTextInLocalFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ReplaceTextInLocalFile.go" >}}
{{</tab>}}
{{< /tabs >}}
