---
title: "Aspose.Cells Cloud Web API - Merge Spreadsheets"
second_title: "Aspose.Cells Cloud"
ArticleTitle: "Merge Spreadsheets into a Single File"
linktitle: "Merge Spreadsheets"
type: docs
url: /merge-spreadsheets/
keywords: "Merge spreadsheets, data merging, file format conversion, REST API, XLSX, CSV, PDF"
description: "Easily merge local spreadsheet files into various formats (XLSX, CSV, PDF) using the Excel API."
weight: 100
kwords: "Excel API, Merge spreadsheets, Office Cloud, REST API, Spreadsheet merging, CSV format, JSON, Markdown"
---

Merge multiple local spreadsheet files into a single file, while supporting output in dozens of file formats.

## **Merge Spreadsheet API**

```http
PUT http://api.aspose.cloud/v4.0/cells/merge/spreadsheet
```

### **Request Parameters:**

| Parameter Name | Type | Path/Query String/HTTP Body | Description |
| :- | :- | :- |:- |
| Spreadsheet | File | FormData | Upload the spreadsheet file. |
| outFormat | String | Query | Specify the output file format. |
| mergeInOneSheet | Boolean | Query | Indicate whether to combine all data into a single worksheet. |
| outPath | String | Query | (Optional) The folder path for the output workbook. Defaults to null. |
| outStorageName | String | Query | Specify the output file storage name. |
| fontsLocation | String | Query | Define custom fonts to be used. |
| region | String | Query | Set the spreadsheet region. |
| password | String | Query | Provide the password for opening the spreadsheet file. |

### **Response**

```json
[
    {
        "Name": "ResponseFile",
        "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
        }
    }
]
```

### Error Codes

- **400 Bad Request**: Invalid Apose.Cells Cloud API URI.
- **401 Unauthorized**: Invalid access token. Or invalid client id and secret.
- **404 Not Found**: The spreadsheet file not accessible.
- **500 Server Error**: The spreadsheet has encountered an anomaly in obtaining calculation data.

## Where should we use the Merge Local Spreadsheet API?

When you need to merge multiple data files together, you can use this API.

## Why should you use the Merge Local Spreadsheet API?

- No need for cloud storage space, just merge directly.
- Development can be quickly completed through the existing SDK.

## How to Use the Merge Local Spreadsheet API with SDKs

### OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/DataProcessingController/MergeSpreadsheets) provides a publicly accessible programming interface, allowing users to perform REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the best way to accelerate development. The SDK handles the underlying details, allowing you to simply implement merge spreadsheets for cells with minimal code.
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples illustrate how to make calls to Aspose.Cells web services using various SDKs:
