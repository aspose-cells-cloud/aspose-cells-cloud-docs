---
title: "Aspose.Cells Cloud Web API - Convert Spreadsheet"
second_title: "Aspose.Cells Cloud"
ArticleTitle: "Convert Spreadsheet"
linktitle: "Convert Spreadsheet"
type: docs
url: /convert-spreadsheet/
keywords: "spreadsheet conversion, convert spreadsheet, cloud conversion, REST API, XLSX, PDF, CSV, JSON, Markdown, convert local files"
description: "Effortlessly converts a spreadsheet from a local drive to various specified formats using the Excel API."
weight: 100
kwords: Excel, Office Cloud, REST API, Spreadsheet Conversion, PDF, CSV, JSON, Markdown, Match all blank cells in an Excel worksheet
---

Convert a local spreadsheet/Excel file to other format file with the Aspose.Cells Cloud Web API.

## **Convert Spreadsheet API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/spreadsheet
```

### **Request Parameters:**

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
| :- | :- | :- |:- |
|Spreadsheet|File|FormData|Upload the spreadsheet file to be converted.|
|format|String|Query|(Required) The desired output format (e.g., "Xlsx", "Pdf", "Csv").|
|outPath|String|Query|(Optional) The folder path where the converted workbook will be stored. The default is null.|
|outStorageName|String|Query|Specify an output file storage name.|
|fontsLocation|String|Query|Use custom fonts for the spreadsheet.|
|region|String|Query|Specify the spreadsheet region setting.|
|password|String|Query|The password for opening the spreadsheet file if it is protected.|

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

## Why should you use the Convert Range to Pdf API?

- No need for cloud storage, reducing the burden on cloud resources.
- Development can be quickly completed through the existing SDK.

## How to Use the Convert Range to Html API with SDKs?

### OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/ConversionController/ConvertSpreadsheet) defines a publicly accessible programming interface, allowing you to perform REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the best way to accelerate development. The SDK handles the underlying details, allowing you to simply implement convert spreadsheet/Excel to other format for cells with minimal code.
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to invoke Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertWorkbook.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertWorkbook.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertWorkbook.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertWorkbook.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertWorkbook.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertWorkbook.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertWorkbook.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertWorkbook.go" >}}
{{</tab>}}
{{< /tabs >}}
