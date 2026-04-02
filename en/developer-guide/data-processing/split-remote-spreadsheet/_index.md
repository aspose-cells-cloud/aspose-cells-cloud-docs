---
title: "Aspose.Cells Cloud Spreadsheet Splitter Web API - Divide Excel Workbook into Multiple Files in 30+ Formats"
second_title: "Document"
ArticleTitle: "Split Excel File in Cloud to Separate Files & Export to 30+ Formats"
linktitle: "Split Remote Spreadsheet in Cloud"
type: docs
url: /split-remote-spreadsheet/
keywords: "Aspose.Cells Cloud, split Excel workbook, spreadsheet splitter, cloud API, export to PDF, export to CSV, export to JSON, multiple format export, cloud spreadsheet processing"
description: "Use Aspose.Cells Cloud API to split an Excel workbook stored in cloud storage into separate worksheets and export each part to over 30 formats such as PDF, CSV, JSON, XLSX, HTML, ODS, and XPS."
weight: 100
---

Divide a large Excel workbook stored in the cloud into separate files by worksheet and export each in 30+ output formats such as PDF, CSV, JSON, ODS, and XPS using Aspose.Cells Cloud.

## **Split Remote Spreadsheet API**

### API Endpoint

```http
PUT http://api.aspose.cloud/v4.0/cells/{name}/split/spreadsheet
```

### **Request Parameters:**

| Parameter Name | Type | Path/Query String/HTTP Body | Description |
| :- | :- | :- | :- |
| name | String | Path | The name of the workbook file (e.g., `data.xlsx`) to be split, located in the specified cloud storage folder. |
| folder | String | Query | The cloud storage folder path where the source workbook is stored. |
| from | Integer | Query | The starting worksheet index (0‑based) for the split operation. For example, `0` indicates the first worksheet. |
| to | Integer | Query | The ending worksheet index (0‑based) for the split operation. For example, `2` splits worksheets 0, 1, and 2. |
| outFormat | String | Query | The output file format for the split files. Supported formats include `XLSX`, `PDF`, `CSV`, `JSON`, `HTML`, and 30+ others. |
| storageName | String | Query | *(Optional)* The name of the cloud storage where the source workbook resides. If omitted, the default cloud storage is used. |
| outPath | String | Query | *(Optional)* The target cloud folder path where the split files will be saved. If omitted, files are saved in the source folder. |
| outStorageName | String | Query | The name of the cloud storage where the output split files will be stored. |
| fontsLocation | String | Query | *(Optional)* Specifies a custom cloud folder path containing font files for proper text rendering in PDF/image outputs. |
| region | String | Query | *(Optional)* Sets the locale for formatting numbers, dates, and currency in the output files (e.g., `"en-US"`, `"zh-CN"`, `"de-DE"`). |
| password | String | Query | *(Optional)* If the source workbook is password‑protected, provide the password to open the file. |

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

- **400 Bad Request**: Invalid Aspose.Cells Cloud API URI.
- **401 Unauthorized**: Invalid access token. Or invalid client id and secret.
- **404 Not Found**: The spreadsheet file not accessible.
- **500 Server Error**: The spreadsheet has encountered an anomaly in obtaining calculation data.

## Where should we use the Split Remote Spreadsheet API?

- **Department Data Distribution**: Split a unified workbook containing data from multiple departments into department‑specific files.
- **Regional Report Distribution**: Split national sales statements into separate regional reporting files by region.
- **Customer Data Masking Distribution**: Splitting a workbook containing sensitive information into a dedicated customer view file.
- **Periodic Report Splitting**: Automatically split summary reports into weekly or daily reports on a monthly basis.
- **Multi-Format Distribution**: Split a single Excel file into multiple format versions such as PDF, CSV, JSON, etc. at the same time.
- **Templated Splitting**: Splitting data files into standardized output files based on predefined templates.
- **Data Source Preprocessing**: Split the Excel file into a standardized CSV file before loading the data into the database.
- **API Data Preparation**: Splitting large datasets into smaller chunks suitable for API transfer.
- **Microservices Data Distribution**: Split the central data file into separate data files required by each microservice.

## Why should you use the Split Remote Spreadsheet API?

- **Developer‑Friendly**: Aspose.Cells Cloud offers SDK libraries in multiple languages, enabling quick development and comes with comprehensive documentation. Compared to building custom chart rendering solutions, this significantly reduces the development workload.
- **Reduced Labor Costs**: Reduced the need for positions dedicated to document consolidation.
- **Pay‑per‑use**: No upfront investment, only pay for API calls actually used.
- **Zero Maintenance Costs**: No need to maintain servers, update software, or deal with compatibility issues.
- **Preserves complex Excel formatting** in universally accessible PDF format.

## How to Use the Split Remote Spreadsheet API with SDKs

### Split Remote Spreadsheet API Specification

The [Split Remote Spreadsheet API Specification](https://reference.aspose.cloud/cells/#/DataProcessingController/SplitRemoteSpreadsheet) defines a publicly accessible programming interface and enables REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to split the spreadsheet stored in the cloud into separate files with short code.  
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.  
The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SplitFileInRemote.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SplitFileInRemote.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SplitFileInRemote.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SplitFileInRemote.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SplitFileInRemote.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SplitFileInRemote.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SplitFileInRemote.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SplitFileInRemote.go" >}}
{{</tab>}}
{{< /tabs >}}