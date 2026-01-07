---
title: "Aspose.Cells Cloud Web API - Merge Matching Spreadsheets in Remote Folder to 30+ Formats."
second_title: "Document"
ArticleTitle: "Merge matching spreadsheet files into a file in a remote Folder."
linktitle: "Merge Spreadsheets in Remote Folder"
type: docs
url: /merge-spreadsheets-in-remote-folder/
keywords: "merge matching spreadsheet files in remote folder, Aspose.Cells Cloud merge API, batch merge Excel files cloud, merge spreadsheets to PDF CSV JSON, cloud folder spreadsheet merger, remote Excel file merging, merge matching files to multiple formats, Aspose merge API, automate Excel file merging"
description: "Combine the spreadsheet files stored in the cloud storage into one file, and the file format supports 30 formats for output, such as PDF,CSV, JSON and other common formats."
weight: 100
---

Merge matching spreadsheet files from a remote cloud folder and export to 30+ supported formats like PDF, CSV, JSON, ODS, and XPS using Aspose.Cells Cloud API.

## **Merge Spreadsheets in Remote Folder API**

### API Endpoint

```http
PUT http://api.aspose.cloud/v4.0/cells/merge/remote-spreadsheets
```

### **Request Parameters:**

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
| :- | :- | :- | :- |
| folder | String | Query | The source folder path in cloud storage where the spreadsheet files to be merged are located. |
| fileMatchExpression | String | Query | A string expression or pattern to filter and select matching files in the source folder for merging (e.g., `"*report*.xlsx"`). |
| outFormat | String | Query | Specifies the output file format after merging (e.g., `PDF`, `CSV`, `JSON`, `XLSX`). Supports 30+ common formats. |
| mergeInOneSheet | Boolean | Query | When `true`, merges content from all matched files into a single worksheet. When `false`, each file's content is kept in separate worksheets. |
| storageName | String | Query | *(Optional)* The name of the cloud storage where source files reside. If omitted, the default cloud storage is used. |
| outPath | String | Query | *(Optional)* Specifies the target folder path in cloud storage where the merged file will be saved. If omitted, the merged file is saved in the source folder. |
| outStorageName | String | Query | The name of the cloud storage where the output merged file will be saved. |
| fontsLocation | String | Query | *(Optional)* Specifies a custom folder path containing font files to ensure proper text rendering when exporting to PDF or image formats. |
| region | String | Query | *(Optional)* Sets the locale/region for number, date, and currency formatting in the output file (e.g., `"en-US"`, `"de-DE"`). |
| password | String | Query | *(Optional)* If any matched spreadsheet file is password-protected, provide the password to open the file. |

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

- **400 Bad Request**: Invalid Aspose.Cells Cloud API URI.
- **401 Unauthorized**: Invalid access token. Or invalid client id and secret.
- **404 Not Found**: The spreadsheet file not accessible.
- **500 Server Error**: The spreadsheet has encountered an anomaly in obtaining calculation data.

## Where should we use the Merge Spreadsheet in remote folder API?

When you need to merge multiple data files together, you can use this API.

## Why should you use the Merge Spreadsheet in remote folder API?

- **Developer-Friendly**: Aspose.Cells Cloud offers SDK libraries in multiple languages, enabling quick development and comes with comprehensive documentation. Compared to building custom chart rendering solutions, this significantly reduces the development workload.
- **Reduced Labor Costs**: Reduced the need for positions dedicated to document consolidation.
- **Pay-per-use**: No upfront investment, only pay for API calls actually used.
- **Zero Maintenance Costs**: No need to maintain servers, update software, or deal with compatibility issues.

## How to Use the Merge Spreadsheet in remote folder API with SDKs

### Merge Spreadsheet in remote folder API Specification

The [Merge Spreadsheet in remote folder API Specification](https://reference.aspose.cloud/cells/#/DataProcessingController/MergeSpreadsheetsInRemoteFolder) provides a publicly accessible programming interface allowing REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low-level details, allowing you to merge matching spreadsheet files into files in remote folder with short code.
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples illustrate how to interact with Aspose.Cells web services using various SDKs:
{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MergeSpreadsheetsInRemoteFolder.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MergeSpreadsheetsInRemoteFolder.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MergeSpreadsheetsInRemoteFolder.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MergeSpreadsheetsInRemoteFolder.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MergeSpreadsheetsInRemoteFolder.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MergeSpreadsheetsInRemoteFolder.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MergeSpreadsheetsInRemoteFolder.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MergeSpreadsheetsInRemoteFolder.go" >}}
{{</tab>}}
{{< /tabs >}}
