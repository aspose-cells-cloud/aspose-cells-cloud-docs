---
title: "Aspose.Cells Cloud Web API - Export Remote Excel Worksheet to other formats - Free Online Tool"
second_title: "Document"
ArticleTitle: "How to Export the Remote Spreadsheet Worksheet to other formats: Step‑Step Guide"
linktitle: "Export Spreadsheet as Format"
type: docs
url: /export-spreadsheet-as-format/
keywords: "Aspose.Cells, spreadsheet conversion, API, export, PDF, CSV, JSON, XLSX"
description: "Convert Excel workbooks stored in Aspose Cloud to PDF, XLSX, CSV, JSON, or HTML via a single REST endpoint. Learn request syntax, parameters, and see SDK examples in C#, Java, Python, and more."
weight: 100
---

Export a cloud spreadsheet (Excel) to another file format.

## **Export Spreadsheet as Format API**

All requests must be made over **HTTPS** to protect credentials.

### Web API

```http
GET https://api.aspose.cloud/v4.0/cells/{name}?format={format}&folder={folder}&storageName={storageName}&outPath={outPath}&outStorageName={outStorageName}&fontsLocation={fontsLocation}&region={region}&password={password}
```

### **Request Parameters:**

| Parameter Name | Type   | Path/Query String/HTTP Body | Description                                                                                                                                        |
| :------------- | :----- | :-------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------- |
| name           | String | Path                        | (Required) The name of the workbook file to be retrieved.                                                                                          |
| format         | String | Query                       | (Required) The desired output format (e.g., “Xlsx”, “PDF”, “CSV”).                                                                                 |
| folder         | String | Query                       | (Optional) The folder path where the workbook is stored. The default is null.                                                                      |
| storageName    | String | Query                       | (Optional) The name of the storage if using custom cloud storage. Use default storage if omitted.                                                  |
| outPath        | String | Query                       | (Optional) The folder path where the workbook will be stored. The default is null.                                                                 |
| outStorageName | String | Query                       | (Optional) Output file storage name.                                                                                                               |
| fontsLocation  | String | Query                       | (Optional) Custom fonts location.                                                                                                                  |
| region         | String | Query                       | (Optional) Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior. |
| password       | String | Query                       | (Optional) The password for opening the spreadsheet file.                                                                                          |

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

The response contains a single object that represents the converted file stream.

### Error Codes

- **400 Bad Request** – Invalid Aspose.Cells Cloud API URI.
- **401 Unauthorized** – Invalid access token, or invalid client ID and secret.
- **404 Not Found** – The spreadsheet file is not accessible.
- **500 Server Error** – The spreadsheet encountered an anomaly while obtaining calculation data.

## Where should you use the Export Spreadsheet as another format API?

- **Legacy System Migration**: Convert thousands of legacy XLS files to XLSX for modern systems.
- **Archive Standardization**: Normalize various spreadsheet formats (XLS, XLSM, ODS, CSV) to a single format for archival.
- **Office Suite Interoperability**: Convert Excel files to formats compatible with LibreOffice, Google Sheets, or Apple Numbers.
- **Data Source Normalization**: Convert various spreadsheet formats to CSV or JSON for database ingestion.
- **Web Publishing**: Convert financial models to HTML for web display.

## Why should you use the Export Spreadsheet as another format API?

- **Developer‑Friendly**: Aspose.Cells Cloud offers SDK libraries in multiple languages, enabling quick development and comes with comprehensive documentation. Compared with building custom chart‑rendering solutions, this significantly reduces the development workload.
- **Reduced Labor Costs**: Reduces the need for positions dedicated to document consolidation.
- **Pay‑per‑use**: No upfront investment; you only pay for API calls actually used.
- **Zero Maintenance Costs**: No need to maintain servers, update software, or deal with compatibility issues.
- **Comprehensive Format Support**: Convert between 20+ spreadsheet formats.
- **Preserve Data Fidelity & Formatting**: Maintains the original layout, formulas, and styling during conversion.

## How to Use the Export Spreadsheet as Format API with SDKs?

### Export Spreadsheet as Format API Specification

The [Export Spreadsheet as Format API Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportSpreadsheetAsFormat) provides a publicly accessible programming interface to perform REST interactions seamlessly.

### Use Aspose.Cells Cloud SDKs

Using an SDK is the fastest way to develop, as it abstracts away low‑level details, allowing you to export a spreadsheet to a format file with short code.  
Before calling the API, obtain an OAuth 2.0 access token and include it in the `Authorization: Bearer <token>` header.

Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples illustrate how to interact with Aspose.Cells web services via various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportSpreadsheetAsFormat.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportSpreadsheetAsFormat.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportSpreadsheetAsFormat.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportSpreadsheetAsFormat.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportSpreadsheetAsFormat.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportSpreadsheetAsFormat.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportSpreadsheetAsFormat.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportSpreadsheetAsFormat.go" >}}
{{</tab>}}
{{< /tabs >}}
