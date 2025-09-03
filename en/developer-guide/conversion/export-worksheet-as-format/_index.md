---
title: "Export Worksheet to Desired Format - Excel API"
second_title: "Aspose.Cells Cloud"
linktitle: "Export Worksheet"
type: docs
url: /export-worksheet-as-format/
keywords: "Export worksheet, Cloud storage conversion, File format transformation, API for spreadsheets"
description: "Efficiently converts a worksheet from cloud storage into various formats such as PDF, CSV, and images."
weight: 100
kwords: "Export worksheet, Cloud conversion, PDF, Image formats, Excel, REST API, CSV, JSON, Markdown, Handle blank cells in Excel"
---

# **Excel API : ExportWorksheetAsFormat**

## **Overview**

This API enables the conversion of a worksheet stored in cloud storage to a specified format, facilitating seamless integration and data sharing.

## **Function Description**

The `ExportWorksheetAsFormat` method processes a worksheet from cloud storage, converting it to the requested output format (PDF, or Image) without needing to download the file locally. It requires valid cloud storage credentials and an accessible file path or identifier. This remote conversion minimizes data transfer and enhances performance, especially with large files. If the source file is not found, access is denied, or an error occurs during conversion, an appropriate exception will be thrown. Supported output formats depend on the capabilities of the underlying cloud conversion service.

## **API Endpoint**

```http
GET http://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}
```

## The request parameters of **exportWorksheetAsFormat** API are

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
| :- | :- | :- |:- |
|name|String|Path|(Required) The name of the workbook file to be retrieved.|
|worksheet|String|Path|(Required) The specific worksheet to convert.|
|format|String|Query|(Required) The desired output format (e.g., "png", "pdf", "svg").|
|folder|String|Query|(Optional) The folder path where the workbook is stored. The default is null.|
|storageName|String|Query|(Optional) The name of the custom cloud storage. Use default storage if omitted.|
|outPath|String|Query|(Optional) The output folder path. The default is null.|
|outStorageName|String|Query|(Optional) Output file Storage Name.|
|fontsLocation|String|Query|(Optional) Specify custom fonts if needed.|
|region|String|Query|The spreadsheet region setting.|
|password|String|Query|The password for accessing the spreadsheet file.|

## **Response Structure**

```json
{
File
}
```

## Error Handling

- **400 Bad Request**: Invalid URL or parameters.
- **401 Unauthorized**: Authentication failed or no credentials provided.
- **404 Not Found**: The source file is inaccessible.
- **500 Server Error**: An anomaly occurred while obtaining conversion data from the spreadsheet.

## **Usage Scenarios**

## **Key Features and Benefits**

- **Cloud-Native Conversion**: Convert spreadsheets directly in cloud storage, eliminating the need for local file downloads.
- **Format Versatility**: Supports multiple output formats (PDF, CSV, Image) catering to various use cases (editing, sharing).
- **Streamlined Workflow**: Facilitates direct conversion from cloud-stored spreadsheets to required formats, enhancing efficiency.

## **OpenAPI Specification**

The [OpenAPI Specifiation](https://reference.aspose.cloud/cells/#/ConversionController/ExportWorksheetAsFormat) provides a publicly accessible programming interface for performing REST interactions directly from a web browser.

## **Excel API SDK**

Leveraging an SDK can significantly expedite development. An SDK handles low-level details, allowing you to focus on your project tasks. Explore the [GitHub repository](https://github.com/aspose-cells-cloud) for a comprehensive list of Aspose.Cells Cloud SDKs.

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportWorksheetAsFormat.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportWorksheetAsFormat.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportWorksheetAsFormat.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportWorksheetAsFormat.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportWorksheetAsFormat.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportWorksheetAsFormat.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportWorksheetAsFormat.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportWorksheetAsFormat.go" >}}
{{</tab>}}
{{< /tabs >}}
