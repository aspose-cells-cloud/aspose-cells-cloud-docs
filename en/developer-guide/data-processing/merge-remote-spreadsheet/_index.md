---
title: "Aspose.Cells Cloud Web API - Merge one spreadsheet into another. "
second_title: Aspose.Cells Cloud"
ArticleTitle: "Merge one spreadsheet into another"
linktitle: "Merge Remote Spreadsheet"
type: docs
url: /merge-remote-spreadsheet/
keywords: "Merge spreadsheets, cloud storage, Aspose.Cells Cloud Web API, spreadsheet merging, XLSX, CSV, PDF"
description: "Combine a spreadsheet file stored in a cloud storage into another spreadsheet, and you can specify the format and location of the data output.."
weight: 100
kwords: "Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, JSON, Markdown, merge blank cells, cloud processing"
---

Combine a spreadsheet file stored in a cloud storage into another spreadsheet, and you can specify the format and location of the data output.

## **Merge Remote Spreadsheet API**

```http
PUT http://api.aspose.cloud/v4.0/cells/{name}/merge/spreadsheet
```

### **Request Parameters:**

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
| :- | :- | :- |:- |
|name|String|Path|The name of the workbook file to be merged.|
|mergedSpreadsheet|String|Query|The list of spreadsheet files to merge.|
|folder|String|Query|The folder path where the workbook is stored.|
|outFormat|String|Query|The output file format (e.g., XLSX, PDF).|
|mergeInOneSheet|Boolean|Query|Whether to combine all data into a single worksheet.|
|storageName|String|Query|(Optional) The name of the storage if using custom cloud storage. Defaults to default storage if omitted.|
|outPath|String|Query|(Optional) The folder path for the merged workbook. Defaults to null.|
|outStorageName|String|Query|The name of the storage for the output file.|
|fontsLocation|String|Query|Custom font location.|
|region|String|Query|The spreadsheet region setting.|
|password|String|Query|The password for accessing the spreadsheet file.|

### **Response**

```json
[
    {
        "Name": "ResponseFile",
        "DataType": {
            "Identifier": "File",
            "Reference": "Stream"
        }
    }
]
```

### Error Codes

- **400 Bad Request**: Invalid Aspose.Cells Cloud API URI.
- **401 Unauthorized**: Invalid access token. Or invalid client id and secret.
- **404 Not Found**: The spreadsheet file not accessible.
- **500 Server Error**: The spreadsheet has encountered an anomaly in obtaining calculation data.

## Where should we use the Merge Remote Spreadsheet API?

- When you need to merge multiple data files together in cloud storage.


## Why should you use the Merge Remote Spreadsheet API?

- Cloud storage files do not need to be downloaded, and can be merged directly in the cloud.
- Development can be quickly completed through the existing SDK.

## How to Use the Merge Remote Spreadsheet API with SDKs

### Merge Remote Spreadsheet API Specification

The [Merge Remote Spreadsheet API Specification](https://reference.aspose.cloud/cells/#/DataProcessingController/MergeRemoteSpreadsheet) provides a publicly accessible programming interface for executing REST interactions directly from a web browser.

## Excel API SDK

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low-level details, allowing you to merge a spreadsheet into  another spreadsheet with short code.
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.
The following code examples demonstrate how to interact with Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MergeRemoteSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MergeRemoteSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MergeRemoteSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MergeRemoteSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MergeRemoteSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MergeRemoteSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MergeRemoteSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MergeRemoteSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}
