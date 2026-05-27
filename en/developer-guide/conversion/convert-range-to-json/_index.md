---
title: "Convert Excel Range to JSON – Aspose.Cells Cloud API (v4.0)"
second_title: "Document"
ArticleTitle: "Step-by-Step Guide to Convert a Local Spreadsheet Range to JSON with Aspose.Cells Cloud"
linktitle: "Convert Range to JSON"
type: docs
url: /convert-range-to-json/
keywords: "convert Excel range to JSON, Aspose.Cells Cloud API, spreadsheet to JSON, Excel range conversion, cloud API"
description: "Convert a specific range from a local Excel file to JSON using Aspose.Cells Cloud API. Learn request parameters, sample response, error codes, and SDK examples."
weight: 100
---

Export range data from a local Excel file to a JSON file using the Cloud API.

## Convert Range to JSON API

### Web API

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/range/json
```

### Request Parameters:

| Parameter Name | Type   | Path/Query String/HTTP Body | Description                                                           |
| -------------- | ------ | --------------------------- | --------------------------------------------------------------------- |
| Spreadsheet    | File   | FormData                    | Upload the spreadsheet file.                                          |
| worksheet      | String | Query                       | Name of the worksheet in the spreadsheet.                             |
| range          | String | Query                       | Cell area to convert, e.g., A1:C10.                                   |
| outPath        | String | Query                       | (Optional) Folder path where the workbook is stored; default is null. |
| outStorageName | String | Query                       | Name of the output file storage.                                      |
| fontsLocation  | String | Query                       | Location for storing custom fonts for home use.                       |
| region         | String | Query                       | The spreadsheet region setting.                                       |
| password       | String | Query                       | Password for opening the spreadsheet file.                            |

### Response

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
- **500 Server Error**: The spreadsheet has encountered an anomaly in obtaining calculation data.

## Where Should You Use the Convert Range to JSON API?

- **Real-time Dashboards**: Convert live Excel data to JSON for real‑time charting libraries (Chart.js, D3.js).  
- **Spreadsheet-as-Service**: Excel ranges as JSON endpoints for other microservices to consume.  
- **Webhook Payloads**: Convert spreadsheet data to JSON for webhook notifications.  
- **Rapid Data Prototyping**: Quick conversion of cleaned Excel data to JSON for Python/R analysis.  
- **Machine Learning Pipelines**: Pre‑process training data from business‑maintained spreadsheets.  
- **E-commerce Operations**: Transform product catalogs or pricing sheets to JSON for website sync.  
- **Reporting Automation**: Generate JSON data feeds from financial models for automated reporting.  
- **App Configuration**: Manage feature flags, settings, or A/B test parameters in Excel → JSON.  
- **Multi-language Support**: Convert localization spreadsheets to JSON for i18n libraries.  
- **Dynamic Menus/Navigation**: Manage website navigation structures in Excel, deploy as JSON.

## Why Should You Use the Convert Range to JSON API?

- **Developer‑Friendly**: Aspose.Cells Cloud offers SDK libraries in multiple languages, enabling quick development and comes with comprehensive documentation. Compared to building custom chart‑rendering solutions, this significantly reduces the development workload.  
- **Cost‑Effective**: You can convert range data without first uploading the workbook, which saves storage space and reduces costs.  
- **Fuel Modern Web & Mobile Applications**: JSON is the native data language of the web. By converting Excel ranges to JSON, you can seamlessly feed live spreadsheet data into JavaScript frameworks (React, Vue, Angular), mobile apps, or single‑page applications (SPAs) without complex parsing logic.  
- **JSON Is the Lingua Franca of Modern Systems**: Compatible with virtually every programming language, database, and web service. Unlike proprietary formats, JSON ensures your Excel data can be consumed anywhere.  
- **Structured Data Preservation**  
  - **Intelligent Structure Detection**: Automatically converts tabular data to proper JSON arrays/objects.  
  - **Header Mapping**: Uses first row as JSON keys for clean object structures.  
  - **Data Type Retention**: Preserves number, date, and boolean types (not just text).

## How to Use the Convert Range to JSON API with SDKs?

### Convert Range to JSON API Specification

The [Convert Range to JSON API Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToJson) defines a publicly accessible programming interface and allows you to carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to convert a range of data to a JSON file with concise code.  
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:
{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToJson.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToJson.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToJson.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToJson.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToJson.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToJson.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToJson.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToJson.go" >}}
{{</tab>}}
{{< /tabs >}}