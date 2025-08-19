---
title: "Compress spreadsheet"
second_title: "Aspose.Cells Cloud Document"
linktitle: "Compress spreadsheet"
type: docs
url: /compress-spreadsheet/
keywords: ""
description: "The Web API endpoint allows users to compress a spreadsheet to reduce its file size. This function provides a straightforward way to optimize the storage and performance of spreadsheets by applying a specified compression level. "
weight: 100
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdown, Match all blank cells in an Excel worksheet
---

# **Excel API : CompressSpreadsheet**

## **Overview**

The Web API endpoint allows users to compress a spreadsheet to reduce its file size. This function provides a straightforward way to optimize the storage and performance of spreadsheets by applying a specified compression level. 

## **Function Description**

By using the CompressSpreadsheet API, you can dynamically manage the storage and performance of your spreadsheets, applying specified compression levels to reduce file sizes and optimize storage usage. This feature enhances your ability to manage and optimize your spreadsheets efficiently, ensuring minimal storage usage and enhanced performance.


## **API Endpoint** 

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/compress
```

## The request parameters of **compressSpreadsheet** API are: 

| Parameter Name | Type | Path/Query String/HTTPBody | Description | 
| :- | :- | :- |:- | 
|Spreadsheet|File|FormData|Upload spreadsheet file.|
|level|Integer|Query|Specifies the compression level to be applied to the spreadsheet. The level should be within a valid range (e.g., 0-9 for most compression algorithms, where 0 is no compression and 9 is maximum compression).|
|outPath|String|Query|(Optional) The folder path where the workbook is stored. The default is null.|
|outStorageName|String|Query|Output file Storage Name.|
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

- **Dynamic Compression**: Allows users to compress a spreadsheet to reduce its file size.
- **Specified Compression Levels**: Provides the ability to apply different levels of compression based on user requirements.

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/ManagementController/CompressSpreadsheet) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

## Excel API SDK 

Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:


{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CompressSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CompressSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CompressSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CompressSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CompressSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CompressSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CompressSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CompressSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}


