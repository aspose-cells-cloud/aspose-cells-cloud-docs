---
title: "Convert Table to HTML - Excel API"
second_title: "Aspose.Cells Cloud"
linktitle: "Convert Table to HTML"
type: docs
url: /convert-table-to-html/
keywords: "Excel to HTML, Spreadsheet Conversion, HTML Generation, Cloud API, REST API, Convert Excel to HTML, Table to HTML, Document Conversion, Cloud Services"
description: "Easily convert tables from local spreadsheet files into HTML format using our cloud-based API."
weight: 100
kwords: "Excel, Office Cloud, REST API, Spreadsheet, HTML, PDF, CSV, JSON, Markdown, Match blank cells in Excel"
---

# **Excel API: ConvertTableToHtml**

## **Overview**

This API enables the conversion of tables from spreadsheet files on your local drive into HTML format.

## **Function Description**

The `ConvertTableToHtml` method reads a specified spreadsheet file from the local file system, converts its table into the desired HTML file format, and returns the converted result. Ensure that the source file path and target format are specified correctly. Proper permissions must be granted to read the source file and write the converted file, if applicable. The entire conversion process occurs securely on our cloud server, eliminating the need for any cloud storage or external downloads. If the source file does not exist, is inaccessible, or if an error occurs during the conversion process, an appropriate exception will be thrown. Supported formats for conversion are contingent on the capabilities of the libraries in use.

## **API Endpoint**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/table/html
```

## The request parameters of **convertTableToHtml** API are

| Parameter Name | Type | Path/Query String/HTTP Body | Description |
| :- | :- | :- | :- |
| Spreadsheet | File | FormData | Upload the spreadsheet file to be converted. |
| worksheet | String | Query | The name of the worksheet within the spreadsheet. |
| tableName | String | Query | The name of the table to convert. |
| outPath | String | Query | (Optional) The folder path where the converted file will be stored. The default value is null. |
| outStorageName | String | Query | The designated storage name for the output file. |
| fontsLocation | String | Query | Specify custom fonts for the conversion. |
| region | String | Query | Define the spreadsheet region settings. |
| password | String | Query | The password required to access the spreadsheet file. |

## **Response Structure**

```json
{
File
}
```

## Error Handling

- **400 Bad Request**: The request URL is invalid.
- **401 Unauthorized**: Authentication has failed, or no credentials were provided.
- **404 Not Found**: The source file is not accessible.
- **500 Server Error**: An anomaly has occurred while obtaining conversion data from the spreadsheet.

## Usage Scenarios

## Key Features and Benefits

- **Cloud-Native Conversion**: Convert local files directly in the cloud, removing the necessity to store them there.
- **Reduced Cloud Resource Burden**: By converting files without uploading them, you save on cloud storage space.
- **Simplified Workflow**: Seamlessly convert local spreadsheets to HTML format via our cloud services, avoiding unnecessary intermediate steps.

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/ConversionController/ConvertTableToHtml) outlines a publicly accessible programming interface, allowing you to perform REST interactions directly from your web browser.

## Excel API SDK

Utilizing an SDK is the most efficient way to expedite development. An SDK manages low-level details, allowing you to concentrate on your project tasks. Please visit the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of available Aspose.Cells Cloud SDKs.

The following code examples illustrate how to interact with Aspose.Cells web services using various SDKs:
