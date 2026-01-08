---
title: "Aspose.Cells Cloud Replace Web API - Update Text in Remote Spreadsheets Range"
second_title: "Document"
ArticleTitle: "Bulk Range Text Replacement in Cloud Excel Files - Find & Replace API"
linktitle: "Replace Remote Range Content"
type: docs
url: /replace-content-in-remote-range/
keywords: "find and replace Excel cloud, replace text in remote spreadsheet, update Excel content online, Aspose.Cells replace API, modify Excel files remotely, search and replace Excel API, edit cloud Excel files, automate text replacement Excel"
description: "Efficiently find and replace specified text within any range of a remote Excel file stored in cloud storage. Update content across entire workbooks or selected areas with Aspose.Cells Cloud Web API."
weight: 100
---

Perform bulk text replacement across remote Excel files stored in the cloud. Find and update specific text strings within selected ranges efficiently using Aspose.Cells Find and Replace API.

## **Replace Content in Remote Range API**

### API Endpoint

```
PUT http://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{cellArea}/replace/content
```

### **Request Parameters:**

| Parameter Name | Type | Path/Query String/HTTP Body | Description |
| :- | :- | :- | :- |
| name | String | Path | The name of the workbook file stored in cloud storage to be modified (e.g., `"report.xlsx"`). |
| searchText | String | Query | The text string to search for within the specified worksheet and cell area. Supports exact text matching. |
| replaceText | String | Query | The text string that will replace all occurrences of the `searchText` within the specified range. |
| worksheet | String | Path | The name of the worksheet where the find-and-replace operation will be performed. |
| cellArea | String | Path | The specific cell range (e.g., `"A1:D20"`) where the text search and replacement will occur. |
| folder | String | Query | The cloud storage folder path where the source workbook is located. |
| storageName | String | Query | *(Optional)* The name of the cloud storage where the workbook resides. If omitted, the default cloud storage is used. |
| region | String | Query | *(Optional)* Sets the locale for text handling, which may affect case sensitivity and character encoding in search operations (e.g., `"en-US"`, `"tr-TR"`). |
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

## Where should we use the Replace content of Range in Remote Spreadsheet API?

- **Batch Cloud File Update**: Modify the contents of multiple Excel files stored in cloud storage such as AWS S3 and Azure Blob
- **Dynamic population of cloud templates**: Batch populate dynamic data for report templates stored in the cloud
- **Cross-region file synchronization**: Synchronize the content consistency of Excel files in cloud storage in different geographical regions

## Why should you use the Replace content of Range in Remote Spreadsheet API?

- **Developer-Friendly**: Aspose.Cells Cloud offers SDK libraries in multiple languages, enabling quick development and comes with comprehensive documentation. Compared to building custom chart rendering solutions, this significantly reduces the development workload.
- **Reduced Labor Costs**: Reduced the need for positions dedicated to document consolidation.
- **Pay-per-use**: No upfront investment, only pay for API calls actually used.
- **Zero Maintenance Costs**: No need to maintain servers, update software, or deal with compatibility issues.
- **Preserves complex Excel formatting** in universally accessible PDF format.

## How to Use the Replace content of Range in Remote Spreadsheet API with SDKs

### OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/SearchControllor/ReplaceContentInRemoteRange) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the best way to accelerate development. The SDK handles the underlying details, allowing you to simply implement replace content in spreadsheets for cells with minimal code.
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ReplaceTextInRemoteRange.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ReplaceTextInRemoteRange.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ReplaceTextInRemoteRange.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ReplaceTextInRemoteRange.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ReplaceTextInRemoteRange.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ReplaceTextInRemoteRange.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ReplaceTextInRemoteRange.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ReplaceTextInRemoteRange.go" >}}
{{</tab>}}
{{< /tabs >}}
