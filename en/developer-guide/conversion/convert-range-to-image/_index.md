---
title: "Aspose.Cells Cloud Web API - Convert Local Excel Range Data to an Image File - Free Online Tool"
second_title: "Document"
ArticleTitle: "How to Convert Local Spreadsheet Range Data to an Image File: Step‑by‑Step Guide"
linktitle: "Convert Range to Image"
type: docs
url: /convert-range-to-image/
keywords: "Aspose.Cells Cloud, Convert Range to Image, Spreadsheet to Image, Cloud Conversion, Image Formats, REST API, PNG, SVG, TIFF, JPEG, BMP"
description: "Use Aspose.Cells Cloud REST API to convert a specific range from a local Excel file (XLSX or XLS) into various image formats such as PNG, JPEG, SVG, TIFF, or BMP without uploading the entire workbook."
weight: 100
---

Export data of a range from a local Excel file to an [Image](https://docs.fileformat.com/image/) file using the Cloud API.

**Supported IMAGE FORMATS:**

- [PNG](https://docs.fileformat.com/image/png/)
- [SVG](https://docs.fileformat.com/page-description-language/svg/)
- [TIFF](https://docs.fileformat.com/image/tiff/)
- [JPEG](https://docs.fileformat.com/image/jpeg/)
- [BMP](https://docs.fileformat.com/image/bmp/)

## **Convert Range to Image API**

### API Endpoint

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/range/image
```

### **Request Parameters:**

| Parameter Name | Type    | Path/Query String/HTTPBody | Description                                                               |
| :------------- | :------ | :------------------------- | :------------------------------------------------------------------------ |
| Spreadsheet    | File    | FormData                   | Upload the spreadsheet file for conversion.                               |
| worksheet      | String  | Query                      | The worksheet name of the spreadsheet.                                    |
| range          | String  | Query                      | Define the cell area to convert (e.g., A1:C10).                           |
| format         | String  | Query                      | Specify the output file format (e.g., png, svg, tiff).                    |
| printHeadings  | Boolean | Query                      | Indicate if row and column headings should be printed.                    |
| outPath        | String  | Query                      | (Optional) The folder path where the workbook is stored; default is null. |
| outStorageName | String  | Query                      | Name of the output file storage.                                          |
| fontsLocation  | String  | Query                      | Custom fonts to use for the conversion.                                   |
| region         | String  | Query                      | Define the spreadsheet region setting.                                    |
| password       | String  | Query                      | Password for opening the spreadsheet file if it is protected.            |

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
- **401 Unauthorized**: Invalid access token, or invalid client ID and secret.  
- **404 Not Found**: The spreadsheet file is not accessible.  
- **500 Server Error**: The spreadsheet encountered an anomaly while obtaining calculation data.

## **Where Should You Use the Convert Range to Image API?**

- **Static Report Snapshots**: Convert financial data ranges, tables, or calculations into images for inclusion in PDF reports, PowerPoint slides, or printed documents where editing is not required.  
- **Data Visualization in Presentations**: Turn complex spreadsheet ranges containing formatted tables, conditional formatting, or simple data visualizations into images to embed in presentations (PPTX, Google Slides).  
- **Documentation & Training Materials**: Capture spreadsheet examples, templates, or data‑entry forms as images for user manuals, tutorials, or knowledge‑base articles.  
- **Thumbnail Previews**: Create small image previews of key spreadsheet sections for file browsers, document libraries, or search results.

## Why Should You Use the Convert Range to Image API?

- **Developer‑Friendly**: Aspose.Cells Cloud offers SDK libraries in multiple languages, enabling quick development and comes with comprehensive documentation. Compared with building custom chart‑rendering solutions, this significantly reduces development workload.  
- **Cost‑Effective**: You can convert range data without first uploading the entire workbook, which saves storage space and reduces costs.  
- **Pixel‑Perfect Preservation**: Faithfully replicates Excel’s appearance—including cell formatting, formulas (as displayed values), borders, colors, and conditional formatting—in the output image.  
- **Universal Compatibility**: Image formats (PNG, JPEG, TIFF, BMP, SVG, and others) are viewable on any device or platform without specialized software, ensuring maximum accessibility.

## How to Use the Convert Range to Image API with SDKs?

### Convert Range to Image API Specification

The [Convert Range to Image API Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToImage) provides a publicly accessible programming interface, enabling REST interactions directly from your web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away low‑level details, allowing you to convert range data to an image with minimal code.  
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples illustrate how to call Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToImage.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToImage.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToImage.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToImage.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToImage.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToImage.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToImage.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToImage.go" >}}
{{</tab>}}
{{< /tabs >}}