---
title: "Aspose.Cells Cloud Web API - Search Worksheet Content in Remote Spreadsheet"
second_title: "Document"
ArticleTitle: "Search Worksheet Content in Remote Spreadsheet"
linktitle: "Search Remote Worksheet Content"
type: docs
url: /search-content-in-remote-worksheet/
keywords: "Excel API, Search Remote Worksheet, Cloud Spreadsheet, REST API, Search Text, Aspose.Cells, Document Search, Spreadsheet API"
description: "Efficiently search for text within a worksheet of a remote spreadsheet stored in the cloud."
weight: 100
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, JSON, Markdown, Match all blank cells in an Excel worksheet, Remote Worksheet Search
---

Search for specified text within a worksheet of a remote spreadsheet stored in cloud storage.

## **Interface Details**

## **Search Content in Remote Worksheet**

```
PUT http://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/search/content
```

### **Request Parameters:**

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

### **Response**

```json
{
  "Name": "BrokenLinksResponse",
  "Type": "Class",
  "ParentName": "CellsCloudResponse",
  "Properties": [
    {
      "Name": "BrokenLinks",
      "DataType": {
        "Identifier": "Container",
        "Reference": "BrokenLink",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "BrokenLink",
        },
      }
    },
    {
      "Name": "Code",
      "DataType": {
        "Identifier": "Integer",
      }
    },
    {
      "Name": "Status",
      "DataType": {
        "Identifier": "String",
      }
    }
  ]
}
```

### Error Codes

- **400 Bad Request**: Invalid Aspose.Cells Cloud API URI.
- **401 Unauthorized**: Invalid access token. Or invalid client id and secret.
- **404 Not Found**: The spreadsheet file not accessible.
- **500 Server Error**: The spreadsheet has encountered an anomaly in obtaining calculation data.

## Where should we use the Search content within the worksheet of Spreadsheet API?

When you need to Search content within the worksheet of Spreadsheet, you can use this API.

## Why should you use the Search content within the worksheet of Spreadsheet API?

- Effortlessly search content within a remote spreadsheet worksheet with this API.
- Development can be quickly completed through the existing SDK.

## How to Use the Search for broken links within the worksheet of the Spreadsheet API with SDKs

### OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/SearchControllor/SearchContentInRemoteWorksheet) defines a publicly accessible programming interface and enables REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the best way to accelerate development. The SDK handles the underlying details, allowing you to simply implement search content within worksheet of spreadsheets for cells with minimal code.
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:
