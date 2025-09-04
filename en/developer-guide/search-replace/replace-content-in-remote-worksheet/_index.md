---
title: "Replace Worksheet Content in Remote Spreadsheet - Excel API"
second_title: "Aspose.Cells Cloud"
linktitle: "Replace Worksheet Content in Remote Spreadsheet"
type: docs
url: /replace-content-in-remote-worksheet/
keywords: "Excel API, Replace Content, Remote Worksheet, Cloud Spreadsheet, REST API, Text Replacement, Office Cloud Integration, Aspose.Cells"
description: "Efficiently replace text in the worksheet of a remote spreadsheet using the Aspose.Cells API."
weight: 100
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, JSON, Markdown, Match all blank cells in an Excel worksheet, ReplaceContentInRemoteWorksheet
---

# **Excel API: ReplaceContentInRemoteWorksheet**

Efficiently replace specified text in the worksheet of a remote spreadsheet using the Aspose.Cells API.

## **Interface Details**

### **Endpoint**

```
PUT http://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/replace/content
```

### **Function Description**

This method allows you to replace specified text within a worksheet of a spreadsheet file stored in remote cloud storage. It supports replacing occurrences of the target text across all sheets and cells of the workbook directly within the cloud environment. The operation is performed remotely, eliminating the need to download the file to the local machine. Ensure that you have valid cloud storage credentials and accessible file paths or identifiers for the target spreadsheet. If the source file cannot be accessed, permissions are insufficient, or an error occurs during the replacement process (such as an unsupported file format), an appropriate exception will be thrown. Depending on the implementation, this method may return the number of replacements made or the locations of the replaced texts (e.g., sheet name, cell coordinates). Users must specify the exact text to replace and its replacement to ensure accurate modifications.

### The request parameters of **replaceContentInRemoteWorksheet** API are

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

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/SearchControllor/ReplaceContentInRemoteWorksheet) defines a publicly accessible programming interface and allows you to carry out REST interactions directly from a web browser.

## Excel API SDK

Utilizing an SDK is the most efficient way to accelerate your development. An SDK handles low-level details, allowing you to concentrate on your project objectives. Please visit the [GitHub repository](https://github.com/aspose-cells-cloud) for a comprehensive list of Aspose.Cells Cloud SDKs.

The following code examples illustrate how to interact with Aspose.Cells web services using various SDKs:
