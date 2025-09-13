---
title: "Aspose.Cells Cloud Web API - Convert a Spreadsheet Chart to an Image"
second_title: "Aspose.Cells Cloud Document"
ArticleTitle: "Convert a Spreadsheet Chart to an Image"
linktitle: "Convert Chart to Image"
type: docs
url: /convert-chart-to-image/
keywords: "convert chart to image, png, svg, tiff, jpg, bmp, convert a Spreadsheet chart to png,convert an Excel chart to svg, convert an Excel chart to jpg, convert a Spreadsheet chart to bmp, convert an Excel chart to tiff"
description: "Convert a chart from a local spreadsheet/Excel file to an image file with the Aspose.Cells Cloud Web API."
weight: 100
kwords: "convert an Excel chart to image, png, svg, tiff, jpg, bmp, Spreadsheet"
---

Convert a chart from a local spreadsheet/Excel file to an image format file. Supported **IMAGE FORMATS:** [PNG](https://docs.fileformat.com/image/png/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/)

## **Convert Chart to Image API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/chart/image
```

### **Request Parameters:**

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
| :- | :- | :- |:- |
|Spreadsheet|File|FormData|Upload the spreadsheet file containing the chart.|
|worksheet|String|Query|Specify the worksheet name if applicable.|
|chartIndex|Integer|Query|Index of the chart to convert.|
|format|String|Query|(Required) The desired image type (e.g., svg, png, jpg).|
|outPath|String|Query|(Optional) The folder path where the workbook is stored; defaults to null.|
|outStorageName|String|Query|Name of the storage for the output file.|
|fontsLocation|String|Query|Specify custom fonts if needed.|
|region|String|Query|Set the spreadsheet region.|
|password|String|Query|The password for opening the spreadsheet file.|

## **Response**

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

## Where should you use the Convert Chart to Image API?

- Export the charts in the spreadsheet as images.

## Why should you use the Convert Chart to Image API?

- No need for cloud storage, reducing the burden on cloud resources.
- Development can be quickly completed through the existing SDK.

## How to Use the Convert Chart to Image API with SDKs?

### Convert Chart to Image API Specification

The [Convert Chart to Image API Specification](https://reference.aspose.cloud/cells/#/ConversionController/ConvertChartToImage) defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low-level details, allowing you to convert a chart to an image with short code.
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertChartToImage.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertChartToImage.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertChartToImage.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertChartToImage.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertChartToImage.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertChartToImage.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertChartToImage.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertChartToImage.go" >}}
{{</tab>}}
{{< /tabs >}}
