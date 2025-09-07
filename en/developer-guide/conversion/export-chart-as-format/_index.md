---
title: "Aspose.Cells Cloud Web API - Export Spreadsheet Chart as Format"
second_title: "Aspose.Cells Cloud"
ArticleTitle: "Export Spreadsheet Chart as Format"
linktitle: "Export Chart as Format"
type: docs
url: /export-chart-as-format/
keywords: "Export Chart, Cloud Storage API, Spreadsheet Conversion, PDF Export, Image Export, REST API, Excel, CSV, JSON"
description: "Efficiently converts charts from spreadsheets stored in cloud to specified formats like PDF or image directly without downloading."
weight: 100
kwords: "Export Chart, Cloud Storage, REST API, Spreadsheet Conversion, PDF, CSV, JSON, Markdown, Excel, Image Formats"
---

Export a cloud spreadsheet/Excel chart to a another format file with the Aspose.Cells Cloud Web API.

## **Export Chart as Format API**

```http
GET http://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/charts/{chartIndex}
```

### **Request Parameters:**

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
| :- | :- | :- |:- |
| name | String | Path | (Required) The name of the workbook file to be retrieved. |
| worksheet | String | Path | Worksheet name |
| chartIndex | Integer | Path | Chart index |
| format | String | Query | (Required) The desired output format (e.g., "png", "pdf", "svg"). |
| folder | String | Query | (Optional) The folder path where the workbook is stored; defaults to null. |
| storageName | String | Query | (Optional) The name of the storage if using custom cloud storage; use default storage if omitted. |
| outPath | String | Query | (Optional) The folder path where the workbook is stored; defaults to null. |
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

## Why should you use the Export Spreadsheet Chart as Format API?

- You can convert cloud files to different formats anytime and anywhere.
- Development can be quickly completed through the existing SDK.

## How to Use the Export Spreadsheet Chart as Format API with SDKs?

### OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/ConversionController/ExportChartAsFormat) defines a publicly accessible programming interface, allowing you to carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the best way to accelerate development. The SDK handles the underlying details, allowing you to simply implement export cloud spreadsheet/Excel chart to another format file for cells with minimal code.
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.
The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportChartAsFormat.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportChartAsFormat.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportChartAsFormat.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportChartAsFormat.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportChartAsFormat.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportChartAsFormat.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportChartAsFormat.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportChartAsFormat.go" >}}
{{</tab>}}
{{< /tabs >}}
