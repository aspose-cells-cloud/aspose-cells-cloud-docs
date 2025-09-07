---
title: "Aspose.Cells Cloud WEb API - Split Spreadsheet"
second_title: "Aspose.Cells Cloud"
ArticleTitle: "Split Spreadsheets into multiple files"
linktitle: "Split Spreadsheet"
type: docs
url: /split-spreadsheet/
keywords: "Excel API, Split Spreadsheet, Spreadsheet Management, Cloud Processing, File Formats, REST API, XLSX, CSV, PDF, JSON, Markdown"
description: "Efficiently split a local spreadsheet into multiple files in various formats without requiring cloud storage."
weight: 100
kwords: "Excel API, Office Cloud, REST API, Spreadsheet, PDF, CSV, JSON, Markdown, Split Local Spreadsheet, Cloud Processing, File Management, Error Handling"
---

Split a spreadsheet stored into multiple files. Support 30+ outfile formats.

## **Split Spreadsheet API**

```http
PUT http://api.aspose.cloud/v4.0/cells/split/spreadsheet
```

### **Request Parameters:**

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
| :- | :- | :- |:- |
| Spreadsheet | File | FormData | Upload the spreadsheet file to be split. |
| from | Integer | Query | Specify the beginning worksheet index. |
| to | Integer | Query | Specify the ending worksheet index. |
| outFormat | String | Query | Define the output file format. |
| outPath | String | Query | (Optional) The folder path for storing the output workbook. Defaults to null. |
| outStorageName | String | Query | Define the output file storage name. |
| fontsLocation | String | Query | Specify custom fonts if required. |
| regoin | String | Query | Set the spreadsheet region. |
| password | String | Query | Provide the password for accessing the spreadsheet file. |

## **Response**

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

### Error Codes

- **400 Bad Request**: Invalid Apose.Cells Cloud API URI.
- **401 Unauthorized**: Invalid access token. Or invalid client id and secret.
- **404 Not Found**: The spreadsheet file not accessible.
- **500 Server Error**: The spreadsheet has encountered an anomaly in obtaining calculation data.

## Where should we use the Split Remote Spreadsheet API?

When you need to split a spreadsheet to more files, you can use this API.

## Why should you use the Split Remote Spreadsheet API?

- No need for cloud storage space, just split directly.
- Development can be quickly completed through the existing SDK.

## How to Use the Split Remote Spreadsheet API with SDKs

### OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/DataProcessingController/SplitSpreadsheet) provides a publicly accessible programming interface for performing REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the best way to accelerate development. The SDK handles the underlying details, allowing you to simply implement split spreadsheets for cells with minimal code.
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples illustrate how to invoke Aspose.Cells web services using different SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SplitLocalFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SplitLocalFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SplitLocalFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SplitLocalFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SplitLocalFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SplitLocalFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SplitLocalFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SplitLocalFile.go" >}}
{{</tab>}}
{{< /tabs >}}
