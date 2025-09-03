---
title: "Export Spreadsheet as Format - Excel API"
second_title: "Aspose.Cells Cloud"
linktitle: "Export Spreadsheet as Format"
type: docs
url: /export-spreadsheet-as-format/
keywords: "Export spreadsheet, Cloud storage API, Convert spreadsheet, Spreadsheet formats, XLSX, PDF, CSV, JSON, Markdown"
description: "Efficiently converts spreadsheets stored in cloud storage to various formats like XLSX, PDF, and CSV."
weight: 100
kwords: "Excel, Office Cloud, REST API, Spreadsheet conversion, PDF, CSV, JSON, Markdown, Handle blank cells in Excel worksheets"
---

# **Excel API: ExportSpreadsheetAsFormat**

## **Overview**

This API allows for the conversion of spreadsheets stored in cloud storage to specified formats such as XLSX, PDF, and CSV without the need to download the files locally.

## **Function Description**

The `ExportSpreadsheetAsFormat` method directly processes a spreadsheet in cloud storage, converting it to the requested output format (e.g., XLSX, PDF, CSV). This eliminates the need to download the file, enhancing performance and reducing data transfer, especially for large files. The operation requires valid cloud storage credentials alongside an accessible file path or identifier. In case of errors such as file not found or access denied, suitable exceptions will be thrown. Supported output formats depend on the capabilities of the underlying cloud service.

## **API Endpoint**

```http
GET http://api.aspose.cloud/v4.0/cells/{name}
```

## The Request Parameters of **ExportSpreadsheetAsFormat** API are

| Parameter Name | Type | Path/Query String/HTTP Body | Description |
| :- | :- | :- |:- |
| name | String | Path | (Required) The name of the workbook file to be retrieved. |
| format | String | Query | (Required) The desired output format (e.g., "Xlsx", "Pdf", "Csv"). |
| folder | String | Query | (Optional) The folder path where the workbook is stored. The default is null. |
| storageName | String | Query | (Optional) The name of the storage if using custom cloud storage. Use default storage if omitted. |
| outPath | String | Query | (Optional) The folder path where the workbook will be stored. The default is null. |
| outStorageName | String | Query | Output file Storage Name. |
| fontsLocation | String | Query | Use custom fonts. |
| region | String | Query | The spreadsheet region setting. |
| password | String | Query | The password for opening the spreadsheet file. |

## **Response Structure**

```json
{
File
}
```

## **Error Handling**

- **400 Bad Request**: Invalid URL.
- **401 Unauthorized**: Authentication has failed, or no credentials were provided.
- **404 Not Found**: Source file not accessible.
- **500 Server Error**: An error occurred while processing the spreadsheet conversion.

## **Usage Scenarios**

## **Key Features and Benefits**

- **Cloud-Native Conversion**: Processes spreadsheets directly in cloud storage, eliminating local download steps.
- **Format Versatility**: Supports popular output formats (XLSX, PDF, CSV) for various applications such as editing and data sharing.
- **Simplified Workflow**: Facilitates direct conversion of cloud-stored spreadsheets, streamlining the user experience.

## **OpenAPI Specification**

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/ConversionController/ExportSpreadsheetAsFormat) provides a publicly accessible programming interface to perform REST interactions seamlessly.

## **Excel API SDK**

Using an SDK accelerates development by managing low-level operations, allowing you to concentrate on your project tasks. Visit the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples illustrate how to interact with Aspose.Cells web services via various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportSpreadsheetAsFormat.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportSpreadsheetAsFormat.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportSpreadsheetAsFormat.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportSpreadsheetAsFormat.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportSpreadsheetAsFormat.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportSpreadsheetAsFormat.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportSpreadsheetAsFormat.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportSpreadsheetAsFormat.go" >}}
{{</tab>}}
{{< /tabs >}}
