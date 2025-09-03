---
title: "Merge Remote Spreadsheet - Excel API"
second_title: Aspose.Cells Cloud"
linktitle: "Merge Remote Spreadsheet"
type: docs
url: /merge-remote-spreadsheet/
keywords: "Merge spreadsheets, cloud storage, Excel API, REST API, spreadsheet merging, XLSX, CSV, PDF output"
description: "Integrate and merge multiple spreadsheet files stored in cloud storage into a specified output format, enhancing productivity and data handling."
weight: 100
kwords: "Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, JSON, Markdown, merge blank cells, cloud processing"
---

# **Excel API : MergeRemoteSpreadsheet**

## **Overview**

This API enables the merging of multiple spreadsheet files stored in cloud storage into a single output file in a specified format (e.g., XLSX, CSV, PDF). The operation is performed remotely, ensuring that no files need to be downloaded to the local machine. It requires valid cloud storage credentials and accessible file paths or identifiers for all input files. This method enhances performance by executing the merging process within the cloud environment.

## **Function Description**

The `mergeRemoteSpreadsheet` method merges multiple spreadsheet files stored in cloud storage into a single output file in the specified format (e.g., XLSX, CSV, PDF). It operates remotely, reducing data transfer and improving performance. If any of the source files cannot be accessed or if an error occurs during the merge or conversion process, an appropriate exception will be thrown. Supported output formats depend on the capabilities of the underlying cloud processing service.

## **API Endpoint**

```http
PUT http://api.aspose.cloud/v4.0/cells/{name}/merge/spreadsheet
```

## The request parameters of **mergeRemoteSpreadsheet** API are

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
| :- | :- | :- |:- |
|name|String|Path|The name of the workbook file to be merged.|
|mergedSpreadsheet|String|Query|The list of spreadsheet files to merge.|
|folder|String|Query|The folder path where the workbook is stored.|
|outFormat|String|Query|The output file format (e.g., XLSX, PDF).|
|mergeInOneSheet|Boolean|Query|Whether to combine all data into a single worksheet.|
|storageName|String|Query|(Optional) The name of the storage if using custom cloud storage. Defaults to default storage if omitted.|
|outPath|String|Query|(Optional) The folder path for the merged workbook. Defaults to null.|
|outStorageName|String|Query|The name of the storage for the output file.|
|fontsLocation|String|Query|Custom font location.|
|region|String|Query|The spreadsheet region setting.|
|password|String|Query|The password for accessing the spreadsheet file.|

## **Response Structure**

```json
{
File
}
```

## Error Handling

- **400 Bad Request**: Invalid URL or parameters.
- **401 Unauthorized**: Authentication failed or credentials were not provided.
- **404 Not Found**: Source file not accessible.
- **500 Server Error**: An error occurred during the merging process.

## Usage Scenarios

## Key Features and Benefits

- **Cloud Storage Integration**: Seamlessly merges multiple spreadsheet files from cloud storage into a single output file in the specified format.
- **Remote Processing**: Eliminates the need to download files to the local machine, enhancing efficiency.
- **Efficient Data Handling**: Reduces data transfer and improves performance by processing files directly in the cloud environment.

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/DataProcessingController/MergeRemoteSpreadsheet) provides a publicly accessible programming interface for executing REST interactions directly from a web browser.

## Excel API SDK

Utilizing an SDK is the optimal approach to accelerate development. An SDK manages low-level details, allowing you to concentrate on your project tasks. Explore the [GitHub repository](https://github.com/aspose-cells-cloud) for a comprehensive list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to interact with Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MergeRemoteSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MergeRemoteSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MergeRemoteSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MergeRemoteSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MergeRemoteSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MergeRemoteSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MergeRemoteSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MergeRemoteSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}
