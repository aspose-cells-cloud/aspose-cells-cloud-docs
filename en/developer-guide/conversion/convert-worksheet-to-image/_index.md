---
title: "Aspose.Cells Cloud Web API - Convert a Spreadsheet Worksheet to an Image"
second_title: "Document"
ArticleTitle: "Convert a Spreadsheet Worksheet to an Image"
linktitle: "Convert Worksheet to Image"
type: docs
url: /convert-worksheet-to-image/
keywords: "Aspose.Cells Cloud Web API, Convert Worksheet to Image, Cloud Conversion, Image Format Conversion, Excel to Image, REST"
description: "Convert a spreadsheet worksheet from a local drive into various image formats efficiently using Aspose.Cells API."
weight: 100
kwords: Excel, Office Cloud, REST API, Spreadsheet, Image Conversion, SVG, PNG, TIFF, Cloud Services, Local to Cloud Conversion, Match all blank cells in an Excel worksheet
---

Convert a local spreadsheet/Excel worksheet to an image.

## **Convert Worksheet to Image API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/worksheet/image
```

### **Request Parameters:**

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
| :- | :- | :- |:- |
| Spreadsheet | File | FormData | Upload the spreadsheet file. |
| worksheet | String | Query | Name of the worksheet in the spreadsheet. |
| format | String | Query | Desired image format: svg, png, tiff, etc. |
| outPath | String | Query | (Optional) The folder path where the workbook is stored. The default is null. |
| outStorageName | String | Query | Name of the output file storage. |
| fontsLocation | String | Query | Use custom fonts. |
| region | String | Query | The spreadsheet region setting. |
| password | String | Query | The password for opening the spreadsheet file. |

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

## Why should you use the Convert Table to Image API?

- No need for cloud storage, reducing the burden on cloud resources.
- Development can be quickly completed through the existing SDK.

## How to Use the Convert Table to Image API with SDKs?

### Convert Table to Image API Specification

The [Convert Table to Image API Specification](https://reference.aspose.cloud/cells/#/ConversionController/ConvertWorksheetToImage) defines a publicly accessible programming interface and allows for REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low-level details, allowing you to convert a spreadsheet table data to an image with short code.
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertWorksheetToSvg.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertWorksheetToSvg.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertWorksheetToSvg.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertWorksheetToSvg.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertWorksheetToSvg.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertWorksheetToSvg.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertWorksheetToSvg.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertWorksheetToSvg.go" >}}
{{</tab>}}
{{< /tabs >}}
