---
title: "Aspose.Cells Cloud Web API - Replace Content in Remote Spreadsheet"
second_title: "Document"
ArticleTitle: "Replace Content in Remote a Spreadsheet"
linktitle: "Replace Remote Spreadsheet Content"
type: docs
url: /replace-content-in-remote-spreadsheet/
keywords: "Replace content, remote spreadsheet, Excel API, REST API, cloud storage, text replacement"
description: "Efficiently replace text in remote spreadsheets using the Excel API."
weight: 100
kwords: "Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, JSON, Markdown, Replace content in Excel, Cloud-based text replacement, Modify text in remote spreadsheet"
---

Efficiently replace specified text within a remote spreadsheet file.

## **Replace Content in Remote Spreadsheet API**

```
PUT http://api.aspose.cloud/v4.0/cells/{name}/replace/content
```

### **Request Parameters:**

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
| :- | :- | :- |:- |
| name | String | Path | The name of the workbook file to be modified. |
| searchText | String | Query | The text to search for in the spreadsheet. |
| replaceText | String | Query | The text to replace the found occurrences. |
| folder | String | Query | The folder path where the workbook is stored. |
| storageName | String | Query | (Optional) The name of the storage if using custom cloud storage. Use default storage if omitted. |
| region | String | Query | The spreadsheet region setting. |
| password | String | Query | The password for opening the spreadsheet file. |

### **Response**

```json
{
  "Name": "CellsCloudResponse",
  "Type": "Class",
  "Properties": [
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

## Where should we use the Replace content in Remote Spreadsheet API?

When you need to replace content in remote spreadsheet, you can use this API.

## Why should you use the Replace content in Remote Spreadsheet API?

- Quickly replace content in remote spreadsheets.
- Development can be quickly completed through the existing SDK.

## How to Use the Replace content in Remote Spreadsheet API with SDKs

### OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/SearchControllor/ReplaceContentInRemoteSpreadsheet) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the best way to accelerate development. The SDK handles the underlying details, allowing you to simply implement replace content in spreadsheets for cells with minimal code.
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:
