---
title: "Aspose.Cells Cloud Web API - Merge Spreadsheets in Remote Folder"
second_title: "Aspose.Cells Cloud"
ArticleTitle: "Merge Spreadsheets into a Single File in Cloud Storage Folder"
linktitle: "Merge Spreadsheets in Remote Folder"
type: docs
url: /merge-spreadsheets-in-remote-folder/
keywords: "Merge spreadsheets, cloud storage, Excel API, remote processing, spreadsheet formats, REST API"
description: "Seamlessly merge spreadsheet files stored in cloud storage into specified output formats like XLSX, CSV, and PDF."
weight: 100
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, JSON, Markdown, Merge spreadsheets, Cloud processing, Remote file handling
---

Merge multiple spreadsheet files which stored in a cloud storage folder, while supporting output in 30+ file formats.

## **Merge Spreadsheets in Remote Folder API**

```http
PUT http://api.aspose.cloud/v4.0/cells/merge/remote-spreadsheets
```

### **Request Parameters:**

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
| :- | :- | :- |:- |
| folder | String | Query | The folder where the merged files will be stored.|
| fileMatchExpression | String | Query | Expression to match files for merging. |
| outFormat | String | Query | The desired output file format. |
| mergeInOneSheet | Boolean | Query | Indicates whether to combine all data into a single worksheet. |
| storageName | String | Query | (Optional) The name of the custom cloud storage; defaults to default storage if omitted. |
| outPath | String | Query | (Optional) The folder path for storing the workbook; defaults to null. |
| outStorageName | String | Query | The name of the storage for the output file. |
| fontsLocation | String | Query | Specifies custom fonts. |
| region | String | Query | Sets the spreadsheet region. |
| password | String | Query | The password for opening the spreadsheet file. |

## **Response**

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

## Where should we use the Merge Spreadsheet in remote folder API?

When you need to merge multiple data files together, you can use this API.

## Why should you use the Merge Spreadsheet in remote folder API?

- Cloud storage files do not need to be downloaded, and can be merged directly in the cloud.
- Batch merge multiple spreadsheet files together, Support matching expression.
- Development can be quickly completed through the existing SDK.

## How to Use the Merge Spreadsheet in remote folder API with SDKs

### OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/DataProcessingController/MergeSpreadsheetsInRemoteFolder) provides a publicly accessible programming interface allowing REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the best way to accelerate development. The SDK handles the underlying details, allowing you to simply implement merge spreadsheets for cells with minimal code.
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples illustrate how to interact with Aspose.Cells web services using various SDKs:
