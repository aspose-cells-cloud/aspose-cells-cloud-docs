---
title: "Aspose.Cells Cloud Spreadsheet Merger - Combine Excel Files from Cloud Storage with API."
second_title: Aspose.Cells Cloud"
ArticleTitle: "Merge Excel Files in Cloud - Combine Spreadsheets Online with Aspose.Cells Cloud API"
linktitle: "Merge Remote Spreadsheet"
type: docs
url: /merge-remote-spreadsheet/
keywords: "merge Excel files online, combine spreadsheets cloud API, Aspose.Cells merge workbooks, merge Excel files stored in cloud storage, combine Excel files API, merge multiple spreadsheets, cloud Excel merger, automatic spreadsheet merging, Excel file combination tool, merge Excel online free"
description: "Combine a spreadsheet file stored in a cloud storage into another spreadsheet, and you can specify the format and location of the data output.."
weight: 100
---

Quickly merge Excel files stored in the cloud with other spreadsheets using Aspose.Cells Cloud API, and flexibly specify the output data format and storage location.

## **Merge Remote Spreadsheet API**

### API Endpoint

```http
PUT http://api.aspose.cloud/v4.0/cells/{name}/merge/spreadsheet
```

### **Request Parameters:**

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
| :- | :- | :- | :- |
| name | String | Path | The name of the source workbook file to be merged. |
| mergedSpreadsheet | String | Query | A comma-separated list of spreadsheet file names to merge into the source workbook. |
| folder | String | Query | The folder path in cloud storage containing the source workbook. |
| outFormat | String | Query | The desired format for the merged output file (e.g., `XLSX`, `PDF`, `CSV`). |
| mergeInOneSheet | Boolean | Query | If set to `true`, merges data from all source files into a single worksheet. If `false`, each file's content is placed in separate worksheets. |
| storageName | String | Query | *(Optional)* The name of the cloud storage where the source workbook resides. If omitted, the default cloud storage is used. |
| outPath | String | Query | *(Optional)* The target folder path in cloud storage for saving the merged file. If omitted, the merged file is saved in the source folder. |
| outStorageName | String | Query | The name of the cloud storage for saving the output file. |
| fontsLocation | String | Query | *(Optional)* Specifies a custom folder path for font files used during conversion to image/PDF formats. |
| region | String | Query | *(Optional)* Sets the locale/region for date, number, and currency formatting in the output file (e.g., `en-US`, `de-DE`). |
| password | String | Query | *(Optional)* The password required to open the source workbook if it is password-protected. |

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

## Where should we use the Merge Remote Spreadsheet API?

### **Enterprise-Grade Data Integration**

- **Multi-Department Report Consolidation**: Consolidate separate Excel reports submitted by sales, marketing, finance, and more.
- **Branch Data Summary**: A performance data file that summarizes the performance data of each branch nationwide or globally.
- **Partner Data Consolidation**: Consolidate data submissions from multiple partners.

### **Cloud Document Processing Process**

- Cloud Storage File Processing: Directly merge Excel files stored in AWS S3, Azure Blob, and Google Cloud Storage.
- **Multi-Source Data Consolidation**: Consolidate files from different cloud locations into a single file.
- **Automated Data Pipelines**: Integrate into data ETL processes to automate file merging.

### **Document Management Automation**

- **Version Control Consolidation**: Consolidate different versions of a project plan or budget file.
- **Template Data Population**: Incorporate data files into standardized reporting templates.
- **Regular Report Generation**: Automate the generation of weekly, monthly, and quarterly summary reports.

### **Cross-Platform Collaboration**

- **Remote Team Collaboration**: Consolidate work submitted by dispersed team members.
- **Customer Data Organization**: Consolidate order or feedback data from different customers.
- **Supplier Information Summary**: Consolidate quotes or product information from multiple suppliers.

## Why should you use the Merge Remote Spreadsheet API?

- **Developer-Friendly**: Aspose.Cells Cloud offers SDK libraries in multiple languages, enabling quick development and comes with comprehensive documentation. Compared to building custom chart rendering solutions, this significantly reduces the development workload.
- **Reduced Labor Costs**: Reduced the need for positions dedicated to document consolidation.
- **Pay-per-use**: No upfront investment, only pay for API calls actually used.
- **Zero Maintenance Costs**: No need to maintain servers, update software, or deal with compatibility issues.

## How to Use the Merge Remote Spreadsheet API with SDKs

### Merge Remote Spreadsheet API Specification

The [Merge Remote Spreadsheet API Specification](https://reference.aspose.cloud/cells/#/DataProcessingController/MergeRemoteSpreadsheet) provides a publicly accessible programming interface for executing REST interactions directly from a web browser.

## Excel API SDK

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low-level details, allowing you to merge a spreadsheet into  another spreadsheet with short code.
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.
The following code examples demonstrate how to interact with Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MergeRemoteSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MergeRemoteSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MergeRemoteSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MergeRemoteSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MergeRemoteSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MergeRemoteSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MergeRemoteSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MergeRemoteSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}
