---
title: "Convert Table to Image - Excel API"
second_title: "Aspose.Cells Cloud"
linktitle: "Convert Table to Image"
type: docs
url: /convert-table-to-image/
keywords: "table to image, Excel API, cloud conversion, spreadsheet to image, image formats"
description: "Convert a local spreadsheet table into an image file efficiently using the Excel API."
weight: 100
kwords: "Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, JSON, Markdown, convert table to image, cloud-native conversion, image file formats, spreadsheet conversion"
---

# **Excel API: Convert Table to Image**

## **Overview**

This API method allows you to convert a table from a spreadsheet located on your local drive into an image file seamlessly.

## **Function Description**

The `convertTableToImage` method reads a specified spreadsheet file from the local file system, converts the designated table into the desired image format, and returns the resulting image. Ensure that the source file path and target format are specified accurately. It is crucial to have the correct permissions to read the source file and write the converted image if necessary. The entire conversion process is handled on the cloud server, which means there is no requirement for cloud storage or external downloads. If the source file is not found, inaccessible, or if any errors occur during the conversion, an appropriate exception will be raised. Supported output formats for conversion depend on the libraries available.

## **API Endpoint**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/table/image
```

## The request parameters of **convertTableToImage** API are

| Parameter Name | Type | Path/Query String/HTTP Body | Description |
| :- | :- | :- |:- |
|Spreadsheet|File|FormData|Upload the spreadsheet file.|
|worksheet|String|Query|Specify the worksheet name within the spreadsheet.|
|tableName|String|Query|Name of the table to convert.|
|format|String|Query|Desired image file format (e.g., png, svg).|
|outPath|String|Query|(Optional) The folder path where the converted image will be stored. Defaults to null.|
|outStorageName|String|Query|Specify the output file storage name.|
|fontsLocation|String|Query|Use custom fonts if required.|
|region|String|Query|Defines the spreadsheet region settings.|
|password|String|Query|Password required to access the spreadsheet file.|

## **Response Structure**

```json
{
File
}
```

## Error Handling

- **400 Bad Request**: Invalid URL provided.
- **401 Unauthorized**: Authentication failed, or no credentials provided.
- **404 Not Found**: The source file is inaccessible.
- **500 Server Error**: An error occurred during data conversion.

## Usage Scenarios

## Key Features and Benefits

- **Cloud-Native Conversion**: Convert local spreadsheet files directly in the cloud, without the need for local storage.
- **Reduced Cloud Resource Burden**: Save cloud storage space by avoiding unnecessary uploads.
- **Format Versatility**: Supports multiple output image formats including png, svg, tiff, and more.
- **Simplified Workflow**: Streamline the process of converting spreadsheets to image formats via cloud services, bypassing intermediate steps.

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/ConversionController/ConvertTableToImage) provides a publicly accessible programming interface for conducting REST interactions directly from a web browser.

## Excel API SDK

Utilizing an SDK is the most efficient way to accelerate development. An SDK manages low-level details, allowing you to concentrate on your project objectives. Please visit the [GitHub repository](https://github.com/aspose-cells-cloud) for an extensive list of Aspose.Cells Cloud SDKs.

The following code examples illustrate how to invoke Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToSvg.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToSvg.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToSvg.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToSvg.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToSvg.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToSvg.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToSvg.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToSvg.go" >}}
{{</tab>}}
{{< /tabs >}}
