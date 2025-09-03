---
title: "Convert Table to CSV - Excel API"
second_title: "Aspose.Cells Cloud"
linktitle: "Convert Table to CSV"
type: docs
url: /convert-table-to-csv/
keywords: "table to csv, convert spreadsheet to csv, Excel to CSV conversion, CSV file generation, cloud-based file conversion"
description: "Efficiently converts a table from a spreadsheet on your local drive to a CSV file using our API."
weight: 100
kwords: "Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, JSON, Markdown, Match all blank cells in an Excel worksheet, Table to CSV, Local to Cloud Conversion"
---

# **Excel API: Convert Table to CSV**

## **Overview**

This API converts a table from a spreadsheet located on your local drive into a CSV file, facilitating easy data handling and import/export tasks.

## **Function Description**

The `convertTableToCsv` method reads a specified spreadsheet file from the local file system, converts its table into the desired CSV format, and returns the resulting CSV file. Ensure that the source file path and target format are specified correctly. Adequate permissions must be granted to read the source file and write the converted file as necessary. The conversion occurs entirely on the cloud server, negating the need for any cloud storage or external downloads. If the source file is missing, inaccessible, or if an error arises during conversion, an appropriate exception will be raised. Supported conversion formats are contingent on the capabilities of the available libraries.

## **API Endpoint**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/table/csv
```

## The request parameters of **convertTableToCsv** API are

| Parameter Name   | Type  | Path/Query String/HTTP Body | Description                                     |
|-------------------|-------|------------------------------|-------------------------------------------------|
| Spreadsheet       | File  | FormData                     | Upload the spreadsheet file.                    |
| worksheet         | String| Query                        | Name of the worksheet in the spreadsheet.       |
| tableName         | String| Query                        | Name of the table to be converted.              |
| outPath           | String| Query                        | (Optional) Folder path where the workbook is stored; defaults to null. |
| outStorageName    | String| Query                        | Name of the output file storage.                |
| fontsLocation     | String| Query                        | Path for using custom fonts.                     |
| region            | String| Query                        | Defines the spreadsheet region setting.         |
| password          | String| Query                        | Password for opening the spreadsheet file.      |

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
- **500 Server Error**: An anomaly occurred in obtaining conversion data from the spreadsheet.

## **Usage Scenarios**

## **Key Features and Benefits**

- **Cloud-Native Conversion**: Perform conversion of local files directly in the cloud, eliminating the need for file storage.
- **Reduced Cloud Resource Burden**: No requirement to upload files to the cloud, conserving cloud storage space.
- **Simplified Workflow**: Effortlessly convert local spreadsheets to CSV format directly through cloud services, minimizing intermediate steps.

## **OpenAPI Specification**

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/ConversionController/ConvertTableToCsv) provides a publicly accessible programming interface, allowing REST interactions directly from a web browser.

## **Excel API SDK**

Utilizing an SDK significantly accelerates development. An SDK handles low-level details, allowing you to focus on your project tasks. For a complete list of Aspose.Cells Cloud SDKs, please visit the [GitHub repository](https://github.com/aspose-cells-cloud).

The following code examples illustrate how to make calls to Aspose.Cells web services using various SDKs:
