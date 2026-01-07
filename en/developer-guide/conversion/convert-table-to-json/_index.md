---
title: "Aspose.Cells Cloud Web API - Convert Local Excel Table data to a JSON file - Free Online Tool"
second_title: "Document"
ArticleTitle: "How to Convert the Local Spreadsheet data of Table to a JSON file: Step-by-Step Guide"
linktitle: "Convert Table to JSON"
type: docs
url: /convert-table-to-json/
keywords: "Excel API, JSON conversion, spreadsheet to JSON, cloud file conversion, REST API, Aspose.Cells"
description: "Convert a local spreadsheet table to JSON format efficiently using the Excel API. This method enables seamless file processing without the need for cloud storage."
weight: 100
kwords: "Excel API, JSON conversion, cloud file conversion, spreadsheet, REST API, Aspose.Cells, local drive processing, file format conversion"
---

Convert a local spreadsheet/Excel table to a json file with the Aspose.Cells Cloud Web API.

## **Convert Table to JSON API**

### API Endpoint

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/table/json
```

### **Request Parameters:**

| Parameter Name    | Type  | Path/Query String/HTTP Body | Description                                        |
|-------------------|-------|-----------------------------|----------------------------------------------------|
| Spreadsheet       | File  | FormData                    | Upload the spreadsheet file.                       |
| worksheet         | String| Query                       | Specify the worksheet name of the spreadsheet.     |
| tableName         | String| Query                       | Provide the name of the table to convert.          |
| outPath           | String| Query                       | (Optional) The folder path where the workbook is stored; defaults to null. |
| outStorageName    | String| Query                       | Specify the output file storage name.              |
| fontsLocation     | String| Query                       | Use custom fonts for conversion.                   |
| region            | String| Query                       | Define the region settings for the spreadsheet.    |
| password          | String| Query                       | The password required to open the spreadsheet file. |

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
- **401 Unauthorized**: Invalid access token. Or invalid client id and secret.
- **404 Not Found**: The spreadsheet file not accessible.
- **500 Server Error**: The spreadsheet has encountered an anomaly in obtaining calculation data.

## **Where Should You Use the Convert Table to JSON API?**

- **Real-time Dashboards**: Convert live Excel data to JSON for real-time charting libraries (Chart.js, D3.js).
- **Spreadsheet-as-Service**: Excel table as JSON endpoints for other microservices to consume.
- **Webhook Payloads**: Convert spreadsheet data to JSON for webhook notifications.
- **Rapid Data Prototyping**: Quick conversion of cleaned Excel data to JSON for Python/R analysis.
- **Machine Learning Pipelines**: Preprocess training data from business-maintained spreadsheets.
- **E-commerce Operations**: Transform product catalogs or pricing sheets to JSON for website sync.
- **Reporting Automation**: Generate JSON data feeds from financial models for automated reportin.
- **App Configuration**: Manage feature flags, settings, or A/B test parameters in Excel → JSON
- **Multi-language Support**: Convert localization spreadsheets to JSON for i18n libraries
- **Dynamic Menus/Navigation**: Manage website navigation structures in Excel, deploy as JSON

## Why should you use the Convert Table to JSON API?

- **Developer-Friendly**: Aspose.Cells Cloud offers SDK libraries in multiple languages, enabling quick development and comes with comprehensive documentation. Compared to building custom chart rendering solutions, this significantly reduces the development workload.
- **Cost-Effective**: You can convert table data without first uploading the workbook, which saves storage space and reduces costs.
- **To Fuel Modern Web & Mobile Applications**: JSON is the native data language of the web.  By converting Excel table to JSON, you can **seamlessly feed live spreadsheet data into JavaScript frameworks** (React, Vue, Angular), mobile apps, or single-page applications (SPAs) without complex parsing logic.
- **JSON is the lingua franca of modern systems**: compatible with virtually every programming language, database, and web service.  Unlike proprietary formats, JSON ensures your Excel data can be consumed anywhere.
- **Structured Data Preservation**
  - **Intelligent Structure Detection**: Automatically converts tabular data to proper JSON arrays/objects
  - **Header Mapping**: Uses first row as JSON keys for clean object structures
  - **Data Type Retention**: Preserves number, date, and boolean types (not just text)

## How to Use the Convert Table to JSON API with SDKs?

### Convert Table to JSON API Specification

The [Convert Table to JSON API Specification](https://reference.aspose.cloud/cells/#/ConversionController/ConvertTableToJson) provides a publicly accessible programming interface, enabling REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low-level details, allowing you to convert a spreadsheet table data to a json file with short code.
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to interact with Aspose.Cells web services using various SDKs:
{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToJson.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToJson.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToJson.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToJson.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToJson.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToJson.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToJson.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToJson.go" >}}
{{</tab>}}
{{< /tabs >}}
