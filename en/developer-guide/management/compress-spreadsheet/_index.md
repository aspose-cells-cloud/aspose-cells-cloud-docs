---
title: "Aspose.Cells Cloud Web API - Compress the size of the Spreadsheet."
second_title: "Document"
ArticleTitle: "Compress the size of the Spreadsheet"
linktitle: "Compress Spreadsheet"
type: docs
url: /compress-spreadsheet/
keywords: "Spreadsheet Compression, Reduce File Size, Aspose.Cells Cloud Web API"
description: "The Compress Spreadsheet API allows users to efficiently reduce the file size of spreadsheets by applying specified compression levels, optimizing storage, and enhancing performance."
weight: 100
kwords: "Excel, Office Cloud, REST, Spreadsheet Compression, File Size Optimization, PDF, CSV, Json, Markdown"
---

Compress the size of the spreadsheet.

## **Compress Spreadsheet API**

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/compress
```

### **Request Parameters:**

| Parameter Name | Type | Path/Query String/HTTP Body | Description |
| :- | :- | :- |:- |
|Spreadsheet|File|FormData|Upload the spreadsheet file to be compressed.|
|level|Integer|Query|Specifies the compression level to be applied, ranging from 0 (no compression) to 9 (maximum compression).|
|outPath|String|Query|(Optional) The folder path where the compressed workbook will be stored. Default is null.|
|outStorageName|String|Query|Output file storage name.|
|region|String|Query|The spreadsheet region setting.|
|password|String|Query|The password required to open the spreadsheet file.|

### **Response**

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

### Error Codes

- **400 Bad Request**: Invalid Aspose.Cells Cloud API URI.
- **401 Unauthorized**: Invalid access token. Or invalid client id and secret.
- **404 Not Found**: The spreadsheet file not accessible.
- **500 Server Error**: The spreadsheet has encountered an anomaly in obtaining calculation data.

## Where should we use the Compress Spreadsheet API?

When you need to reducing the size of spreadsheets, you can use this API.

## Why should you use the Compress Spreadsheet API?

- The spreadsheet is too large and needs to reduce the file size.
- Development can be quickly completed through the existing SDK.

## How to Use the Compress Spreadsheet API with SDKs

### Compress Spreadsheet API Specification

The [Compress Spreadsheet API Specification](https://reference.aspose.cloud/cells/#/ManagementController/CompressSpreadsheet) provides a publicly accessible interface for REST interactions, allowing direct API calls from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low-level details, allowing you to compress the spreadsheet size with short code.
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to interact with Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CompressSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CompressSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CompressSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CompressSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CompressSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CompressSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CompressSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CompressSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}
