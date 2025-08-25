---
title: "Convert worksheet to image"
second_title: "Developer Guide"
linktitle: "Convert worksheet to image"
type: docs
url: /convert-worksheet-to-image/
keywords: ""
description: "Converts a worksheet of spreadsheet on a local drive to the image format. "
weight: 100
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdown, Match all blank cells in an Excel worksheet
---

# **Excel API : ConvertWorksheetToImage**

## **Overview**

Converts a worksheet of spreadsheet on a local drive to the image format. 

## **Function Description**

This method reads a spreadsheet file from the local file system, converts it's worksheet to the desired image format (e.g., svg, png, ...), and returns the converted result. 
The source file path and target format must be specified correctly. 
Ensure that the necessary permissions are in place to read the source file and write the converted file if applicable. 
The conversion process occurs entirely on the cloud server, eliminating the need for any cloud storage or external downloads. 
If the source file does not exist, is inaccessible, or if an error occurs during the conversion process, an appropriate exception will be thrown. 
Supported formats for conversion depend on the available libraries and their capabilities.


## **API Endpoint** 

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/worksheet/image
```

## The request parameters of **convertWorksheetToImage** API are: 

| Parameter Name | Type | Path/Query String/HTTPBody | Description | 
| :- | :- | :- |:- | 
|Spreadsheet|File|FormData|Upload spreadsheet file.|
|worksheet|String|Query|worksheet name of spreadsheet.|
|format|String|Query|image format:svg, png, and so on.|
|outPath|String|Query|(Optional) The folder path where the workbook is stored. The default is null.|
|outStorageName|String|Query|Output file Storage Name.|
|fontsLocation|String|Query|Use Custom fonts.|
|regoin|String|Query|The spreadsheet region setting.|
|password|String|Query|The password for opening spreadsheet file.|


## **Response Structure**

```json
{
File
}
```

## Error Handling

- **400 Bad Request**: Invalid url.
- **401 Unauthorized**:  Authentication has failed, or no credentials were provided.
- **404 Not Found**: Source file not accessible.
- **500 Server Error** The spreadsheet has encountered an anomaly in obtaining conversion data.


## Usage Scenarios
## Key Features and Benefits

- **Cloud-Native Conversion**: Conversion of local files directly in the cloud, eliminating the need to store them there.
- **Reduced Cloud Resource Burden**: No need to upload files to the cloud, saving cloud storage space.
- **Format Versatility**: Supports common output image formats (png, svg, tiff and so on).
- **Simplified Workflow**: Convert local spreadsheets to the desired format directly through cloud services, without intermediate steps.

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/ConversionController/ConvertWorksheetToImage) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

## Excel API SDK 

Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:


{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertWorksheetToSvg.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertWorksheetToSvg.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertWorksheetToSvg.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertWorksheetToSvg.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertWorksheetToSvg.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertWorksheetToSvg.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertWorksheetToSvg.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertWorksheetToSvg.go" >}}
{{</tab>}}
{{< /tabs >}}


