---
title: "Convert Range to Image - Excel API"
second_title: "Aspose.Cells Cloud"
linktitle: "Convert Range to Image"
type: docs
url: /convert-range-to-image/
keywords: "Excel API, Convert Range to Image, Spreadsheet to Image, Cloud Conversion, Image Formats, Aspose.Cells"
description: "Easily convert a range of a spreadsheet on your local drive to an image file using the Excel API with cloud-native technology."
weight: 100
kwords: Excel, Office Cloud, REST API, Spreadsheet, Image Conversion, PNG, SVG, TIFF, JSON, Markdown, Match all blank cells in an Excel worksheet
---

# **Excel API: ConvertRangeToImage**

## **Overview**

This API allows you to convert a specified range of a spreadsheet on your local drive into an image file.

## **Function Description**

This method reads a spreadsheet file from the local file system, converts the specified range to the desired image format, and returns the converted result.
Ensure that the source file path and target format are specified correctly, and that you have the necessary permissions to read the source file and write the converted file if applicable.
The conversion process occurs entirely on the cloud server, eliminating the need for any cloud storage or external downloads.
If the source file does not exist, is inaccessible, or if an error occurs during the conversion process, an appropriate exception will be thrown.
Supported formats for conversion depend on the available libraries and their capabilities.

## **API Endpoint**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/range/image
```

## The request parameters of **convertRangeToImage** API are

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

## **Response Structure**

```json
{
File
}
```

## Error Handling

- **400 Bad Request**: Invalid URL or parameters.
- **401 Unauthorized**: Authentication failed or no credentials provided.
- **404 Not Found**: The source file is not accessible.
- **500 Server Error**: An error occurred while processing the conversion.

## Usage Scenarios

## Key Features and Benefits

- **Cloud-Native Conversion**: Convert local files directly in the cloud, avoiding the need to store them there.
- **Reduced Cloud Resource Burden**: No need to upload files to the cloud, saving valuable storage space.
- **Simplified Workflow**: Seamlessly convert local spreadsheets to image formats via cloud services without intermediate steps.

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/ConversionController/ConvertRangeToImage) provides a publicly accessible programming interface, enabling REST interactions directly from your web browser.

## Excel API SDK

Utilizing an SDK is the most efficient way to expedite development. An SDK manages low-level details, allowing you to focus on your project tasks. Visit the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

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
