---
title: "Aspose.Cells Cloud Web API - Split Spreadsheet in the Cloud"
second_title: "Aspose.Cells Cloud"
ArticleTitle: "Split Spreadsheets into multiple files in the Cloud"
linktitle: "Split Remote Spreadsheet in Cloud"
type: docs
url: /split-remote-spreadsheet/
keywords: "spreadsheet splitting, cloud spreadsheet API, Excel remote processing, split Excel file, multi-format output, cloud storage integration"
description: "Efficiently split a spreadsheet stored in cloud storage into multiple output formats without downloading."
weight: 100
kwords: "Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, JSON, Markdown, split remote spreadsheet, cloud processing, multi-file output"
---

Split a spreadsheet stored in cloud storage into multiple files. Support 30+ outfile formats.

## **Split Remote Spreadsheet API**

```http
PUT http://api.aspose.cloud/v4.0/cells/{name}/split/spreadsheet
```

### **Request Parameters:**

| Parameter Name | Type | Path/Query String/HTTP Body | Description |
| :- | :- | :- |:- |
| name | String | Path | The name of the workbook file to be split. |
| folder | String | Query | The folder path where the workbook is stored. |
| from | Integer | Query | Begin worksheet index. |
| to | Integer | Query | End worksheet index. |
| outFormat | String | Query | The desired output format (e.g., "Xlsx", "Pdf", "Csv"). |
| storageName | String | Query | (Optional) The name of the storage if using custom cloud storage. Use default storage if omitted. |
| outPath | String | Query | (Optional) The folder path where the workbook is stored. The default is null. |
| outStorageName | String | Query | Output file storage name. |
| fontsLocation | String | Query | Use custom fonts. |
| region | String | Query | The spreadsheet region setting. |
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

## Where should we use the Split Remote Spreadsheet API?

When you need to merge multiple data files together, you can use this API.

## Why should you use the Split Remote Spreadsheet API?

- Cloud storage files do not need to be downloaded, and can be split directly in the cloud.
- Development can be quickly completed through the existing SDK.

## How to Use the Split Remote Spreadsheet API with SDKs

### OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/DataProcessingController/SplitRemoteSpreadsheet) defines a publicly accessible programming interface and enables REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the best way to accelerate development. The SDK handles the underlying details, allowing you to simply implement split remote spreadsheet for cells with minimal code.
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.
The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SplitFileInRemote.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SplitFileInRemote.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SplitFileInRemote.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SplitFileInRemote.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SplitFileInRemote.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SplitFileInRemote.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SplitFileInRemote.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SplitFileInRemote.go" >}}
{{</tab>}}
{{< /tabs >}}
