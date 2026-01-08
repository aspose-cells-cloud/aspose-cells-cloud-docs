---
title: "Aspose.Cells Cloud Replace Web API - Update Text in Remote Spreadsheets"
second_title: "Document"
ArticleTitle: "Bulk Text Replacement in Cloud Excel Files - Find & Replace API"
linktitle: "Replace Remote Spreadsheet Content"
type: docs
url: /replace-content-in-remote-spreadsheet/
keywords: "find and replace in cloud Excel, replace text remote spreadsheet, update Excel content online, Aspose.Cells replace API, modify Excel files in cloud, search and replace API, edit remote Excel, automate text replacement, cloud Excel editing"
description: "Efficiently find and replace specified text within remote Excel files stored in cloud storage. Update content across entire workbooks with Aspose.Cells Find and Replace API."
weight: 100
---

Perform bulk text replacement across remote Excel files stored in the cloud. Find and update specific text strings efficiently using Aspose.Cells Find and Replace API for cloud spreadsheets.

## **Replace Content in Remote Spreadsheet API**

### API Endpoint

```
PUT http://api.aspose.cloud/v4.0/cells/{name}/replace/content
```

### **Request Parameters:**

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
| :- | :- | :- | :- |
| name | String | Path | The name of the workbook file stored in cloud storage to be modified (e.g., `"report.xlsx"`, `"data.xls"`). |
| searchText | String | Query | The text string to search for within the entire workbook. The search is case-sensitive and applies to all worksheets unless otherwise constrained. |
| replaceText | String | Query | The text string that will replace all occurrences of `searchText` found within the workbook. |
| folder | String | Query | The cloud storage folder path where the source workbook is located (e.g., `"/documents/quarterly/"`). |
| storageName | String | Query | *(Optional)* The name of the custom cloud storage (e.g., `"MyS3Bucket"`, `"AzureContainer"`). If omitted, the operation uses the default cloud storage configured for your account. |
| region | String | Query | *(Optional)* Sets the locale for text handling, which may affect character encoding and language-specific search behavior (e.g., `"en-US"`, `"de-DE"`). |
| password | String | Query | *(Optional)* If the workbook is password-protected, provide the password to open and modify the file. |

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

- **Batch Cloud File Update**: Modify the contents of multiple Excel files stored in cloud storage such as AWS S3 and Azure Blob
- **Dynamic population of cloud templates**: Batch populate dynamic data for report templates stored in the cloud
- **Cross-region file synchronization**: Synchronize the content consistency of Excel files in cloud storage in different geographical regions

## Why should you use the Replace content in Remote Spreadsheet API?

- **Developer-Friendly**: Aspose.Cells Cloud offers SDK libraries in multiple languages, enabling quick development and comes with comprehensive documentation. Compared to building custom chart rendering solutions, this significantly reduces the development workload.
- **Reduced Labor Costs**: Reduced the need for positions dedicated to document consolidation.
- **Pay-per-use**: No upfront investment, only pay for API calls actually used.
- **Zero Maintenance Costs**: No need to maintain servers, update software, or deal with compatibility issues.
- **Preserves complex Excel formatting** in universally accessible PDF format.

## How to Use the Replace content in Remote Spreadsheet API with SDKs

### OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/SearchControllor/ReplaceContentInRemoteSpreadsheet) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the best way to accelerate development. The SDK handles the underlying details, allowing you to simply implement replace content in spreadsheets for cells with minimal code.
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:
