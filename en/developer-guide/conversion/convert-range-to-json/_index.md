---
title: "Convert Range to JSON - Excel API"
second_title: "Aspose.Cells Cloud"
linktitle: "Convert Range to JSON"
type: docs
url: /convert-range-to-json/
keywords: "Convert range to JSON, JSON conversion, spreadsheet to JSON, Excel API, Aspose.Cells, cloud-based conversion, REST API"
description: "Efficiently converts a specified range of a spreadsheet on a local drive to a JSON file format."
weight: 100
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, JSON, Markdown, Convert range to JSON, Efficient data conversion
---

# **Excel API : Convert Range to JSON**

## **Overview**

Efficiently converts a specified range of a spreadsheet on a local drive to a JSON file format.

## **Function Description**

This method reads a spreadsheet file from the local file system, converts its range to the desired JSON file, and returns the converted result.
The source file path and target format must be specified correctly.
Ensure that the necessary permissions are in place to read the source file and write the converted file if applicable.
The conversion process occurs entirely on the cloud server, eliminating the need for any cloud storage or external downloads.
If the source file does not exist, is inaccessible, or if an error occurs during the conversion process, an appropriate exception will be thrown.
Supported formats for conversion depend on the available libraries and their capabilities.

## **API Endpoint**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/range/json
```

## The request parameters of **convertRangeToJson** API are

| Parameter Name     | Type  | Path/Query String/HTTP Body | Description                                      |
| ------------------ | ----- | ---------------------------- | ------------------------------------------------ |
| Spreadsheet        | File  | FormData                     | Upload the spreadsheet file.                     |
| worksheet          | String| Query                       | Name of the worksheet in the spreadsheet.       |
| range              | String| Query                       | Cell area to convert, e.g., A1:C10.             |
| outPath            | String| Query                       | (Optional) Folder path where the workbook is stored; default is null. |
| outStorageName     | String| Query                       | Name of the output file storage.                 |
| fontsLocation      | String| Query                       | Custom fonts usage.                              |
| region             | String| Query                       | The spreadsheet region setting.                  |
| password           | String| Query                       | Password for opening the spreadsheet file.       |

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
- **500 Server Error**: An anomaly occurred while obtaining conversion data for the spreadsheet.

## **Usage Scenarios**

## **Key Features and Benefits**

- **Cloud-Native Conversion**: Seamlessly convert local files directly in the cloud, without the need for storage.
- **Reduced Resource Burden**: Avoid uploading files to the cloud, saving on cloud storage costs.
- **Streamlined Workflow**: Easily convert local spreadsheets to JSON format through cloud services, eliminating unnecessary steps.

## **OpenAPI Specification**

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/ConversionController/ConvertRangeToJson) defines a publicly accessible programming interface and allows you to carry out REST interactions directly from a web browser.

## **Excel API SDK**

Utilizing an SDK is the optimal way to accelerate development. An SDK manages low-level details, enabling you to concentrate on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a comprehensive list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:
