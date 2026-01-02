---
title: "Aspose.Cells Cloud Web API - Merge matching spreadsheet files into a file in a remote Folder."
second_title: "Document"
ArticleTitle: "Merge matching spreadsheet files into a file in a remote Folder."
linktitle: "Merge Spreadsheets in Remote Folder"
type: docs
url: /merge-spreadsheets-in-remote-folder/
keywords: "Merge spreadsheets, cloud storage, Excel API, remote processing, spreadsheet formats, REST API"
description: "Combine the spreadsheet files stored in the cloud storage into one file, and the file format supports 30 formats for output, such as PDF,CSV, JSON and other common formats."
weight: 100
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, JSON, Markdown, Merge spreadsheets, Cloud processing, Remote file handling
---

Merge matching spreadsheet files into files in remote folder, the output file format supports 30+ formats such as PDF,CSV,Json and other common formats.


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

- **400 Bad Request**: Invalid Aspose.Cells Cloud API URI.
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
