---
title: "Convert range to csv"
second_title: "Aspose.Cells Cloud Document"
linktitle: "Convert range to csv"
type: docs
url: /convert-range-to-csv/
keywords: ""
description: "Converts a range of spreadsheet on a local drive to the csv file. "
weight: 100
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdown, Match all blank cells in an Excel worksheet
---

# **Excel API : ConvertRangeToCsv**

Converts a range of spreadsheet on a local drive to the csv file. 

## **Interface Details**

### **Endpoint** 

```
PUT http://api.aspose.cloud/v4.0/cells/convert/range/csv
```

### **Function Description**

This method reads a spreadsheet file from the local file system, converts it's range to the desired csv file, and returns the converted result.The source file path and target format must be specified correctly.Ensure that the necessary permissions are in place to read the source file and write the converted file if applicable.The conversion process occurs entirely on the cloud server, eliminating the need for any cloud storage or external downloads.If the source file does not exist, is inaccessible, or if an error occurs during the conversion process, an appropriate exception will be thrown.Supported formats for conversion depend on the available libraries and their capabilities.

### The request parameters of **convertRangeToCsv** API are: 

| Parameter Name | Type | Path/Query String/HTTPBody | Description | 
| :- | :- | :- |:- | 
|Spreadsheet|File|FormData|Upload spreadsheet file.|
|worksheet|String|Query|worksheet name of spreadsheet.|
|range|String|Query|cell area. e.g. A1:C10|
|outPath|String|Query|(Optional) The folder path where the workbook is stored. The default is null.|
|outStorageName|String|Query|Output file Storage Name.|
|fontsLocation|String|Query|Use Custom fonts.|
|regoin|String|Query|The spreadsheet region setting.|
|password|String|Query|The password for opening spreadsheet file.|


### **Response Description**
```json
{
File
}
```

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/ConversionController/ConvertRangeToCsv) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

## Excel API SDK 

Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

