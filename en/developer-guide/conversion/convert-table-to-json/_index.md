---
title: "Convert Table to JSON - Excel API"
second_title: "Aspose.Cells Cloud"
linktitle: "Convert Table to JSON"
type: docs
url: /convert-table-to-json/
keywords: "Excel API, JSON conversion, spreadsheet to JSON, cloud file conversion, REST API, Aspose.Cells"
description: "Convert a local spreadsheet table to JSON format efficiently using the Excel API. This method enables seamless file processing without the need for cloud storage."
weight: 100
kwords: "Excel API, JSON conversion, cloud file conversion, spreadsheet, REST API, Aspose.Cells, local drive processing, file format conversion"
---

# **Excel API: ConvertTableToJson**

## **Overview**

The ConvertTableToJson method converts a table from a local spreadsheet into a JSON file format. Designed for efficiency and ease of use, this API allows users to process files directly without requiring cloud storage.

## **Function Description**

This method reads a specified spreadsheet file from the local file system, converts its table into JSON format, and returns the result. Users must accurately specify the source file path and target format. Proper permissions are required to read the source file and write the converted output. The entire conversion process is executed on the cloud server, eliminating the need for external downloads or cloud storage. In the event of an inaccessible source file or conversion error, the method will throw an appropriate exception. Supported formats for conversion are contingent on the capabilities of the available libraries.

## **API Endpoint**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/table/json
```

## The request parameters of **convertTableToJson** API are

| Parameter Name    | Type  | Path/Query String/HTTP Body | Description                                        |
|-------------------|-------|-----------------------------|----------------------------------------------------|
| Spreadsheet       | File  | FormData                    | Upload the spreadsheet file.                       |
| worksheet         | String| Query                       | Specify the worksheet name of the spreadsheet.     |
| tableName         | String| Query                       | Provide the name of the table to convert.          |
| outPath           | String| Query                       | (Optional) The folder path where the workbook is stored; defaults to null. |
| outStorageName    | String| Query                       | Specify the output file storage name.              |
| fontsLocation     | String| Query                       | Use custom fonts for conversion.                   |
| region            | String| Query                       | Define the region settings for the spreadsheet.    |
| password          | String| Query                       | The password required to open the spreadsheet file. |

## **Response Structure**

```json
{
File
}
```

## Error Handling

- **400 Bad Request**: Invalid URL or parameters.
- **401 Unauthorized**: Authentication failed or no credentials provided.
- **404 Not Found**: The specified source file is not accessible.
- **500 Server Error**: An error occurred while obtaining conversion data from the spreadsheet.

## Usage Scenarios

## Key Features and Benefits

- **Cloud-Native Conversion**: Directly convert local files in the cloud without needing to store them there.
- **Reduced Cloud Resource Burden**: Avoid uploading files to save cloud storage space while processing.
- **Simplified Workflow**: Convert local spreadsheets to JSON format seamlessly through cloud services, eliminating unnecessary intermediate steps.

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/ConversionController/ConvertTableToJson) provides a publicly accessible programming interface, enabling REST interactions directly from a web browser.

## Excel API SDK

Utilizing an SDK accelerates development by managing low-level details, allowing you to concentrate on your project tasks. For a complete list of Aspose.Cells Cloud SDKs, please check the [GitHub repository](https://github.com/aspose-cells-cloud).

The following code examples demonstrate how to interact with Aspose.Cells web services using various SDKs:
