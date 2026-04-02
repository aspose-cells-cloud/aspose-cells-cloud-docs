---
title: "Aspose.Cells Cloud Web API - Convert Excel Chart to Image - Free Online Tool"
second_title: "Document"
ArticleTitle: "How to Convert Spreadsheet Chart to Image: Step-by-Step Guide"
linktitle: "Convert Chart to Image"
type: docs
url: /convert-chart-to-image/
keywords: "convert chart to image, excel chart to png, excel chart to svg, excel chart to jpg, excel chart to bmp, excel chart to tiff"
description: "Use Aspose.Cells Cloud Web API to convert an Excel chart into PNG, SVG, TIFF, JPEG, or BMP images directly from a spreadsheet file."
weight: 100
---

Convert a chart from a local spreadsheet or Excel file to an image file. Supported **IMAGE FORMATS:** [PNG](https://docs.fileformat.com/image/png/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/)

## **Convert Chart to Image API**

### API Endpoint

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/chart/image
```

### **Request Parameters:**

| Parameter Name | Type    | Path/Query String/HTTPBody | Description                                                                |
| :------------- | :------ | :------------------------- | :------------------------------------------------------------------------- |
| Spreadsheet    | File    | FormData                   | Upload the spreadsheet file containing the chart.                          |
| worksheet      | String  | Query                      | Specify the worksheet name if applicable.                                  |
| chartIndex     | Integer | Query                      | Index of the chart to convert.                                             |
| format         | String  | Query                      | (Required) The desired image type (e.g., svg, png, jpg).                   |
| outPath        | String  | Query                      | (Optional) The folder path where the output file will be stored; defaults to null. |
| outStorageName | String  | Query                      | Name of the storage for the output file.                                   |
| fontsLocation  | String  | Query                      | Specify custom fonts if needed.                                            |
| region         | String  | Query                      | Set the spreadsheet region.                                                |
| password       | String  | Query                      | The password for opening the spreadsheet file.                             |

## **Response**

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
- **500 Server Error**: The spreadsheet encountered an error while obtaining calculation data.

## Where should you use the Convert Chart to Image API?

- **Report Generation & Dashboards**: Automatically convert charts from Excel data into images (PNG, JPEG, etc.) for embedding in PDF reports, web dashboards, or PowerPoint presentations.  
- **Web/Email Applications**: Serve chart images directly in web pages or emails without requiring users to download or open Excel files. Useful for dynamic reporting tools, newsletters, or automated notifications.  
- **Document Processing Workflows**: Integrate into automated pipelines (e.g., invoicing, analytics) where charts from Excel need to be inserted into other formats (Word, PDF, HTML).  
- **Mobile/Desktop Applications**: Display Excel charts in apps where rendering the full spreadsheet is unnecessary or impractical.  
- **Archiving & Visualization**: Save charts as standalone images for long‑term storage, thumbnails, or quick previews without Excel dependencies.

## Why should you use the Convert Chart to Image API?

- **Preserve Visual Fidelity**: Maintains exact chart formatting (colors, labels, scaling) as seen in Excel, ensuring professional‑quality output.  
- **Platform Agnostic**: No Excel installation required. Works cross‑platform (Windows, Linux, macOS) via REST API, suitable for cloud‑based or server‑side applications.  
- **Automation & Scalability**: Batch‑convert multiple charts or files programmatically, saving time compared to manual export. Handles large volumes efficiently in the cloud.  
- **Flexible Output Formats**: Supports popular image formats (PNG, JPG, BMP, SVG, etc.), allowing integration with diverse systems and media.  
- **Secure & Reliable**: Process files in Aspose’s cloud environment without exposing sensitive data to client‑side tools. High availability and consistent performance.  
- **Developer‑Friendly**: Aspose.Cells Cloud offers SDK libraries in multiple languages, enabling quick development and comes with comprehensive documentation. Compared to building custom chart rendering solutions, this significantly reduces the development workload.  
- **Cost‑Effective**: You can convert charts without uploading the workbook first, which saves storage space and reduces costs.

## How to Use the Convert Chart to Image API with SDKs?

### Convert Chart to Image API Specification

The [Convert Chart to Image API Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertChartToImage) defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to convert a chart to an image with short code.  
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertChartToImage.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertChartToImage.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertChartToImage.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertChartToImage.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertChartToImage.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertChartToImage.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertChartToImage.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertChartToImage.go" >}}
{{</tab>}}
{{< /tabs >}}