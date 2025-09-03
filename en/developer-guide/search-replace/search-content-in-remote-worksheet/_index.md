---
title: "Search Content in Remote Worksheet - Excel API"
second_title: "Aspose.Cells Cloud"
linktitle: "Search Content in Remote Worksheet"
type: docs
url: /search-content-in-remote-worksheet/
keywords: "Excel API, Search Remote Worksheet, Cloud Spreadsheet, REST API, Search Text, Aspose.Cells, Document Search, Spreadsheet API"
description: "Efficiently search for text within a worksheet of a remote spreadsheet stored in the cloud."
weight: 100
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, JSON, Markdown, Match all blank cells in an Excel worksheet, Remote Worksheet Search
---

# **Excel API: Search Content in Remote Worksheet**

Efficiently search for specified text within a worksheet of a remote spreadsheet stored in cloud storage.

## **Interface Details**

### **Endpoint**

```
PUT http://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/search/content
```

### **Function Description**

This method allows users to search for specified text within a worksheet of a spreadsheet file stored in remote cloud storage. It supports searching through all sheets and cells of the workbook, identifying occurrences of the search term directly within the cloud environment. The operation is executed remotely, eliminating the need to download the file locally. Users must ensure they have valid cloud storage credentials and accessible file paths or identifiers for the target spreadsheet. If the source file cannot be accessed, permissions are insufficient, or if an error occurs during the search process (such as an unsupported file format), an appropriate exception will be thrown. Depending on the implementation, the method may return the locations of the matches (e.g., sheet name, cell coordinates). Users should specify exact search criteria, including case sensitivity and whole word matching options, to refine search results.

### The request parameters of **searchContentInRemoteWorksheet** API are

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
| :- | :- | :- |:- |
|name|String|Path|The name of the workbook file to search.|
|worksheet|String|Path|The name of the worksheet.|
|searchText|String|Query|The text to be searched.|
|ignoringCase|Boolean|Query|Indicates whether to ignore case during the search.|
|folder|String|Query|The folder path where the workbook is stored.|
|storageName|String|Query|(Optional) The name of the storage if using custom cloud storage. Default storage is used if omitted.|
|region|String|Query|The spreadsheet region setting.|
|password|String|Query|The password for opening the spreadsheet file.|

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

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/SearchControllor/SearchContentInRemoteWorksheet) defines a publicly accessible programming interface and enables REST interactions directly from a web browser.

## Excel API SDK

Using an SDK is the most efficient way to accelerate development. An SDK manages low-level details, allowing you to focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:
