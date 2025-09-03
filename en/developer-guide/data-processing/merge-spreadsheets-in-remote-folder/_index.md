---
title: "Merge Spreadsheets in Remote Folder - Excel API"
second_title: "Aspose.Cells Cloud"
linktitle: "Merge Spreadsheets in Remote Folder"
type: docs
url: /merge-spreadsheets-in-remote-folder/
keywords: "Merge spreadsheets, cloud storage, Excel API, remote processing, spreadsheet formats, REST API"
description: "Seamlessly merge spreadsheet files stored in cloud storage into specified output formats like XLSX, CSV, and PDF."
weight: 100
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, JSON, Markdown, Merge spreadsheets, Cloud processing, Remote file handling
---

# **Excel API: MergeSpreadsheetsInRemoteFolder**

## **Overview**

This API allows you to merge spreadsheet files located in a cloud storage folder into a specified output format file, such as XLSX, CSV, or PDF.

## **Function Description**

The `MergeSpreadsheetsInRemoteFolder` method combines multiple spreadsheet files stored in cloud storage into a single output file in the desired format.
This operation is executed remotely, eliminating the need to download files to your local machine.
Ensure that valid cloud storage credentials and accessible file paths or identifiers are provided for all input files.
The merging process is performed entirely within the cloud environment, which minimizes data transfer and boosts performance.
In cases where source files cannot be accessed or if an error occurs during the merge or conversion process, an appropriate exception will be raised.
The supported output formats are dependent on the capabilities of the cloud processing service used.

## **API Endpoint**

```http
PUT http://api.aspose.cloud/v4.0/cells/merge/remote-spreadsheets
```

## The request parameters of **MergeSpreadsheetsInRemoteFolder** API are

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
| :- | :- | :- |:- |
| folder | String | Query | The folder where the merged files will be stored.|
| fileMatchExpression | String | Query | Expression to match files for merging. |
| outFormat | String | Query | The desired output file format. |
| mergeInOneSheet | Boolean | Query | Indicates whether to combine all data into a single worksheet. |
| storageName | String | Query | (Optional) The name of the custom cloud storage; defaults to default storage if omitted. |
| outPath | String | Query | (Optional) The folder path for storing the workbook; defaults to null. |
| outStorageName | String | Query | The name of the storage for the output file. |
| fontsLocation | String | Query | Specifies custom fonts. |
| region | String | Query | Sets the spreadsheet region. |
| password | String | Query | The password for opening the spreadsheet file. |

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
- **500 Server Error**: An anomaly occurred while obtaining data from the spreadsheet.

## Usage Scenarios

## Key Features and Benefits

- **Cloud Storage Integration**: Efficiently merges multiple spreadsheet files stored in cloud storage into a single output file in formats like XLSX, CSV, or PDF.
- **Remote Processing**: Conducts the merging operation entirely within the cloud, negating the need to download files locally.
- **Efficient Data Handling**: Enhances performance and reduces data transfer by processing files in the cloud environment.

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/DataProcessingController/MergeSpreadsheetsInRemoteFolder) provides a publicly accessible programming interface allowing REST interactions directly from a web browser.

## Excel API SDK

Utilizing an SDK is the optimal method to expedite development. An SDK manages low-level details, allowing you to concentrate on project tasks. Visit the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples illustrate how to interact with Aspose.Cells web services using various SDKs:
