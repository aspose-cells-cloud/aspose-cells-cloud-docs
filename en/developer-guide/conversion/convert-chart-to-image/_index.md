---
title: "Convert Chart to Image - Excel API"
second_title: "Aspose.Cells Cloud"
linktitle: "Convert Chart to Image"
type: docs
url: /convert-chart-to-image/
keywords: "convert chart to image, Excel API, chart image conversion, Aspose.Cells, REST API, cloud conversion, spreadsheet to image"
description: "Convert a chart from a spreadsheet on your local drive to an image format using the Aspose.Cells REST API."
weight: 100
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdown, Match all blank cells in an Excel worksheet, chart image conversion, Aspose.Cells
---

# **Aspose.Cells API: Convert Chart to Image**

## **Overview**

Convert a chart from a spreadsheet on your local drive to an image format seamlessly with the Aspose.Cells API.

## **Function Description**

This method reads a chart from a spreadsheet file located on the local file system, converts it into the desired image format (e.g., PNG, SVG, TIFF), and returns the converted result.
The source file path and target format must be specified accurately.
Ensure that the necessary permissions are in place to read the source file and write the converted file, if applicable.
The conversion process occurs entirely on the cloud server, eliminating the need for any cloud storage or external downloads.
If the source file does not exist, is inaccessible, or if an error occurs during the conversion process, an appropriate exception will be thrown.
Supported formats for conversion depend on the available libraries and their capabilities.

## **API Endpoint**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/chart/image
```

## The request parameters of **convertChartToImage** API are

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

## **Response Structure**

```json
{
File
}
```

## Error Handling

- **400 Bad Request**: Invalid URL.
- **401 Unauthorized**: Authentication has failed, or no credentials were provided.
- **404 Not Found**: The source file is not accessible.
- **500 Server Error**: An anomaly occurred while obtaining conversion data from the spreadsheet.

## Usage Scenarios

## Key Features and Benefits

- **Cloud-Native Conversion**: Convert local files directly in the cloud, eliminating the need for local storage.
- **Reduced Cloud Resource Burden**: Avoid the need to upload files to the cloud, saving cloud storage space.
- **Simplified Workflow**: Effortlessly convert local spreadsheets to image formats directly through cloud services, without intermediate steps.

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/ConversionController/ConvertChartToImage) defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

## Excel API SDK

Using an SDK is the most efficient way to accelerate development. An SDK handles low-level details, allowing you to focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a comprehensive list of Aspose.Cells Cloud SDKs.

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
