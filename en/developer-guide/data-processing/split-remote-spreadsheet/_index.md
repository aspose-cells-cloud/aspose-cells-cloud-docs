---
url: split-remote-spreadsheet
title: Split Remote Spreadsheet in Cloud
second_title: Developer Reference
linktitle: Split Remote Spreadsheet in Cloud
type: docs
tags:
  - excel
  - split
  - cloud-api
  - rest
  - sdk
categories:
  - data-processing
  - cloud-storage
description: Use Aspose.Cells Cloud API to split Excel workbooks stored in cloud storage into separate files and export to 30+ formats (PDF, CSV, JSON, etc.). Includes REST, cURL, and SDK examples.
weight: 100
keywords: Aspose.Cells Cloud, split Excel workbook, spreadsheet splitter, cloud API, export to PDF, export to CSV, export to JSON, multiple format export, cloud spreadsheet processing
ArticleTitle: "Split Excel Workbook in Cloud with Aspose.Cells Cloud API"
---
The **SplitRemoteSpreadsheet** API (`PUT https://api.aspose.cloud/v4.0/cells/{name}/split/spreadsheet`) in Aspose.Cells Cloud v4.0 splits a remote spreadsheet file stored in cloud storage into multiple output files in formats such as XLSX, CSV, or PDF, based on user-defined criteria like worksheet ranges or custom paths, enabling remote processing without local file downloads.

## The Split Remote Spreadsheet Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/split/spreadsheet
```

### Security and Authentication

The Aspose.Cells Cloud APIs are secure and require [JWT token-based authentication](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| name | String | Path | The name of the workbook file to be split. |
| folder | String | Query | The folder path where the workbook is stored. |
| from | Integer | Query | Begin worksheet index. |
| to | Integer | Query | End worksheet index. |
| outFormat | String | Query | The desired output format (e.g., "Xlsx", "Pdf", "Csv"). |
| storageName | String | Query | (Optional) The name of the storage if using custom cloud storage. Use default storage if omitted. |
| outPath | String | Query | (Optional) The folder path where the workbook is stored. The default is null. |
| outStorageName | String | Query | Output file Storage Name. |
| fontsLocation | String | Query | Use Custom fonts. |
| region | String | Query | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior. |
| password | String | Query | The password for opening spreadsheet file. |

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

**Sample response headers**

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="result"
```

**HTTP Status Codes**

| Code | Meaning | Description |
|---|---|---|
| 200 | OK | The request completed successfully. |
| 400 | Bad Request | Invalid url. |
| 401 | Unauthorized | Authentication has failed, or no credentials were provided. |
| 404 | Not Found | Source file not accessible. |
| 500 | Server Error | The spreadsheet has encountered an anomaly in obtaining data. |

The file can be downloaded directly or saved to the location specified by `outPath`.

#### Success Response Details


#### HTTP Status Codes

| Code | Meaning               | Description                                                            |
| ---- | --------------------- | ---------------------------------------------------------------------- |
| 200  | OK                    | Split completed successfully; response contains the file(s).           |
| 400  | Bad Request           | Missing or invalid parameters (e.g., unsupported file type or format). |
| 401  | Unauthorized          | Invalid or missing JWT token.                                          |
| 404  | Not Found             | Source file not found in storage or inaccessible.                      |
| 500  | Internal Server Error | Unexpected server error during processing (e.g., file corruption).     |

This documentation applies to Aspose.Cells Cloud API v4.0 (released May 2024). For migration from v3.x, see [API Versioning Guide](https://docs.aspose.cloud/total/api-versioning/).

Use the Aspose.Cells Cloud API to split an Excel workbook stored in cloud storage into separate worksheet files and export each to over 30 formats such as PDF, CSV, JSON, XLSX, HTML, ODS, and XPS.

## Use Cases: Split Excel Files in the Cloud

- **Department Data Distribution**: Split a unified workbook containing data from multiple departments into department‑specific files.
- **Regional Report Distribution**: Split national sales statements into separate regional reporting files by region.
- **Customer Data Masking Distribution**: Split a workbook containing sensitive information into a dedicated customer‑view file.
- **Periodic Report Splitting**: Automatically split summary reports into weekly or daily reports on a monthly basis.
- **Multi‑Format Distribution**: Split a single Excel file into multiple format versions such as PDF, CSV, JSON, etc., simultaneously.
- **Templated Splitting**: Split data files into standardized output files based on predefined templates.
- **Data Source Preprocessing**: Split the Excel file into a standardized CSV file before loading the data into the database.
- **API Data Preparation**: Split large datasets into smaller chunks suitable for API transfer.
- **Microservices Data Distribution**: Split the central data file into separate data files required by each microservice.

## How to Use the Split Remote Spreadsheet API

### REST API Example with cURL

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/Report.xlsx/split/spreadsheet?folder=Input&outFormat=PDF&from=0&to=2" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 encoded)",
  "contentType": "application/pdf",
  "fileDownloadName": "Report_0.pdf"
}
```

{{< /tab >}}

{{< /tabs >}}

## Why Use the Split Remote Spreadsheet API?

- **Developer‑Friendly**: Aspose.Cells Cloud offers SDK libraries in multiple languages, enabling rapid development. Combined with comprehensive documentation and sample code, this significantly accelerates time-to-market.
- **Reduced Operational Overhead**: No server-side infrastructure to maintain — Aspose.Cloud handles scaling, security, and updates.
- **Pay‑per‑use**: No upfront investment; you only pay for API calls actually used.
- **Preserves complex Excel formatting** in universally accessible PDF format.
- **Cloud-native architecture**: Enables remote processing, reducing local resource usage and improving performance for large workbooks.

## How to Use the Split Remote Spreadsheet API with SDKs?

### Split Remote Spreadsheet API Specification

The <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/SplitRemoteSpreadsheet" rel="noopener noreferrer">Split Remote Spreadsheet API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.
