---
title: "Aspose.Cells Cloud Excel Compression Web API - Reduce Spreadsheet File Size Programmatically"
second_title: "Document"
ArticleTitle: "How to Compress Excel Files - Reduce Spreadsheet Size & Optimize Performance"
linktitle: "Compress Spreadsheet"
type: docs
url: /compress-spreadsheet/
keywords: " Excel compression API, reduce file size API, spreadsheet optimization API, compress workbook API, Aspose Cells REST API, Excel size reduction, batch compress Excel, cloud compression API, automate Excel optimization, API shrink spreadsheet, performance optimization API"
description: "Learn how to effectively compress Excel files and reduce spreadsheet size. Optimize workbook performance by removing redundant data, compressing images, and cleaning up formatting. Tools and techniques for shrinking large XLSX/XLS files while preserving data integrity."
weight: 100
---

Programmatically compress Excel spreadsheets and reduce file size with Aspose.Cells Cloud API. Optimize workbook performance by removing unused data, compressing embedded objects, and cleaning formatting. RESTful API for automated Excel file compression and optimization workflows.

## **Compress Spreadsheet API**

### API Endpoint

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/compress
```

### **Request Parameters:**

| Parameter Name | Type | Path/Query String/HTTP Body | Description |
| :- | :- | :- |:- |
| Spreadsheet | File | FormData | **Required**. The source Excel workbook file (.xlsx, .xls, etc.) that you wish to compress. |
| level | Integer | Query | **Optional**. Specifies the compression intensity level. Valid range is typically 0 (minimum/fastest compression) to 9 (maximum/slowest compression). If omitted, a balanced default level is applied. |
| outPath | String | Query | **Optional**. The destination folder path within your cloud storage where the compressed workbook should be saved. If `null` or omitted, it may default to the source file's directory. |
| outStorageName | String | Query | **Required**. The name identifier of your configured cloud storage service (e.g., `CorporateDrive`) where the output file will be stored. |
| region | String | Query | **Optional**. The locale setting (e.g., `de-DE`) to apply during the compression process, which may affect region-specific data handling. |
| password | String | Query | **Optional**. The decryption password required to access a password-protected spreadsheet. Leave blank if the file is not encrypted. |

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
- **401 Unauthorized**: Invalid access token. Or invalid client id and secret.
- **404 Not Found**: The spreadsheet file not accessible.
- **500 Server Error**: The spreadsheet has encountered an anomaly in obtaining calculation data.

## Where should we use the Compress Spreadsheet API?

- Automated report distribution process: Before sending the monthly financial statements, which contain a large number of charts and historical data, to the board of directors via email, automatically compress the files to reduce the size of the attachments, ensuring successful delivery and enhancing the receiving experience. 
- User file upload optimization: In the function that allows users to upload Excel files through the website or application, the uploaded files are compressed in the background, significantly saving cloud storage space and reducing long-term storage costs. 
- Data pipeline processing and migration: In the ETL process of migrating large datasets from the old system to the new database, the intermediate generated Excel temporary files are compressed first to speed up the network transmission speed and reduce the storage pressure of the temporary area.

## Why should you use the Compress Spreadsheet API?

- **Developer-Friendly**: Aspose.Cells Cloud offers SDK libraries in multiple languages, enabling quick development and comes with comprehensive documentation. Compared to building custom chart rendering solutions, this significantly reduces the development workload.
- **Reduced Labor Costs**: Reduced the need for positions dedicated to document consolidation.
- **Pay-per-use**: No upfront investment, only pay for API calls actually used.
- **Zero Maintenance Costs**: No need to maintain servers, update software, or deal with compatibility issues.


## How to Use the Compress Spreadsheet API with SDKs

### Compress Spreadsheet API Specification

The [Compress Spreadsheet API Specification](https://reference.aspose.cloud/cells/#/ManagementController/CompressSpreadsheet) provides a publicly accessible interface for REST interactions, allowing direct API calls from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low-level details, allowing you to compress the spreadsheet size with short code.
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to interact with Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CompressSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CompressSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CompressSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CompressSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CompressSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CompressSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CompressSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CompressSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}
