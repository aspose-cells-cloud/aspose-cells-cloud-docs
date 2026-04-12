---
title: "Export Worksheet – Aspose.Cells Cloud API v4 (PDF, PNG, SVG, CSV)"
second_title: "Document"
ArticleTitle: "How to Export a Remote Spreadsheet Worksheet to Another Format: Step‑by‑Step Guide"
linktitle: "Export Worksheet"
type: docs
url: /export-worksheet-as-format/
keywords: "Aspose Cells, export worksheet, cloud API, PDF, PNG, CSV, Excel conversion"
description: "Convert a worksheet stored in Aspose.Cells Cloud to PDF, PNG, SVG, CSV, or other formats via a single GET request. Includes code samples for C#, Java, Python, and more."
weight: 100
---

Export a cloud spreadsheet/Excel worksheet to another format file using the Aspose.Cells Cloud Web API.

## **Export Worksheet as Format API**

### Web API

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}
```

### **Request Parameters**

All path parameters are required; query parameters are optional unless noted.

| Parameter Name     | Type   | Path/Query String/HTTPBody | Description                                                                                                                                        |
| :----------------- | :----- | :------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------- |
| **name**           | String | Path                       | (Required) The name of the workbook file to be retrieved.                                                                                          |
| **worksheet**      | String | Path                       | (Required) The specific worksheet to convert.                                                                                                      |
| **format**         | String | Query                      | (Required) The desired output format (e.g., `png`, `pdf`, `svg`).                                                                                  |
| **folder**         | String | Query                      | (Optional) The folder path where the workbook is stored. The default is `null`.                                                                    |
| **storageName**    | String | Query                      | (Optional) The name of the custom cloud storage. Use default storage if omitted.                                                                   |
| **outPath**        | String | Query                      | (Optional) The output folder path. The default is `null`.                                                                                          |
| **outStorageName** | String | Query                      | (Optional) Output file storage name.                                                                                                               |
| **fontsLocation**  | String | Query                      | (Optional) Specify custom fonts if needed.                                                                                                         |
| **region**         | String | Query                      | (Optional) Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior. |
| **password**       | String | Query                      | (Optional) The password for accessing the spreadsheet file.                                                                                        |

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

- **400 Bad Request** – Invalid Aspose.Cells Cloud API URI.
- **401 Unauthorized** – Invalid or missing access token.
- **404 Not Found** – The spreadsheet file is not accessible.
- **500 Server Error** – The spreadsheet encountered an anomaly while obtaining calculation data.

## **Where Should You Use the Export Worksheet to Another Format API?**

- **Legacy System Migration** – Convert thousands of legacy XLS files to XLSX for modern systems.
- **Archive Standardization** – Normalize various spreadsheet formats (XLS, XLSM, ODS, CSV) to a single format for archival.
- **Office Suite Interoperability** – Convert Excel files to formats compatible with LibreOffice, Google Sheets, or Apple Numbers.
- **Data Source Normalization** – Convert various spreadsheet formats to CSV or JSON for database ingestion.
- **Web Publishing** – Convert financial models to HTML for web display.

## Why Use the Export Worksheet to Another Format API?

- **Developer‑Friendly** – Aspose.Cells Cloud offers SDK libraries in multiple languages, enabling quick development and comprehensive documentation. Compared with building custom chart‑rendering solutions, this significantly reduces development workload.
- **Cost‑Effective** – You can convert worksheets without first uploading the workbook, which saves storage space and reduces costs.
- **Pure Data Extraction Without Formatting** – Retrieve raw data while omitting visual styling.

## How to Use the Export Spreadsheet Worksheet as Format API with SDKs?

### Export Worksheet as Format API Specification

The [Export Worksheet as Format API Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportWorksheetAsFormat) provides a publicly accessible programming interface for performing REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to export a spreadsheet worksheet to a format file with short code.  
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportWorksheetAsFormat.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportWorksheetAsFormat.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportWorksheetAsFormat.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportWorksheetAsFormat.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportWorksheetAsFormat.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportWorksheetAsFormat.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportWorksheetAsFormat.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportWorksheetAsFormat.go" >}}
{{</tab>}}
{{< /tabs >}}
