---
title: "Merge spreadsheets in remote folder"
second_title: "Developer Guide"
linktitle: "Merge spreadsheets in remote folder"
type: docs
url: /merge-spreadsheets-in-remote-folder/
keywords: ""
description: "Merge spreadsheet files in folder of cloud storage into a specified format file. "
weight: 100
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdown, Match all blank cells in an Excel worksheet
---

# **Excel API : MergeSpreadsheetsInRemoteFolder**

## **Overview**

Merge spreadsheet files in folder of cloud storage into a specified format file. 

## **Function Description**

This method merges multiple spreadsheet files stored in cloud storage into a single output file in the specified format (e.g., XLSX, CSV, PDF). 
The operation is performed remotely, without requiring the files to be downloaded to the local machine. 
Valid cloud storage credentials and accessible file paths or identifiers are required for all input files. 
The merging process is executed entirely within the cloud environment, reducing data transfer and improving performance. 
If any of the source files cannot be accessed, or if an error occurs during the merge or conversion process, an appropriate exception will be thrown. 
Supported output formats depend on the capabilities of the underlying cloud processing service.


## **API Endpoint** 

```http
PUT http://api.aspose.cloud/v4.0/cells/merge/remote-spreadsheets
```

## The request parameters of **mergeSpreadsheetsInRemoteFolder** API are: 

| Parameter Name | Type | Path/Query String/HTTPBody | Description | 
| :- | :- | :- |:- | 
|folder|String|Query|The folder used to store the merged files.|
|fileMatchExpression|String|Query||
|outFormat|String|Query|The out file format.|
|mergeInOneSheet|Boolean|Query|Whether to combine all data into a single worksheet.|
|storageName|String|Query|(Optional) The name of the storage if using custom cloud storage. Use default storage if omitted.|
|outPath|String|Query|(Optional) The folder path where the workbook is stored. The default is null.|
|outStorageName|String|Query|Output file Storage Name.|
|fontsLocation|String|Query|Use Custom fonts.|
|regoin|String|Query|The spreadsheet region setting.|
|password|String|Query|The password for opening spreadsheet file.|


## **Response Structure**

```json
{
File
}
```

## Error Handling

- **400 Bad Request**: Invalid url.
- **401 Unauthorized**:  Authentication has failed, or no credentials were provided.
- **404 Not Found**: Source file not accessible.
- **500 Server Error** The spreadsheet has encountered an anomaly in obtaining data.


## Usage Scenarios
## Key Features and Benefits

- **Cloud Storage Integration**: Merges multiple spreadsheet files stored in cloud storage into a single output file in the specified format (e.g., XLSX, CSV, PDF).
- **Remote Processing**: Performs the merging operation entirely within the cloud environment, eliminating the need to download files to the local machine.
- **Efficient Data Handling**: Reduces data transfer and enhances performance by processing files remotely.

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/DataProcessingController/MergeSpreadsheetsInRemoteFolder) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

## Excel API SDK 

Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

