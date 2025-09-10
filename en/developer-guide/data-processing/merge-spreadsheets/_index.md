---
title: "Aspose.Cells Cloud Web API - Merge multiple Spreadsheets into a single spreadsheet."
second_title: "Aspose.Cells Cloud"
ArticleTitle: "Merge multiple Spreadsheets into a single spreadsheet."
linktitle: "Merge Spreadsheets"
type: docs
url: /merge-spreadsheets/
keywords: "Merge spreadsheets, data merging, file format conversion, REST, XLSX, CSV, PDF"
description: "Easily merge local spreadsheet files into various formats (XLSX, CSV, PDF) using the Excel API."
weight: 100
kwords: "Excel API, Merge spreadsheets, Office Cloud, REST API, Spreadsheet merging, CSV format, JSON, Markdown"
---

Merge multiple local spreadsheet files into a single file, while supporting output in 30+ of file formats.

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
            "Reference": "Stream"
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

Using the SDK is the fastest way to develop, as it abstracts away the low-level details, allowing you to merge multiple spreadsheets into  a spreadsheet with short code.
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples illustrate how to make calls to Aspose.Cells web services using various SDKs:
{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MergeSpreadsheets.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MergeSpreadsheets.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MergeSpreadsheets.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MergeSpreadsheets.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MergeSpreadsheets.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MergeSpreadsheets.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MergeSpreadsheets.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MergeSpreadsheets.go" >}}
{{</tab>}}
{{< /tabs >}}
