---
title: "Replace Content in Remote Spreadsheet - Excel API"
second_title: "Aspose.Cells Cloud"
linktitle: "Replace Remote Spreadsheet Content"
type: docs
url: /replace-content-in-remote-spreadsheet/
keywords: "Replace content, remote spreadsheet, Excel API, REST API, cloud storage, text replacement"
description: "Efficiently replace text in remote spreadsheets using the Excel API."
weight: 100
kwords: "Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, JSON, Markdown, Replace content in Excel, Cloud-based text replacement, Modify text in remote spreadsheet"
---

# **Excel API: Replace Content in Remote Spreadsheet**

Efficiently replace text in remote spreadsheets using the Excel API.

## **Interface Details**

### **Endpoint**

```
PUT http://api.aspose.cloud/v4.0/cells/{name}/replace/content
```

### **Function Description**

This method allows users to replace specified text within a spreadsheet file stored in remote cloud storage. It supports replacing occurrences of the target text across all sheets and cells of the workbook directly within the cloud environment. The operation is performed remotely, eliminating the need to download the file to the local machine. Ensure that you have valid cloud storage credentials and accessible file paths or identifiers for the target spreadsheet. If the source file cannot be accessed, permissions are insufficient, writing to the file fails, or an error occurs during the replacement process (such as an unsupported file format), an appropriate exception will be thrown. Depending on the implementation, the method may return the number of replacements made or the locations of the replaced texts (e.g., sheet name, cell coordinates). Users should specify the exact text to replace and its replacement to ensure accurate modifications.

### The request parameters of **replaceContentInRemoteSpreadsheet** API are

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
| :- | :- | :- |:- |
| name | String | Path | The name of the workbook file to be modified. |
| searchText | String | Query | The text to search for in the spreadsheet. |
| replaceText | String | Query | The text to replace the found occurrences. |
| folder | String | Query | The folder path where the workbook is stored. |
| storageName | String | Query | (Optional) The name of the storage if using custom cloud storage. Use default storage if omitted. |
| region | String | Query | The spreadsheet region setting. |
| password | String | Query | The password for opening the spreadsheet file. |

### **Response Description**

```json
{
  "Name": "CellsCloudResponse",
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Code",
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Integer",
        "Name": "integer"
      }
    },
    {
      "Name": "Status",
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "String",
        "Name": "string"
      }
    }
  ]
}
```

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/SearchControllor/ReplaceContentInRemoteSpreadsheet) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

## Excel API SDK

Using an SDK is the best way to speed up development. An SDK manages low-level details, allowing you to focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:
