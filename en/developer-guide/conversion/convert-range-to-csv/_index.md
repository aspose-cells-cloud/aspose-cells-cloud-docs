---
title: "Convert Range to CSV - Excel API"
second_title: "Aspose.Cells Cloud"
linktitle: "Convert Range to CSV"
type: docs
url: /convert-range-to-csv/
keywords: "Excel API, Convert Range to CSV, Cloud Conversion, Spreadsheet API, CSV Export, RESTful API, Aspose.Cells"
description: "Convert a specified range from a local spreadsheet file to a CSV format using the Excel API, ensuring seamless cloud execution."
weight: 100
kwords: Excel, Office Cloud, REST API, Spreadsheet, CSV, JSON, Markdown, Cloud Conversion, File Management, Excel Range
---

# **Excel API: ConvertRangeToCsv**

## **Overview**

This API allows you to convert a specified range from a local spreadsheet file into a CSV format.

## **Function Description**

The `ConvertRangeToCsv` method reads a spreadsheet file from the local file system, converts the specified range to a CSV file, and returns the conversion result. It's crucial to specify the source file path and target format correctly. Ensure that the necessary permissions are in place to access the source file and to write the converted file if applicable. The conversion process takes place entirely on the cloud server, removing the need for cloud storage or external downloads. If the source file is non-existent, inaccessible, or if any error occurs during the conversion process, an appropriate exception will be triggered. Supported formats for conversion are contingent on the available libraries and their capabilities.

## **API Endpoint**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/range/csv
```

## The request parameters of **convertRangeToCsv** API are

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
| :- | :- | :- |:- |
|Spreadsheet|File|FormData|Upload the spreadsheet file.|
|worksheet|String|Query|Name of the worksheet to be processed.|
|range|String|Query|Specify the cell area (e.g., A1:C10).|
|outPath|String|Query|(Optional) The folder path where the workbook will be stored. Default is null.|
|outStorageName|String|Query|Name of the output file storage.|
|fontsLocation|String|Query|Specify custom fonts if required.|
|region|String|Query|Defines the spreadsheet region setting.|
|password|String|Query|Password required to open the spreadsheet file.|

## **Response Structure**

```json
{
File
}
```

## Error Handling

- **400 Bad Request**: Invalid URL provided.
- **401 Unauthorized**: Authentication failed or no credentials were provided.
- **404 Not Found**: The source file is not accessible.
- **500 Server Error**: An anomaly occurred when obtaining conversion data from the spreadsheet.

## Usage Scenarios

## Key Features and Benefits

- **Cloud-Native Conversion**: Effortlessly convert local files directly in the cloud, negating the need for file storage.
- **Reduced Cloud Resource Burden**: No uploads required, conserving cloud storage capacity.
- **Simplified Workflow**: Directly convert local spreadsheets to CSV format using cloud services without intermediate steps.

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/ConversionController/ConvertRangeToCsv) outlines a publicly accessible API, enabling REST interactions directly from a web browser.

## Excel API SDK

Utilizing an SDK is the optimal approach to expedite development. SDKs manage low-level details, allowing you to concentrate on your project tasks. Explore the complete list of Aspose.Cells Cloud SDKs in our [GitHub repository](https://github.com/aspose-cells-cloud).

The following code examples illustrate how to call Aspose.Cells web services using various SDKs:
