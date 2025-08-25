---
title: "Search content in remote spreadsheet"
second_title: "Developer Guide"
linktitle: "Search content in remote spreadsheet"
type: docs
url: /search-content-in-remote-spreadsheet/
keywords: ""
description: "Search text in the remoted spreadsheet. "
weight: 100
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdown, Match all blank cells in an Excel worksheet
---

# **Excel API : SearchContentInRemoteSpreadsheet**

Search text in the remoted spreadsheet. 

## **Interface Details**

### **Endpoint** 

```
PUT http://api.aspose.cloud/v4.0/cells/{name}/search/content
```

### **Function Description**

This method searches for specified text within a spreadsheet file stored in remote cloud storage.It supports searching through all sheets and cells of the workbook, identifying occurrences of the search term directly within the cloud environment.The operation is performed remotely, eliminating the need to download the file to the local machine.Ensure that you have valid cloud storage credentials and accessible file paths or identifiers for the target spreadsheet.If the source file cannot be accessed, permissions are insufficient, or if an error occurs during the search process (such as an unsupported file format), an appropriate exception will be thrown.Depending on the implementation, the method may return the locations of the matches (e.g., sheet name, cell coordinates).Users should specify the exact search criteria, including case sensitivity and whole word matching options, to refine search results.

### The request parameters of **searchContentInRemoteSpreadsheet** API are: 

| Parameter Name | Type | Path/Query String/HTTPBody | Description | 
| :- | :- | :- |:- | 
|name|String|Path|The name of the workbook file to be search.|
|searchText|String|Query|The searched text.|
|ignoringCase|Boolean|Query|Ignore the text of the search.|
|folder|String|Query|The folder path where the workbook is stored.|
|storageName|String|Query|(Optional) The name of the storage if using custom cloud storage. Use default storage if omitted.|
|regoin|String|Query|The spreadsheet region setting.|
|password|String|Query|The password for opening spreadsheet file.|


### **Response Description**
```json
{
  "Name": "SearchResponse",
  "Type": "Class",
  "ParentName": "CellsCloudResponse",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "TextItems",
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "TextItem",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "TextItem",
          "Name": "class:textitem"
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

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/SearchControllor/SearchContentInRemoteSpreadsheet) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

## Excel API SDK 

Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:


{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchTextInRemoteSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchTextInRemoteSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchTextInRemoteSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchTextInRemoteSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchTextInRemoteSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchTextInRemoteSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchTextInRemoteSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchTextInRemoteSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}


