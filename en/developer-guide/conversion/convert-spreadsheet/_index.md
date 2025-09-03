---
title: "Convert Spreadsheet - Excel API"
second_title: "Aspose.Cells Cloud"
linktitle: "Convert Spreadsheet"
type: docs
url: /convert-spreadsheet/
keywords: "spreadsheet conversion, Excel API, cloud conversion, REST API, XLSX, PDF, CSV, JSON, Markdown, convert local files"
description: "Effortlessly converts a spreadsheet from a local drive to various specified formats using the Excel API."
weight: 100
kwords: Excel, Office Cloud, REST API, Spreadsheet Conversion, PDF, CSV, JSON, Markdown, Match all blank cells in an Excel worksheet
---

# **Excel API : Convert Spreadsheet**

## **Overview**

This API converts a spreadsheet located on a local drive into the specified output format, including XLSX, PDF, and CSV.

## **Function Description**

The `ConvertSpreadsheet` method reads a spreadsheet file from the local file system and converts it into the desired output format (e.g., XLSX, PDF, CSV). The source file path and target format must be specified correctly. Ensure that the necessary permissions are in place to read the source file and write the converted file if applicable. The conversion process is performed entirely on the cloud server, eliminating the need for any external cloud storage or downloads. If the source file is inaccessible or an error occurs during the conversion process, an appropriate exception will be thrown. Supported formats for conversion depend on the available libraries and their capabilities.

## **API Endpoint**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/spreadsheet
```

## The request parameters of **convertSpreadsheet** API are

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
| :- | :- | :- |:- |
|Spreadsheet|File|FormData|Upload the spreadsheet file to be converted.|
|format|String|Query|(Required) The desired output format (e.g., "Xlsx", "Pdf", "Csv").|
|outPath|String|Query|(Optional) The folder path where the converted workbook will be stored. The default is null.|
|outStorageName|String|Query|Specify an output file storage name.|
|fontsLocation|String|Query|Use custom fonts for the spreadsheet.|
|region|String|Query|Specify the spreadsheet region setting.|
|password|String|Query|The password for opening the spreadsheet file if it is protected.|

## **Response Structure**

```json
{
File
}
```

## Error Handling

- **400 Bad Request**: Invalid URL or request parameters.
- **401 Unauthorized**: Authentication has failed, or no credentials were provided.
- **404 Not Found**: Source file not accessible or does not exist.
- **500 Server Error**: An anomaly occurred during the spreadsheet conversion process.

## Usage Scenarios

## Key Features and Benefits

- **Cloud-Native Conversion**: Convert local files directly in the cloud, reducing the need for intermediate storage.
- **Resource Efficiency**: Save cloud storage space as files do not need to be uploaded.
- **Format Versatility**: Supports multiple output formats including XLSX, PDF, and CSV.
- **Streamlined Workflow**: Convert local spreadsheets directly through cloud services without unnecessary steps.

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/ConversionController/ConvertSpreadsheet) defines a publicly accessible programming interface, allowing you to perform REST interactions directly from a web browser.

## Excel API SDK

Using an SDK accelerates the development process. An SDK manages low-level details, allowing you to focus on your project tasks. Please check the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

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
