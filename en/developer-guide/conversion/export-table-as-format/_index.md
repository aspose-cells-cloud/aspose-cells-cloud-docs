---
title: "Aspose.Cells Cloud Web API - Export a Remote Spreadsheet Table to Another Format"
second_title: "Document"
ArticleTitle: "How to Export a Remote Spreadsheet Table to Another Format: Step‑by‑Step Guide"
linktitle: "Export Table to Specified Format"
type: docs
url: /export-table-as-format/
keywords: "Aspose.Cells, Export Table, API, PDF, PNG, CSV, JSON, Cloud, Excel, REST"
description: "Convert a table from a cloud‑stored Excel workbook to PDF, PNG, CSV, JSON, or other formats using Aspose.Cells Cloud API. Secure HTTPS endpoint, authentication, and sample code in 8 languages."
weight: 100
---

Export a cloud‑stored spreadsheet (Excel) table to another format file.

## **Export Table as Format API**

### Web API

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/tables/{tableName}
```

### **Request Parameters:**

| Parameter Name | Type   | Path/Query String/HTTPBody | Description                                                                                                                                       |
| :------------- | :----- | :------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------ |
| name           | String | Path                       | **Required.** The name of the workbook file to be retrieved.                                                                                      |
| worksheet      | String | Path                       | Name of the worksheet.                                                                                                                            |
| tableName      | String | Path                       | Name of the table.                                                                                                                                |
| format         | String | Query                      | **Required.** The desired output format (e.g., “png”, “pdf”, “svg”).                                                                              |
| folder         | String | Query                      | Optional. The folder path where the workbook is stored. Default is `null`.                                                                        |
| storageName    | String | Query                      | Optional. The name of the storage if using custom cloud storage. Use default storage if omitted.                                                  |
| outPath        | String | Query                      | Optional. The folder path for output storage. Default is `null`.                                                                                  |
| outStorageName | String | Query                      | Optional. Name of the output file storage.                                                                                                        |
| fontsLocation  | String | Query                      | Optional. Location for custom fonts.                                                                                                              |
| region         | String | Query                      | Optional. Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior. |
| password       | String | Query                      | Optional. Password for opening the spreadsheet file.                                                                                              |

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

## **Where Should You Use the Export Table to Another Format API?**

- **Legacy System Migration**: Convert thousands of legacy XLS files to XLSX for modern systems.
- **Archive Standardization**: Normalize various spreadsheet formats (XLS, XLSM, ODS, CSV) to a single format for archival.
- **Office Suite Interoperability**: Convert Excel files to formats compatible with LibreOffice, Google Sheets, or Apple Numbers.
- **Data Source Normalization**: Convert various spreadsheet formats to CSV or JSON for database ingestion.
- **Web Publishing**: Convert financial models to HTML for web display.

## Why Should You Use the Export Table to Another Format API?

- **Developer‑Friendly**: Aspose.Cells Cloud offers SDK libraries in multiple languages, enabling quick development and comes with comprehensive documentation. Compared to building custom chart‑rendering solutions, this significantly reduces development workload.
- **Reduced Labor Costs**: Decreases the need for positions dedicated to document consolidation.
- **Pay‑per‑Use**: No upfront investment; you only pay for API calls actually used.
- **Zero Maintenance Costs**: No need to maintain servers, update software, or deal with compatibility issues.
- **The API returns only the raw table data without any workbook styling.**

## How to Use the Export Spreadsheet Table as Format API with SDKs?

### Export Table as Format API Specification

The [Export Table as Format API Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportTableAsFormat) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to export a spreadsheet table to a format file with short code. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportTableAsFormat.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportTableAsFormat.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportTableAsFormat.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportTableAsFormat.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportTableAsFormat.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportTableAsFormat.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportTableAsFormat.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportTableAsFormat.go" >}}
{{</tab>}}
{{< /tabs >}}
