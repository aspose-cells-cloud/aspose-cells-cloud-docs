---
title: "Merge remote spreadsheet"
second_title: "Aspose.Cells Cloud Document"
linktitle: "Merge remote spreadsheet"
type: docs
url: /merge-remote-spreadsheet/
keywords: ""
description: "Merge a spreadsheet file into other spreadsheet in cloud storage, and output a specified format file. "
weight: 100
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdown, Match all blank cells in an Excel worksheet
---

# **Excel API : MergeRemoteSpreadsheet**

Merge a spreadsheet file into other spreadsheet in cloud storage, and output a specified format file. 

## **Interface Details**

### **Endpoint** 

```
PUT http://api.aspose.cloud/v4.0/cells/{name}/merge/spreadsheet
```

### **Function Description**

This method merges multiple spreadsheet files stored in cloud storage into a single output file in the specified format (e.g., XLSX, CSV, PDF).The operation is performed remotely, without requiring the files to be downloaded to the local machine.Valid cloud storage credentials and accessible file paths or identifiers are required for all input files.The merging process is executed entirely within the cloud environment, reducing data transfer and improving performance.If any of the source files cannot be accessed, or if an error occurs during the merge or conversion process, an appropriate exception will be thrown.Supported output formats depend on the capabilities of the underlying cloud processing service.

### The request parameters of **mergeRemoteSpreadsheet** API are: 

| Parameter Name | Type | Path/Query String/HTTPBody | Description | 
| :- | :- | :- |:- | 
|name|String|Path|The name of the workbook file to be split.|
|mergedSpreadsheet|String|Query||
|folder|String|Query|The folder path where the workbook is stored.|
|outFormat|String|Query|The out file format.|
|mergeInOneSheet|Boolean|Query|Whether to combine all data into a single worksheet.|
|storageName|String|Query|(Optional) The name of the storage if using custom cloud storage. Use default storage if omitted.|
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

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/DataProcessingController/MergeRemoteSpreadsheet) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

## Excel API SDK 

Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:


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


