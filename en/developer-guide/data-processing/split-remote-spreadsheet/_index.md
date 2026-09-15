---
url: split-remote-spreadsheet
title: Split Remote Spreadsheet in Cloud
second title: Developer Reference
linktitle: Split Remote Spreadsheet in Cloud
date: 2024-05-20T10:00:00Z
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
canonical_url: https://reference.aspose.cloud/cells/split-remote-spreadsheet/
keywords: Aspose.Cells Cloud, split Excel workbook, spreadsheet splitter, cloud API, export to PDF, export to CSV, export to JSON, multiple format export, cloud spreadsheet processing
---

## Prerequisites

- An Aspose.Cells Cloud account and API credentials ([get free trial](https://purchase.aspose.cloud/temporary-license)).
- Install the SDK for your preferred language (see [Aspose.Cells Cloud SDKs on GitHub](https://github.com/aspose-cells-cloud)).
- Enable cloud storage access (e.g., Aspose Cloud Storage, Google Drive, or Amazon S3).

## Split Remote Spreadsheet API

This documentation applies to Aspose.Cells Cloud API v4.0 (released May 2024). For migration from v3.x, see [API Versioning Guide](https://docs.aspose.cloud/total/api-versioning/).

Use the Aspose.Cells Cloud API to split an Excel workbook stored in cloud storage into separate worksheet files and export each to over 30 formats such as PDF, CSV, JSON, XLSX, HTML, ODS, and XPS.

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/split/spreadsheet
```

### Security and Authentication

The Aspose.Cells Cloud APIs are secure and require [JWT token-based authentication](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### Request Parameters

| Parameter Name   | Type    | Location | Description                                                                                                                                  |
| :--------------- | :------ | :------- | :------------------------------------------------------------------------------------------------------------------------------------------- |
| `name`           | String  | Path     | The name of the workbook file (e.g., `data.xlsx`) to be split, located in the specified cloud storage folder.                                |
| `folder`         | String  | Query    | The cloud storage folder path where the source workbook is stored.                                                                           |
| `from`           | Integer | Query    | The starting worksheet index (0‑based) for the split operation. For example, `from=0` indicates the first worksheet.                         |
| `to`             | Integer | Query    | The ending worksheet index (0‑based) for the split operation. For example, `from=0` and `to=2` splits worksheets 0, 1, and 2 (inclusive).    |
| `outFormat`      | String  | Query    | The output file format for the split files. Supported formats include `XLSX`, `PDF`, `CSV`, `JSON`, `HTML`, and 30+ others. Default: `XLSX`. |
| `storageName`    | String  | Query    | _(Optional)_ The name of the cloud storage where the source workbook resides. If omitted, the default cloud storage is used.                 |
| `outPath`        | String  | Query    | _(Optional)_ The target cloud folder path where the split files will be saved. If omitted, files are saved in the source folder.             |
| `outStorageName` | String  | Query    | The name of the cloud storage where the output split files will be stored.                                                                   |
| `fontsLocation`  | String  | Query    | _(Optional)_ Specifies a custom cloud folder path containing font files for proper text rendering in PDF/image outputs.                      |
| `region`         | String  | Query    | _(Optional)_ Sets the locale for formatting numbers, dates, and currency in the output files (e.g., `"en-US"`, `"zh-CN"`, `"de-DE"`).        |
| `password`       | String  | Query    | _(Optional)_ If the source workbook is password‑protected, provide the password to open the file.                                            |

### Response

```json
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 encoded)",
  "contentType": "MIME type",
  "fileDownloadName": "optional file name"
}
```

The file can be downloaded directly or saved to the location specified by `outPath`.

#### Success Response Details

| Status Code | Content-Type               | Description                         |
| ----------- | -------------------------- | ----------------------------------- |
| 200 OK      | `application/octet-stream` | Binary stream of the split file(s). |

#### HTTP Status Codes

| Code | Meaning               | Description                                                            |
| ---- | --------------------- | ---------------------------------------------------------------------- |
| 200  | OK                    | Split completed successfully; response contains the file(s).           |
| 400  | Bad Request           | Missing or invalid parameters (e.g., unsupported file type or format). |
| 401  | Unauthorized          | Invalid or missing JWT token.                                          |
| 404  | Not Found             | Source file not found in storage or inaccessible.                      |
| 500  | Internal Server Error | Unexpected server error during processing (e.g., file corruption).     |

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

### Using Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to split the spreadsheet stored in the cloud into separate files with short code.

Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call the API using various SDKs:

{{< tabs tabTotal="8" tabID="2" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SplitFileInRemote.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SplitFileInRemote.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SplitFileInRemote.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SplitFileInRemote.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SplitFileInRemote.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SplitFileInRemote.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SplitFileInRemote.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SplitFileInRemote.go" >}}
{{< /tab >}}
{{< /tabs >}}

## Why Use the Split Remote Spreadsheet API?

- **Developer‑Friendly**: Aspose.Cells Cloud offers SDK libraries in multiple languages, enabling rapid development. Combined with comprehensive documentation and sample code, this significantly accelerates time-to-market.
- **Reduced Operational Overhead**: No server-side infrastructure to maintain — Aspose.Cloud handles scaling, security, and updates.
- **Pay‑per‑use**: No upfront investment; you only pay for API calls actually used.
- **Preserves complex Excel formatting** in universally accessible PDF format.
- **Cloud-native architecture**: Enables remote processing, reducing local resource usage and improving performance for large workbooks.

{{< figure src="https://i.imgur.com/placeholder_split_flow.png" alt="Flowchart: Upload Excel file → API call with parameters → Split into worksheets → Export to PDF/CSV/JSON" caption="Figure 1: How the Split Remote Spreadsheet API works" >}}
