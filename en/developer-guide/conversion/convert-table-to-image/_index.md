---
title: "Aspose.Cells Cloud Web API - Convert Local Excel Table data to an Image file - Free Online Tool"
second_title: "Document"
ArticleTitle: "How to Convert the Local Spreadsheet data of Table to an Image file: Step-by-Step Guide"
linktitle: "Convert Table to Image"
type: docs
url: /convert-table-to-image/
keywords: "table to image, Aspose.Cells Cloud Web API, cloud conversion, spreadsheet to image, image formats, Excel, Office Cloud, REST API, convert table to image, cloud conversion, image file formats, spreadsheet conversion"
description: "Convert a local spreadsheet table into an image file efficiently using the Aspose.Cells Cloud Web API."
weight: 100
---

Export data of table from a local Excel Files to an [Image](https://docs.fileformat.com/image/) file using Cloud API.

**Supported IMAGE FORMATS:**

- [PNG](https://docs.fileformat.com/image/png/)
- [SVG](https://docs.fileformat.com/page-description-language/svg/)
- [TIFF](https://docs.fileformat.com/image/tiff/)
- [JPEG](https://docs.fileformat.com/image/jpeg/)
- [BMP](https://docs.fileformat.com/image/bmp/)

## **Convert Table to Image API**

### API Endpoint

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/table/image
```

### **Request Parameters:**

| Parameter Name | Type | Path/Query String/HTTP Body | Description |
| :- | :- | :- |:- |
|Spreadsheet|File|FormData|Upload the spreadsheet file.|
|worksheet|String|Query|The worksheet name of Spreadsheet/Excel|
|tableName|String|Query|Name of the table to convert.|
|format|String|Query|Desired image file format (e.g., png, svg).|
|outPath|String|Query|(Optional) The folder path where the converted image will be stored. Defaults to null.|
|outStorageName|String|Query|Specify the output file storage name.|
|fontsLocation|String|Query|Use custom fonts if required.|
|region|String|Query|Defines the spreadsheet region settings.|
|password|String|Query|Password required to access the spreadsheet file.|

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

## **Where Should You Use the Convert Table to Image API?**

- **Static Report Snapshots**: Convert financial data table, tables, or calculations into images for inclusion in PDF reports, PowerPoint slides, or printed documents where editing is not required.
- **Data Visualization in Presentations**: Turn complex spreadsheet tables containing formatted tables, conditional formatting, or simple data visualizations into images to embed in presentations (PPTX, Google Slides).
- **Documentation & Training Materials**: Capture spreadsheet examples, templates, or data entry forms as images for user manuals, tutorials, or knowledge base articles.
- **Thumbnail Previews**: Create small image previews of key spreadsheet sections for file browsers, document libraries, or search results.

## Why should you use the Convert Table to Image API?

- **Developer-Friendly**: Aspose.Cells Cloud offers SDK libraries in multiple languages, enabling quick development and comes with comprehensive documentation. Compared to building custom chart rendering solutions, this significantly reduces the development workload.
- **Cost-Effective**: You can convert charts without first uploading the workbook, which saves storage space and reduces costs.
- **Pixel-Perfect Preservation**: Faithfully replicates Excel’s appearance—including cell formatting, formulas (as displayed values), borders, colors, and conditional formatting—in the output image.
- **Universal Compatibility**:Image formats (PNG, JPEG, TIFF, BMP, SVG, and so on.) are viewable on any device or platform without specialized software, ensuring maximum accessibility.

## How to Use the Convert Table to Image API with SDKs?

### Convert Table to Image API Specification

The [Convert Table to Image API Specification](https://reference.aspose.cloud/cells/#/ConversionController/ConvertTableToImage) provides a publicly accessible programming interface for conducting REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low-level details, allowing you to convert a spreadsheet table data to an image with short code.
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples illustrate how to invoke Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToSvg.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToSvg.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToSvg.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToSvg.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToSvg.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToSvg.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToSvg.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToSvg.go" >}}
{{</tab>}}
{{< /tabs >}}
