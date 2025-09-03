---
title: "Export Table to Specified Format"
second_title: "Aspose.Cells Cloud"
linktitle: "Export Table to Specified Format"
type: docs
url: /export-table-as-format/
keywords: "Cloud Storage, Spreadsheet Conversion, API Integration, Export Table, REST API, PDF, CSV, Excel, JSON, Markdown, Cloud-Native Solutions"
description: "Efficiently converts tables from spreadsheets in cloud storage to various specified formats."
weight: 100
kwords: "Spreadsheet Conversion, Cloud Storage, API Integration, PDF, CSV, Excel, JSON, Markdown, Export Table, Cloud-Native Solutions"
---

# **Excel API : ExportTableAsFormat**

## **Overview**

Efficiently converts tables from spreadsheets in cloud storage to various specified formats.

## **Function Description**

This method processes a table of spreadsheet directly in cloud storage, converting it to the requested output format (PDF, or Image format) without requiring the file to be downloaded to the local machine. The operation relies on valid cloud storage credentials and an accessible file path or identifier. The conversion is performed remotely, reducing data transfer and improving performance for large files. If the source file is not found, access is denied, or an error occurs during conversion, an appropriate exception will be thrown. Supported output formats are determined by the capabilities of the underlying cloud conversion service.

## **API Endpoint**

```http
GET http://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/tables/{tableName}
```

## The request parameters of **exportTableAsFormat** API are

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
| :- | :- | :- |:- |
|name|String|Path|(Required) The name of the workbook file to be retrieved.|
|worksheet|String|Path|Name of the worksheet.|
|tableName|String|Path|Name of the table.|
|format|String|Query|(Required) The desired format (e.g., "png", "pdf", "svg").|
|folder|String|Query|(Optional) The folder path where the workbook is stored. The default is null.|
|storageName|String|Query|(Optional) The name of the storage if using custom cloud storage. Use default storage if omitted.|
|outPath|String|Query|(Optional) The folder path for output storage. The default is null.|
|outStorageName|String|Query|Name of the output file storage.|
|fontsLocation|String|Query|Location for custom fonts.|
|region|String|Query|Setting for spreadsheet region.|
|password|String|Query|Password for opening the spreadsheet file.|

## **Response Structure**

```json
{
File
}
```

## Error Handling

- **400 Bad Request**: Invalid URL.
- **401 Unauthorized**: Authentication has failed, or no credentials were provided.
- **404 Not Found**: Source file not accessible.
- **500 Server Error**: An anomaly occurred while obtaining conversion data.

## **Usage Scenarios**

## **Key Features and Benefits**

- **Cloud-Native Conversion**: Processes spreadsheets directly in cloud storage, eliminating the need to download files to local machines.
- **Format Versatility**: Supports common output formats (XLSX, PDF, CSV) to meet diverse use cases (e.g., editing, sharing, data import).
- **Simplified Workflow**: Directly converts cloud-stored spreadsheets to needed formats without intermediate steps.

## **OpenAPI Specification**

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/ConversionController/ExportTableAsFormat) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

## **Excel API SDK**

Using an SDK is the best way to speed up development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportTableAsFormat.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportTableAsFormat.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportTableAsFormat.php" >}}
{{</tab>}}
{{<tab tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportTableAsFormat.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportTableAsFormat.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportTableAsFormat.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportTableAsFormat.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportTableAsFormat.go" >}}
{{</tab>}}
{{< /tabs >}}
