---
title: "Search broken links in remote range"
second_title: "Aspose.Cells Cloud Document"
linktitle: "Search broken links in remote range"
type: docs
url: /search-broken-links-in-remote-range/
keywords: ""
description: "Search broken links in the range of remoted spreadsheet. "
weight: 100
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdown, Match all blank cells in an Excel worksheet
---

# **Excel API : SearchBrokenLinksInRemoteRange**

Search broken links in the range of remoted spreadsheet. 

## **Interface Details**

### **Endpoint** 

```
PUT http://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{cellArea}search/broken-links
```

### **Function Description**

This method searches for broken links within a range of spreadsheet file stored in remote cloud storage.It scans all sheets and cells to identify hyperlinks that no longer point to valid destinations, such as dead URLs or missing external references.The operation is performed remotely within the cloud environment, without requiring the file to be downloaded to the local machine.Ensure that you have valid cloud storage credentials and proper access permissions to the target file.If the source file cannot be accessed, if it contains unsupported formats, or if an error occurs during the scanning process, an appropriate exception will be thrown.Depending on the implementation, the method may return a list of broken links with details such as sheet name, cell coordinates, and the invalid URL.Users should carefully review the results to update or remove outdated links in the spreadsheet.

### The request parameters of **searchBrokenLinksInRemoteRange** API are: 

| Parameter Name | Type | Path/Query String/HTTPBody | Description | 
| :- | :- | :- |:- | 
|name|String|Path|The name of the workbook file to be search.|
|worksheet|String|Path|Specify the worksheet for the lookup.|
|cellArea|String|Path|Specify the cell area for the lookup|
|folder|String|Query|The folder path where the workbook is stored.|
|storageName|String|Query|(Optional) The name of the storage if using custom cloud storage. Use default storage if omitted.|
|regoin|String|Query|The spreadsheet region setting.|
|password|String|Query|The password for opening spreadsheet file.|


### **Response Description**
```json
{
  "Name": "BrokenLinksReponse",
  "Type": "Class",
  "ParentName": "CellsCloudResponse",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "BrokenLinks",
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "BrokenLink",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "BrokenLink",
          "Name": "class:brokenlink"
        },
        "Name": "container"
      }
    },
    {
      "Name": "Code",
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": true,
      "DataType": {
        "Identifier": "Integer",
        "Name": "integer"
      }
    },
    {
      "Name": "Status",
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": true,
      "DataType": {
        "Identifier": "String",
        "Name": "string"
      }
    }
  ]
}
```

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/SearchControllor/SearchBrokenLinksInRemoteRange) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

## Excel API SDK 

Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:


{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
	{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchBrokenLinksInRemoteRange.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
	{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchBrokenLinksInRemoteRange.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
	{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchBrokenLinksInRemoteRange.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
	{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchBrokenLinksInRemoteRange.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
	{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchBrokenLinksInRemoteRange.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
	{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchBrokenLinksInRemoteRange.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
	{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchBrokenLinksInRemoteRange.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
	{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchBrokenLinksInRemoteRange.go" >}}
{{</tab>}}
{{< /tabs >}}


