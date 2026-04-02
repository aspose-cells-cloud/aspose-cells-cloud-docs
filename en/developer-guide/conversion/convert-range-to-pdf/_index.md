---
title: "Aspose.Cells Cloud Web API - Convert Local Excel Range Data to a PDF File - Free Online Tool"
second_title: "Document"
ArticleTitle: "How to Convert Local Spreadsheet Range Data to a PDF File: Step-by-Step Guide"
linktitle: "Convert Range to PDF"
type: docs
url: /convert-range-to-pdf/
keywords: "Aspose.Cells Cloud, Convert Range to PDF, Excel to PDF, Spreadsheet Conversion API, REST API, Cloud Conversion"
description: "Easily convert a specific range from a local Excel spreadsheet to a PDF file using Aspose.Cells Cloud's REST API."
weight: 100
---

Export a range of data from a local Excel file to a [PDF](https://docs.fileformat.com/pdf/) file using the Cloud API.

## **Convert Range to PDF API**

### API Endpoint

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/range/pdf
```

### **Request Parameters:**

| Parameter Name | Type   | Path/Query String/HTTP Body | Description                                                                   |
| -------------- | ------ | --------------------------- | ----------------------------------------------------------------------------- |
| Spreadsheet    | File   | FormData                    | Upload the spreadsheet file.                                                  |
| worksheet      | String | Query                       | The worksheet name within the spreadsheet.                                    |
| range          | String | Query                       | The cell area to be converted, e.g., A1:C10.                                  |
| outPath        | String | Query                       | (Optional) The folder path where the workbook is stored. The default is null. |
| outStorageName | String | Query                       | Output file storage name.                                                     |
| fontsLocation  | String | Query                       | Location for storing custom fonts for home use.                               |
| region         | String | Query                       | The spreadsheet region setting.                                               |
| password       | String | Query                       | The password for opening the spreadsheet file.                                |

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
- **500 Server Error**: The spreadsheet encountered an error while obtaining calculation data.

## **Where Should You Use the Convert Range to PDF API?**

- **Financial Statements**: Convert balance sheets, income statements (specific ranges) to PDF for audit‑ready documentation.  
- **Sales Reports**: Transform sales dashboards or commission calculations to distributable PDFs.  
- **Operational Metrics**: Export KPI tables and performance metrics as formal PDF reports.  
- **Contractual Data**: Export pricing tables and service‑level agreements from spreadsheets to PDF attachments.  
- **Audit Trails**: Preserve financial data ranges as uneditable PDF evidence.  
- **Portfolio Summaries**: Export investment performance ranges as client‑ready PDF statements.  
- **Quality Control Reports**: Export inspection data ranges to PDF for compliance records.  
- **Inventory Summaries**: Transform stock‑level tables to PDF for management review.

## Why Should You Use the Convert Range to PDF API?

- **Developer‑Friendly**: Aspose.Cells Cloud offers SDK libraries in multiple languages, enabling rapid development and comprehensive documentation. Compared with building custom chart‑rendering solutions, this significantly reduces development workload.  
- **Cost‑Effective**: You can convert range data without first uploading the entire workbook, saving storage space and reducing costs.  
- **Preserves Complex Excel Formatting** in a universally accessible PDF format.

## How to Use the Convert Range to PDF API with SDKs?

### Convert Range to PDF API Specification

The [Convert Range to PDF API Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToPDF) defines a publicly accessible programming interface and allows you to perform REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away low‑level details, allowing you to convert a range of data to a PDF file with concise code. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToPDF.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToPDF.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToPDF.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToPDF.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToPDF.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToPDF.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToPDF.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToPDF.go" >}}
{{</tab>}}
{{< /tabs >}}