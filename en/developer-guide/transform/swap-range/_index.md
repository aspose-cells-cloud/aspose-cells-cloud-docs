---
title: "Aspose.Cells Cloud Web API - Swap Range in Spreadsheet"
second_title: "Aspose.Cells Cloud Document"
ArticleTitle: "Swap Range Data in a Spreadsheet"
linktitle: "Swap Range"
type: docs
url: /swap-range/
keywords: "Aspose.Cells Cloud Web API, Swap Ranges, Office Cloud, REST"
description: "The Swap Ranges for Excel API provides a powerful tool to interchange any two columns, rows, ranges, or individual cells within an Excel file. This API allows users to efficiently rearrange their tables, ensuring that the original data formatting is preserved and all existing formulas continue to function correctly. By leveraging this API, users can streamline their data manipulation tasks and maintain the integrity of their spreadsheets."
weight: 100
kwords: Excel, Office Cloud, REST, PDF, CSV, Json, Markdown
---

Exchange data between any two columns, rows, ranges, or individual cells in an Excel file.

## **Swap Range API**

```http
PUT http://api.aspose.cloud/v4.0/cells/swap/range
```

### **Request Parameters:**

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
| :- | :- | :- |:- |
|Spreadsheet|File|FormData|Upload the spreadsheet file.|
|worksheet1|String|Query|Specify the worksheet that is the source of the exchange data area.|
|range1|String|Query|Specify the source for the exchange data.|
|worksheet2|String|Query|Specify the worksheet that is the target of the exchange data area.|
|range2|String|Query|Specify the target for the exchange data.|
|outPath|String|Query|(Optional) The folder path where the workbook is stored. The default is null.|
|outStorageName|String|Query|Output file Storage Name.|
|region|String|Query|The spreadsheet region setting.|
|password|String|Query|The password for opening the spreadsheet file.|

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

- **400 Bad Request**: Invalid Apose.Cells Cloud API URI.
- **401 Unauthorized**: Invalid access token. Or invalid client id and secret.
- **404 Not Found**: The spreadsheet file not accessible.
- **500 Server Error**: The spreadsheet has encountered an anomaly in obtaining calculation data.

## Where should we use the Swap Range API?

When you need to swap range data in a spreadsheet, you can use this API.

## Why should you use the Swap Range API?

- Quickly swap range data in an Excel spreadsheet.
- Development can be quickly completed through the existing SDK.

## How to Use the Swap Range API with SDKs

### Swap Range API Specification

The [Swap Range API Specification](https://reference.aspose.cloud/cells/#/TransformController/SwapRange) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low-level details, allowing you to swap range with short code.
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SwapRange.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SwapRange.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SwapRange.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SwapRange.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SwapRange.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SwapRange.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SwapRange.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SwapRange.go" >}}
{{</tab>}}
{{< /tabs >}}
