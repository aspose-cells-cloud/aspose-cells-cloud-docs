---
title: "Export Range as Format - Excel API"
second_title: "Aspose.Cells Cloud"
linktitle: "Export Range as Format"
type: docs
url: /export-range-as-format/
keywords: "Excel API, Export range, Cloud storage, Spreadsheet conversion, REST API, PDF, CSV, JSON, Markdown, Excel worksheet, cloud-native conversion, format versatility"
description: "Convert a specified range of a spreadsheet in cloud storage to various formats such as PDF, CSV, or image formats without downloading the file."
weight: 100
kwords: Excel API, Cloud storage, Spreadsheet conversion, REST API, PDF, CSV, JSON, Markdown, Excel worksheet
---

# **Excel API: ExportRangeAsFormat**

## **Overview**

This API method converts a specified range of a spreadsheet stored in cloud storage to the desired format.

## **Function Description**

The `ExportRangeAsFormat` method processes a designated range of a spreadsheet directly in cloud storage, converting it to the requested output format (PDF, PNG, etc.) without requiring the file to be downloaded to a local machine. This operation necessitates valid cloud storage credentials and an accessible file path or identifier. By performing the conversion remotely, it minimizes data transfer and enhances performance, especially for large files. If the source file is missing, access is denied, or if an error occurs during conversion, an appropriate exception will be raised. Supported output formats depend on the capabilities of the underlying cloud conversion service.

## **API Endpoint**

```http
GET http://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{range}
```

## The request parameters of **ExportRangeAsFormat** API are

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
| :- | :- | :- |:- |
|name|String|Path|(Required) The name of the workbook file to be retrieved.|
|worksheet|String|Path|The The worksheet name of Spreadsheet/Excel|
|range|String|Path|The range to be converted (e.g., A1:C12).|
|format|String|Query|(Required) The desired output format (e.g., "png", "pdf", "svg").|
|folder|String|Query|(Optional) The folder path where the workbook is stored. Defaults to null.|
|storageName|String|Query|(Optional) The name of the storage if using custom cloud storage. Defaults to default storage if omitted.|
|outPath|String|Query|(Optional) The folder path for the output file. Defaults to null.|
|outStorageName|String|Query|The name of the output file storage.|
|fontsLocation|String|Query|Custom fonts location.|
|region|String|Query|The region setting of the spreadsheet.|
|password|String|Query|The password required to open the spreadsheet file.|

## **Response Structure**

```json
{
File
}
```

## Error Handling

- **400 Bad Request**: Invalid URL.
- **401 Unauthorized**: Authentication failed, or no credentials were provided.
- **404 Not Found**: The source file is not accessible.
- **500 Server Error**: An anomaly occurred while obtaining conversion data.

## Usage Scenarios

## Key Features and Benefits

- **Cloud-Native Conversion**: Processes spreadsheets directly in cloud storage, eliminating the need for local downloads.
- **Format Versatility**: Supports a range of output formats (XLSX, PDF, CSV) to cater to various use cases (editing, sharing, importing data).
- **Simplified Workflow**: Facilitates direct conversion of cloud-stored spreadsheets to the desired formats without intermediate steps.

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/ConversionController/ExportRangeAsFormat) provides a publicly accessible programming interface, enabling REST interactions directly from a web browser.

## Excel API SDK

Utilizing an SDK is the most efficient method to accelerate development. An SDK manages low-level details, allowing you to focus on your project objectives. Please visit the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportRangeAsFormat.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportRangeAsFormat.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportRangeAsFormat.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportRangeAsFormat.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportRangeAsFormat.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportRangeAsFormat.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportRangeAsFormat.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportRangeAsFormat.go" >}}
{{</tab>}}
{{< /tabs >}}
