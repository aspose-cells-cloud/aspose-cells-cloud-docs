---
title: "Aspose.Cells Cloud Web API - Convert Local Excel Table Data to a PDF File - Free Online Tool"
second_title: "Document"
ArticleTitle: "How to Convert Local Spreadsheet Table Data to a PDF File: Step‑by‑Step Guide"
linktitle: "Convert Table to PDF"
type: docs
url: /convert-table-to-pdf/
keywords: "Aspose.Cells Cloud, Table to PDF, Excel table conversion, REST API, PDF generation, spreadsheet conversion"
description: "Convert a local Excel table to a PDF file quickly using the Aspose.Cells Cloud REST API."
weight: 100
---

Export table data from a local Excel file to a PDF file using the Cloud API.

## **Convert Table to PDF API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/pdf
```

### **Request Parameters:**

| Parameter Name | Type   | Path/Query String/HTTPBody | Description                                                                             |
| :------------- | :----- | :------------------------- | :-------------------------------------------------------------------------------------- |
| Spreadsheet    | File   | FormData                   | Upload the spreadsheet file to be converted.                                            |
| worksheet      | String | Query                      | The worksheet name of the spreadsheet.                                                  |
| tableName      | String | Query                      | Name of the table to convert.                                                           |
| outPath        | String | Query                      | (Optional) The folder path where the converted PDF will be stored. The default is null. |
| outStorageName | String | Query                      | Specify the name of the output file storage.                                            |
| fontsLocation  | String | Query                      | Use custom fonts for the PDF.                                                           |
| region         | String | Query                      | Specifies the region setting for the spreadsheet.                                       |
| password       | String | Query                      | Password for accessing the spreadsheet file.                                            |

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

## **Where Should You Use the Convert Table to PDF API?**

- **Financial Statements**: Convert balance sheets, income statements (specific tables) to PDF for audit‑ready documentation.
- **Sales Reports**: Transform sales dashboards or commission calculations to distributable PDFs.
- **Operational Metrics**: Export KPI tables and performance metrics as formal PDF reports.
- **Contractual Data**: Export pricing tables and service‑level agreements from spreadsheets to PDF attachments.
- **Audit Trails**: Preserve financial data tables as uneditable PDF evidence.
- **Portfolio Summaries**: Export investment performance tables as client‑ready PDF statements.
- **Quality Control Reports**: Export inspection data tables to PDF for compliance records.
- **Inventory Summaries**: Transform stock‑level tables to PDF for management review.

## Why Should You Use the Convert Table to PDF API?

- **Developer‑Friendly**: Aspose.Cells Cloud offers SDK libraries in multiple languages, enabling rapid development and comes with comprehensive documentation. Compared with building custom chart‑rendering solutions, this significantly reduces development workload.
- **Cost‑Effective**: You can convert table data without first uploading the workbook, which saves storage space and reduces costs.
- **Preserves Complex Excel Formatting** in a universally accessible PDF format.

## How to Use the Convert Table to PDF API with SDKs?

### Convert Table to PDF API Specification

The [Convert Table to PDF API Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToPDF) provides a publicly accessible programming interface for executing REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away low‑level details, allowing you to convert spreadsheet table data to a PDF file with minimal code. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples illustrate how to call Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToPDF.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToPDF.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToPDF.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToPDF.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToPDF.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToPDF.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToPDF.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToPDF.go" >}}
{{</tab>}}
{{< /tabs >}}
