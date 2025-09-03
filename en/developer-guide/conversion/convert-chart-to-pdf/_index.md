---
title: "Convert Chart to PDF - Excel API"
second_title: "Aspose.Cells Cloud"
linktitle: "Convert Chart to PDF"
type: docs
url: /convert-chart-to-pdf/
keywords: "chart to pdf, convert spreadsheet to pdf, Aspose API, cloud conversion, Excel to PDF"
description: "This API converts charts from spreadsheets located on a local drive to PDF format seamlessly."
weight: 100
kwords: "Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, JSON, Markdown, Convert Chart to PDF, Cloud-Native Conversion"
---

# **Excel API: ConvertChartToPdf**

## **Overview**

This API converts charts from spreadsheets on a local drive to PDF format seamlessly.

## **Function Description**

This method reads a spreadsheet file containing a chart from the local file system, converts it into the desired PDF format, and returns the converted result. The source file path and target format must be specified correctly. Ensure that the necessary permissions are in place to read the source file and write the converted file, if applicable. The conversion process occurs entirely on the cloud server, eliminating the need for any cloud storage or external downloads. If the source file does not exist, is inaccessible, or if an error occurs during the conversion process, an appropriate exception will be thrown. Supported formats for conversion depend on the available libraries and their capabilities.

## **API Endpoint**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/chart/pdf
```

## The request parameters of **convertChartToPdf** API are

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

## **Response Structure**

```json
{
File
}
```

## Error Handling

- **400 Bad Request**: Invalid URL or parameters.
- **401 Unauthorized**: Authentication has failed, or no credentials were provided.
- **404 Not Found**: Source file not accessible.
- **500 Server Error**: An anomaly occurred while obtaining conversion data from the spreadsheet.

## Usage Scenarios

## Key Features and Benefits

- **Cloud-Native Conversion**: Convert local files directly in the cloud, eliminating the need to store them there.
- **Reduced Cloud Resource Burden**: No need to upload files to the cloud, saving cloud storage space.
- **Simplified Workflow**: Convert local spreadsheets to PDF format directly through cloud services, without intermediate steps.

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/ConversionController/ConvertChartToPdf) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

## Excel API SDK

Using an SDK is the best way to speed up development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

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
