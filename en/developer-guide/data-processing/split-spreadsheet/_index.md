---
title: "Aspose.Cells Cloud Split Excel WEb API -Split Excel Locally to Multiple Files & Export to 30+ Formats."
second_title: "Document"
ArticleTitle: "Excel Split Tool - Divide Local Spreadsheet into Files in 30+ Formats."
linktitle: "Split Spreadsheet"
type: docs
url: /split-spreadsheet/
keywords: "split Excel file locally, offline spreadsheet splitter, split workbook without cloud, export split Excel to 30 formats, local Excel file splitter, split spreadsheet to PDF CSV JSON offline, Aspose.Cells local split API, desktop Excel split tool, no cloud storage neede"
description: "Split a local Excel file into separate files directly on your device without uploading to cloud storage. Export each split file to 30+ formats including PDF, CSV, JSON, XLSX, and HTML."
weight: 100
---

Divide a local Excel workbook into separate files entirely — no cloud storage needed. Output supports 30+ file formats such as PDF, CSV, JSON, ODS, and XPS.

## **Split Spreadsheet API**

### API Endpoint

```http
PUT http://api.aspose.cloud/v4.0/cells/split/spreadsheet
```

### **Request Parameters:**

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
| :- | :- | :- | :- |
| Spreadsheet | File | FormData | The local spreadsheet file to be split. Supported formats include XLSX, XLS, ODS, CSV, etc. The file is processed entirely on the server without requiring cloud storage. |
| from | Integer | Query | The zero‑based starting index of the worksheet range to split (e.g., `0` for the first worksheet). |
| to | Integer | Query | The zero‑based ending index of the worksheet range to split (e.g., `2` will split worksheets 0, 1, and 2). |
| outFormat | String | Query | The output format for the split files. Supports 30+ formats such as `PDF`, `CSV`, `JSON`, `XLSX`, `HTML`. |
| outPath | String | Query | *(Optional)* The local folder path where the split output files will be saved. If omitted, files are saved in a default temporary location. |
| outStorageName | String | Query | The storage identifier for organizing output files. In local processing mode, this typically refers to a session‑based or user‑defined storage label. |
| fontsLocation | String | Query | *(Optional)* Specifies a local or custom font directory to ensure accurate text rendering when exporting to PDF or image formats. |
| region | String | Query | *(Optional)* Sets the locale for number, date, and currency formatting in the output files (e.g., `"en‑US"`, `"de‑DE"`). |
| password | String | Query | *(Optional)* If the uploaded spreadsheet is password‑protected, provide the password to open and process the file. |

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

## Where should we use the Split Spreadsheet API?

- **Department Data Distribution**: Split a unified workbook containing data from multiple departments into department-specific files.
- **Regional Report Distribution**: Split national sales statements into separate regional reporting files by region.
- **Customer Data Masking Distribution**: Splitting a workbook containing sensitive information into a deduced customer view file.
- **Periodic Report Splitting**: Automatically split summary reports into weekly or daily reports on a monthly basis.
- **Multi-Format Distribution**: Split a single Excel file into multiple format versions such as PDF, CSV, JSON, etc. at the same time.
- **Templated Splitting**: Splitting data files into standardized output files based on predefined templates.
- **Data Source Preprocessing**: Split the Excel file into a standardized CSV file before loading the data into the database.
- **API Data Preparation**: Splitting large datasets into smaller chunks suitable for API transfer.

## Why should you use the Split Spreadsheet API?

- **Developer-Friendly**: Aspose.Cells Cloud offers SDK libraries in multiple languages, enabling quick development and comes with comprehensive documentation. Compared to building custom chart rendering solutions, this significantly reduces the development workload.
- **Reduced Labor Costs**: Reduced the need for positions dedicated to document consolidation.
- **Pay-per-use**: No upfront investment, only pay for API calls actually used.
- **Zero Maintenance Costs**: No need to maintain servers, update software, or deal with compatibility issues.
- **Preserves complex Excel formatting** in universally accessible PDF format.

## How to Use the Split Spreadsheet API with SDKs

### Split Spreadsheet API Specification

The [Split Spreadsheet API Specification](https://reference.aspose.cloud/cells/#/DataProcessingController/SplitSpreadsheet) provides a publicly accessible programming interface for performing REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low-level details, allowing you to split spreadsheet into separate files  with short code.
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples illustrate how to invoke Aspose.Cells web services using different SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SplitLocalFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SplitLocalFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SplitLocalFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SplitLocalFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SplitLocalFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SplitLocalFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SplitLocalFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SplitLocalFile.go" >}}
{{</tab>}}
{{< /tabs >}}
