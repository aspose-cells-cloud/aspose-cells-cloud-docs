---
title: "Aspose.Cells Cloud Web API - Export Spreadsheet Worksheet as Format"
second_title: "Aspose.Cells Cloud"
ArticleTitle: "Export Spreadsheet Worksheet as Format"
linktitle: "Export Worksheet"
type: docs
url: /export-worksheet-as-format/
keywords: "Export worksheet, Cloud storage conversion, File format transformation, API for spreadsheets"
description: "Efficiently converts a worksheet from cloud storage into various formats such as PDF, CSV, and images."
weight: 100
kwords: "Export worksheet, Cloud conversion, PDF, Image formats, Excel, REST API, CSV, JSON, Markdown, Handle blank cells in Excel"
---

Export a cloud spreadsheet/Excel worksheet to a another format file with the Aspose.Cells Cloud Web API.

## **Export Spreadsheet Worksheet as Format API**

```http
GET http://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}
```

## The request parameters of **exportWorksheetAsFormat** API are

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
| :- | :- | :- |:- |
|name|String|Path|(Required) The name of the workbook file to be retrieved.|
|worksheet|String|Path|(Required) The specific worksheet to convert.|
|format|String|Query|(Required) The desired output format (e.g., "png", "pdf", "svg").|
|folder|String|Query|(Optional) The folder path where the workbook is stored. The default is null.|
|storageName|String|Query|(Optional) The name of the custom cloud storage. Use default storage if omitted.|
|outPath|String|Query|(Optional) The output folder path. The default is null.|
|outStorageName|String|Query|(Optional) Output file Storage Name.|
|fontsLocation|String|Query|(Optional) Specify custom fonts if needed.|
|region|String|Query|The spreadsheet region setting.|
|password|String|Query|The password for accessing the spreadsheet file.|

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

## Why should you use the Export Spreadsheet Worksheet as Format API?

- You can convert cloud files to different formats anytime and anywhere.
- Development can be quickly completed through the existing SDK.

## How to Use the Export Spreadsheet Worksheet as Format API with SDKs?

### OpenAPI Specification

The [OpenAPI Specifiation](https://reference.aspose.cloud/cells/#/ConversionController/ExportWorksheetAsFormat) provides a publicly accessible programming interface for performing REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the best way to accelerate development. The SDK handles the underlying details, allowing you to simply implement export cloud spreadsheet/Excel worksheet to another format file for cells with minimal code.
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportWorksheetAsFormat.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportWorksheetAsFormat.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportWorksheetAsFormat.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportWorksheetAsFormat.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportWorksheetAsFormat.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportWorksheetAsFormat.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportWorksheetAsFormat.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportWorksheetAsFormat.go" >}}
{{</tab>}}
{{< /tabs >}}
