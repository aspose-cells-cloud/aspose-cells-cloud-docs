---
title: "Convert Range to HTML - Excel API"
second_title: "Aspose.Cells Cloud"
linktitle: "Convert Range to HTML"
type: docs
url: /convert-range-to-html/
keywords: "Excel API, Convert Range to HTML, Spreadsheet Conversion, HTML File Generation, Cloud API, Document Conversion"
description: "Effortlessly converts a specified range of a spreadsheet on your local drive to an HTML file using the Aspose.Cells API."
weight: 100
kwords: "Excel, Office Cloud, REST API, Spreadsheet, HTML, PDF, CSV, JSON, Markdown, Match Blank Cells, Data Conversion"
---

# **Excel API: ConvertRangeToHtml**

## **Overview**

This API allows you to convert a specified range of a spreadsheet from your local drive directly to an HTML file.

## **Function Description**

The `ConvertRangeToHtml` method reads a specified range from a spreadsheet file located on the local file system, converts it to the desired HTML format, and returns the converted result. Ensure that the source file path and target format are specified correctly. You must have the necessary permissions to read the source file and write the converted file, if applicable. The conversion process occurs entirely on the cloud server, which means there is no need for cloud storage or external downloads. If the source file is missing, inaccessible, or if an error arises during the conversion process, the API will throw an appropriate exception. Supported formats for conversion depend on the available libraries and their capabilities.

## **API Endpoint**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/range/html
```

## The request parameters of **convertRangeToHtml** API are

| Parameter Name   | Type   | Path/Query String/HTTP Body | Description                                           |
|------------------|--------|------------------------------|-------------------------------------------------------|
| Spreadsheet      | File   | FormData                     | Upload the spreadsheet file.                          |
| worksheet        | String | Query                        | Name of the worksheet within the spreadsheet.        |
| range            | String | Query                        | The cell area to convert, e.g., A1:C10.              |
| outPath          | String | Query                        | (Optional) The folder path where the workbook is stored. Default is null. |
| outStorageName   | String | Query                        | Name of the output file storage.                      |
| fontsLocation     | String | Query                        | Specify custom fonts to use.                          |
| region           | String | Query                        | The spreadsheet region setting.                        |
| password         | String | Query                        | Password for opening the spreadsheet file.            |

## **Response Structure**

```json
{
File
}
```

## **Error Handling**

- **400 Bad Request**: Invalid URL.
- **401 Unauthorized**: Authentication failed or no credentials were provided.
- **404 Not Found**: Source file not accessible.
- **500 Server Error**: An anomaly occurred while obtaining conversion data for the spreadsheet.

## **Usage Scenarios**

## **Key Features and Benefits**

- **Cloud-Native Conversion**: Convert local files directly in the cloud, eliminating the need for cloud storage.
- **Resource Efficiency**: No requirement to upload files to the cloud, saving valuable storage space.
- **Streamlined Workflow**: Easily convert local spreadsheets to HTML format directly through cloud services without any intermediate steps.

## **OpenAPI Specification**

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/ConversionController/ConvertRangeToHtml) provides a publicly accessible programming interface, enabling you to carry out REST interactions directly from a web browser.

## **Excel API SDK**

Utilizing an SDK is the most efficient way to accelerate development. An SDK handles low-level details, allowing you to concentrate on your project objectives. Please visit the [GitHub repository](https://github.com/aspose-cells-cloud) for a comprehensive list of Aspose.Cells Cloud SDKs.

The following code examples illustrate how to interact with Aspose.Cells web services using various SDKs:
