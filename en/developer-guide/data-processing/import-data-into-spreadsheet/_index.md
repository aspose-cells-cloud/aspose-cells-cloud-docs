---
title: "Import data into spreadsheet"
second_title: "Aspose.Cells Cloud Document"
linktitle: "Import data into spreadsheet"
type: docs
url: /import-data-into-spreadsheet/
keywords: ""
description: "Import data into a spreadsheet from a supported data file format. "
weight: 100
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdown, Match all blank cells in an Excel worksheet
---

# **Excel API : ImportDataIntoSpreadsheet**

## **Overview**

Import data into a spreadsheet from a supported data file format. 

## **Function Description**

This API allows you to import data into a spreadsheet from a supported data file format (CSV, JSON, XML). 
It takes two main inputs: the target spreadsheet and the data file containing the data to be imported. 
The data file must be in one of the supported formats (CSV, JSON, XML) and should be accessible to the API. 
The import process is handled efficiently, ensuring that the data is correctly parsed and inserted into the specified spreadsheet. 
If the data file is not accessible, the format is unsupported, or an error occurs during the import process, an appropriate exception will be thrown. 
Users should ensure that the data file is correctly formatted and that the spreadsheet is accessible to avoid errors.


## **API Endpoint** 

```http
PUT http://api.aspose.cloud/v4.0/cells/import/data
```

## The request parameters of **importDataIntoSpreadsheet** API are: 

| Parameter Name | Type | Path/Query String/HTTPBody | Description | 
| :- | :- | :- |:- | 
|datafile|File|FormData|Upload data file.|
|Spreadsheet|File|FormData|Upload spreadsheet file.|
|worksheet|String|Query|Specify the worksheet for importing data|
|startcell|String|Query|Specify the starting position for importing data|
|insert|Boolean|Query|The specified import data is for insertion and overwrite.|
|convertNumericData|Boolean|Query|Specify whether to convert numerical data|
|splitter|String|Query|Specify the delimiter for the CSV format.|
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

- **Multiple Data Formats**: Supports importing data from CSV, JSON, and XML file formats.
- **Direct Spreadsheet Integration**: Imports data directly into the specified spreadsheet.
- **Efficient Data Handling**: Processes data efficiently, ensuring accurate parsing and insertion.

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/DataProcessingController/ImportDataIntoSpreadsheet) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

## Excel API SDK 

Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:


{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ImportDataIntoSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ImportDataIntoSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ImportDataIntoSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ImportDataIntoSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ImportDataIntoSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ImportDataIntoSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ImportDataIntoSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ImportDataIntoSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}


