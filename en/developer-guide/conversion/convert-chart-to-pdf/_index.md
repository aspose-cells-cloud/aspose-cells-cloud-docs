---
title: "Aspose.Cells Cloud Web API - Converting Spreadsheet Chart to Pdf"
second_title: "Aspose.Cells Cloud"
ArticleTitle: Converting Spreadsheet Chart to Image
linktitle: "Convert Chart to PDF"
type: docs
url: /convert-chart-to-pdf/
keywords: "convert chart to pdf, convert spreadsheet to pdf, Aspose API, cloud conversion, Excel to PDF"
description: "This API converts charts from spreadsheets located on a local drive to PDF file seamlessly."
weight: 100
kwords: "Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, JSON, Markdown, Convert Chart to PDF, Cloud-Native Conversion"
---

Convert a chart from a local spreadsheet/Excel file to a [PDF](https://docs.fileformat.com/pdf/) file with the Aspose.Cells Cloud Web API.

## **Convert Chart to Pdf API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/chart/pdf
```

### **Request Parameters:**

| Parameter Name       | Type   | Path/Query String/HTTPBody | Description                                               |
| -------------------- | ------ | --------------------------- | --------------------------------------------------------- |
| Spreadsheet          | File   | FormData                   | Upload the spreadsheet file.                              |
| worksheet            | String | Query                      | The name of the worksheet containing the chart.          |
| chartIndex           | Integer| Query                      | The index of the chart to convert.                       |
| outPath             | String | Query                      | (Optional) The folder path where the converted file is stored. The default is null. |
| outStorageName       | String | Query                      | Output file storage name.                                 |
| fontsLocation        | String | Query                      | Use custom fonts if required.                             |
| region               | String | Query                      | The spreadsheet region setting.                           |
| password             | String | Query                      | The password for opening the spreadsheet file.           |

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

## Why should you use the Convert Chart to Pdf API?

- No need for cloud storage, reducing the burden on cloud resources.
- Development can be quickly completed through the existing SDK.

## How to Use the Convert Chart to Pdf API with SDKs?

### OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/ConversionController/ConvertChartToPdf) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

## Use Aspose.Cells Cloud SDKs

Using the SDK is the best way to accelerate development. The SDK handles the underlying details, allowing you to simply implement convert spreadsheet/Excel chart to pdf for cells with minimal code.
The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertChartToPdf.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertChartToPdf.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertChartToPdf.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertChartToPdf.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertChartToPdf.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertChartToPdf.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertChartToPdf.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertChartToPdf.go" >}}
{{</tab>}}
{{< /tabs >}}
