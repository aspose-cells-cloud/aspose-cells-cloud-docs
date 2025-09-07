---
title: "Aspose.Cells Cloud Web API - Convert Spreadsheet Range to Image"
second_title: "Aspose.Cells Cloud"
ArticleTitle: "Converting Spreadsheet Range to Image"
linktitle: "Convert Range to Image"
type: docs
url: /convert-range-to-image/
keywords: "Excel API, Convert Range to Image, Spreadsheet to Image, Cloud Conversion, Image Formats, Aspose.Cells"
description: "Easily convert a range of a spreadsheet on your local drive to an image file using the Excel API with cloud-native technology."
weight: 100
kwords: Excel, Office Cloud, REST API, Spreadsheet, Image Conversion, PNG, SVG, TIFF, JSON, Markdown, Match all blank cells in an Excel worksheet
---

Convert a range from a local spreadsheet/Excel file to an image file with the Aspose.Cells Cloud Web API.

**IMAGE FORMATS:** [PNG](https://docs.fileformat.com/image/png/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/)

## **Convert Range to Image API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/range/image
```

### **Request Parameters:**

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
| :- | :- | :- |:- |
|Spreadsheet|File|FormData|Upload the spreadsheet file for conversion.|
|worksheet|String|Query|The worksheet name of Spreadsheet/Excel|
|range|String|Query|Define the cell area to convert (e.g., A1:C10).|
|format|String|Query|Specify the output file format (e.g., png, svg, tiff).|
|printHeadings|Boolean|Query|Indicate if row and column headings should be printed.|
|outPath|String|Query|(Optional) The folder path where the workbook is stored; default is null.|
|outStorageName|String|Query|Name of the output file storage.|
|fontsLocation|String|Query|Custom fonts to use for the conversion.|
|regoin|String|Query|Define the spreadsheet region setting.|
|password|String|Query|Password for opening the spreadsheet file if protected.|

### **Response**

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

## Why should you use the Convert Range to Image API?

- No need for cloud storage, reducing the burden on cloud resources.
- Development can be quickly completed through the existing SDK.

## How to Use the Convert Range to Html API with SDKs?

### OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/ConversionController/ConvertRangeToImage) provides a publicly accessible programming interface, enabling REST interactions directly from your web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the best way to accelerate development. The SDK handles the underlying details, allowing you to simply implement convert spreadsheet/Excel chart to image for cells with minimal code.
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples illustrate how to call Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToImage.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToImage.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToImage.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToImage.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToImage.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToImage.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToImage.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToImage.go" >}}
{{</tab>}}
{{< /tabs >}}
