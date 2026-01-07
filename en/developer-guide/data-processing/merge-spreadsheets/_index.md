---
title: "Aspose.Cells Cloud Merge Excel Files Web API - Combine Multiple Spreadsheets into One File."
second_title: "Document"
ArticleTitle: Combine Multiple Excel Files into One - Batch Merge Spreadsheets to 30+ Formats"
linktitle: "Merge Spreadsheets"
type: docs
url: /merge-spreadsheets/
keywords: "merge Excel files online, combine multiple spreadsheets into one, merge local Excel files, Aspose.Cells merge tool, Excel file merger, combine multiple Excel files into one workbook, merge spreadsheets online free, Excel consolidation tool, batch merge Excel files, merge XLS XLSX files"
description: "Merge multiple local Excel files (XLS, XLSX) into a single file online using Aspose.Cells. Supports 30+ output formats including PDF, CSV, HTML, and more."
weight: 100
---

Batch merge multiple local spreadsheet files into one unified file. Convert the merged result to 30+ formats, including PDF, CSV, HTML, ODS, and XPS with Aspose.Cells Cloud Web API.

## **Merge Spreadsheet API**

### API Endpoint

```http
PUT http://api.aspose.cloud/v4.0/cells/merge/spreadsheet
```

### **Request Parameters:**

| Parameter Name | Type | Path/Query String/HTTP Body | Description |
| :- | :- | :- | :- |
| Spreadsheet | File | FormData | The local spreadsheet file to upload and process. Supports formats including XLSX, XLS, CSV, ODS, etc. |
| outFormat | String | Query | The format of the output file after merging (e.g., `XLSX`, `PDF`, `CSV`, `HTML`). Supports 30+ common formats. |
| mergeInOneSheet | Boolean | Query | When set to `true`, all data from the input file(s) is merged into a single worksheet. When `false`, each original sheet is preserved. |
| outPath | String | Query | *(Optional)* Specifies the cloud folder path where the merged output file will be saved. If not provided, the file is stored in the default location. |
| outStorageName | String | Query | The cloud storage name where the output file should be saved (e.g., default cloud storage or custom storage name). |
| fontsLocation | String | Query | *(Optional)* Specifies a custom cloud folder path containing font files to ensure correct text rendering in PDF/image outputs. |
| region | String | Query | *(Optional)* Sets the locale for formatting numbers, dates, and currency (e.g., `en-US`, `zh-CN`, `de-DE`) in the output file. |
| password | String | Query | *(Optional)* If the uploaded spreadsheet is password-protected, provide the password for opening the file. |

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

## Where should we use the Merge Local Spreadsheet API?

### **Education and Academic Applications**

- **Student Assignment Grading**: Merge multiple student assignment files for unified comments and grading
- **Research Data Collection**: Merge data collection spreadsheets from different experimental groups
- **Teaching Material Creation**: Merge exercises from multiple chapters into a unified question bank file

### **Data Processing and Analysis**

- **Small Data Set Integration**: Merge CSV or Excel data files exported from different sources
- **Data Analysis Preprocessing**: Merge relevant data source files before conducting data analysis
- **Template Data Filling**: Combine data files into pre-set report templates

### **Development and Technical Support**

- **Test Data Preparation**: Merge multiple test case files for automated testing
- **Log File Analysis**: Merge Excel reports of system logs from different time periods
- **Configuration Management**: Merge multiple configuration spreadsheets into a unified configuration file

## Why should you use the Merge Local Spreadsheet API?

- **Developer-Friendly**: Aspose.Cells Cloud offers SDK libraries in multiple languages, enabling quick development and comes with comprehensive documentation. Compared to building custom chart rendering solutions, this significantly reduces the development workload.
- **Reduced Labor Costs**: Reduced the need for positions dedicated to document consolidation.
- **Pay-per-use**: No upfront investment, only pay for API calls actually used.
- **Zero Maintenance Costs**: No need to maintain servers, update software, or deal with compatibility issues.

## How to Use the Merge Local Spreadsheet API with SDKs

### OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/DataProcessingController/MergeSpreadsheets) provides a publicly accessible programming interface, allowing users to perform REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low-level details, allowing you to merge multiple spreadsheets into  a spreadsheet with short code.
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples illustrate how to make calls to Aspose.Cells web services using various SDKs:
{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MergeSpreadsheets.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MergeSpreadsheets.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MergeSpreadsheets.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MergeSpreadsheets.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MergeSpreadsheets.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MergeSpreadsheets.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MergeSpreadsheets.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MergeSpreadsheets.go" >}}
{{</tab>}}
{{< /tabs >}}
