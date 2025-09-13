---
title: "Aspose.Cells Cloud Web API - Replace Worksheet Content in Remote Spreadsheet"
second_title: "Aspose.Cells Cloud Document"
ArticleTitle: "Replace Worksheet Content in Remote a Spreadsheet"
linktitle: "Replace Remote Worksheet Content"
type: docs
url: /replace-content-in-remote-worksheet/
keywords: "Aspose.Cells Cloud Web API, Replace Content, Remote Worksheet, Cloud Spreadsheet, Text Replacement, Office Cloud Integration"
description: "Efficiently replace text in the worksheet of a remote spreadsheet using the Aspose.Cells API."
weight: 100
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, JSON, Markdown, Match all blank cells in an Excel worksheet, ReplaceContentInRemoteWorksheet
---

Efficiently replace specified text within a worksheet of a remote spreadsheet file.

## **Replace Content in Remote Worksheet API**

```
PUT http://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/replace/content
```

### **Request Parameters:**

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
| :- | :- | :- |:- |
| name | String | Path | The name of the workbook file to be modified. |
| worksheet | String | Path | Specify the worksheet for the replacement. |
| searchText | String | Query | The text to search for in the worksheet. |
| replaceText | String | Query | The text to replace the searched text with. |
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

- **400 Bad Request**: Invalid Apose.Cells Cloud API URI.
- **401 Unauthorized**: Invalid access token. Or invalid client id and secret.
- **404 Not Found**: The spreadsheet file not accessible.
- **500 Server Error**: The spreadsheet has encountered an anomaly in obtaining calculation data.

## Where should we use the Replace content of Worksheet in Remote Spreadsheet API?

When you need to replace content of Worksheet in remote spreadsheet, you can use this API.

## Why should you use the Replace content of Worksheet in Remote Spreadsheet API?

- Quickly replace content of Worksheet in remote spreadsheets.
- Development can be quickly completed through the existing SDK.

## How to Use the Replace content of Worksheet in Remote Spreadsheet API with SDKs

### OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/SearchControllor/ReplaceContentInRemoteWorksheet) defines a publicly accessible programming interface and allows you to carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the best way to accelerate development. The SDK handles the underlying details, allowing you to simply implement replace content of worksheet in spreadsheets for cells with minimal code.
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples illustrate how to interact with Aspose.Cells web services using various SDKs:
