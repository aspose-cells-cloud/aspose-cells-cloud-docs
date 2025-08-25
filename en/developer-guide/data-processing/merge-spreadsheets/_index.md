---
title: "Merge spreadsheets"
second_title: "Developer Guide"
linktitle: "Merge spreadsheets"
type: docs
url: /merge-spreadsheets/
keywords: ""
description: "Merge local spreadsheet files into a specified format file. "
weight: 100
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdown, Match all blank cells in an Excel worksheet
---

# **Excel API : MergeSpreadsheets**

## **Overview**

Merge local spreadsheet files into a specified format file. 

## **Function Description**

This method combines multiple spreadsheet files from the local file system into a single output file in the specified format (e.g., XLSX, CSV, PDF). 
All input files must be accessible and in a supported format for the merge operation to succeed. 
The merged content is processed cloudly, without requiring cloud storage. 
Ensure proper file permissions are granted for reading the source files and writing the output file. 
If any of the files cannot be accessed or an error occurs during the merging process, an appropriate exception will be thrown. 
The final output format can be configured based on available conversion and export capabilities.


## **API Endpoint** 

```http
PUT http://api.aspose.cloud/v4.0/cells/merge/spreadsheet
```

## The request parameters of **mergeSpreadsheets** API are: 

| Parameter Name | Type | Path/Query String/HTTPBody | Description | 
| :- | :- | :- |:- | 
|Spreadsheet|File|FormData|Upload spreadsheet file.|
|outFormat|String|Query|The out file format.|
|mergeInOneSheet|Boolean|Query|Whether to combine all data into a single worksheet.|
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

- **Local File Merge:**: Combines multiple local spreadsheet files into a single output file in the specified format (e.g., XLSX, CSV, PDF).
- **Efficient Data Handling**: Processes the merge operation in the cloud without requiring cloud storage.Merges multiple files into a single output file efficiently, leveraging cloud processing capabilities.
- **Format Flexibility**: Supports a range of output formats based on the available conversion and export capabilities.

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/DataProcessingController/MergeSpreadsheets) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

## Excel API SDK 

Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

