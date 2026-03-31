---
title: "Aspose.Cells Cloud – Merge Excel Files in Cloud | Combine Spreadsheets via API"
second_title: "Aspose.Cells Cloud"
ArticleTitle: "Merge Excel Files in Cloud – Combine Spreadsheets Online with Aspose.Cells Cloud API"
linktitle: "Merge Remote Spreadsheet"
type: docs
url: /merge-remote-spreadsheet/
keywords: "merge excel files in cloud, Aspose.Cells merge API, cloud spreadsheet merge, remote spreadsheet merge, combine Excel workbooks, cloud Excel merger"
description: "Merge Excel workbooks stored in cloud storage with Aspose.Cells Cloud API. Specify output format, target folder, and merge mode in a single HTTPS call."
weight: 100
---

Quickly merge Excel files stored in the cloud with other spreadsheets using Aspose.Cells Cloud API, and specify the output data format and storage location.

## **Merge Remote Spreadsheet API**

**Prerequisites**  
Before calling the API, ensure that you:

* Have generated a valid OAuth 2.0 access token.  
* Are using a supported cloud storage provider (AWS S3, Azure Blob, Google Cloud Storage).  
* Are running at least SDK version **23.12** (or later).  
* Have TLS 1.2 or higher enabled for secure communication.

### API Endpoint

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/merge/spreadsheet
```

> **Note:** The endpoint uses HTTPS, providing encrypted transmission and compliance with Google’s security ranking factors.

### **Request Parameters:**

| Parameter Name      | Type    | Path/Query String/HTTPBody | Description |
| :-                  | :-      | :-                         | :- |
| name                | String  | Path                       | The name of the source workbook file to be merged. |
| mergedSpreadsheet   | String  | Query                      | A comma‑separated list of spreadsheet file names to merge into the source workbook. |
| folder              | String  | Query                      | The folder path in cloud storage containing the source workbook. |
| outFormat           | String  | Query                      | The desired format for the merged output file (e.g., `XLSX`, `PDF`, `CSV`). |
| mergeInOneSheet     | Boolean | Query                      | Set to `true` to merge all source data into a single worksheet; `false` creates separate worksheets for each file. |
| storageName         | String  | Query                      | *(Optional)* The name of the cloud storage where the source workbook resides. If omitted, the default storage is used. |
| outPath             | String  | Query                      | *(Optional)* The target folder path in cloud storage for saving the merged file. If omitted, the file is saved in the source folder. |
| outStorageName      | String  | Query                      | The name of the cloud storage for saving the output file. |
| fontsLocation       | String  | Query                      | *(Optional)* Custom folder path for font files used during conversion to image/PDF formats. |
| region              | String  | Query                      | *(Optional)* Locale/region for date, number, and currency formatting in the output file (e.g., `en-US`, `de-DE`). |
| password            | String  | Query                      | *(Optional)* Password required to open the source workbook if it is protected. |

**Full Request Example (cURL)**  

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/SourceWorkbook.xlsx/merge/spreadsheet\
?mergedSpreadsheet=Report1.xlsx,Report2.xlsx\
&folder=Reports/2024\
&outFormat=pdf\
&outPath=Merged/Result.pdf\
&mergeInOneSheet=true" \
-H "Authorization: Bearer {access_token}" \
-H "Accept: application/json"
```

### **Response**

```json
{
  "FileName": "Result.pdf",
  "Size": 254312,
  "DownloadUrl": "https://mycloudstorage.com/Merged/Result.pdf"
}
```

The response returns the name, size (in bytes), and a direct download URL for the merged file.

### Error Codes

- **400 Bad Request** – The request URI is invalid or required parameters are missing.  
- **401 Unauthorized** – Invalid or missing OAuth 2.0 token, or incorrect client credentials.  
- **404 Not Found** – The specified spreadsheet file cannot be accessed.  
- **500 Server Error** – An unexpected error occurred while processing the workbook.

**Sample Error Payload**

```json
{
  "ErrorCode": "InvalidParameter",
  "Message": "The 'mergedSpreadsheet' query parameter is required.",
  "Description": "Provide at least one spreadsheet name to merge."
}
```

## Where should we use the Merge Remote Spreadsheet API?

### **Enterprise‑grade data integration**

- **Multi‑department report consolidation** – Consolidate separate Excel reports submitted by sales, marketing, finance, and other teams.  
- **Branch data summary** – Summarize performance data from each branch worldwide.  
- **Partner data consolidation** – Merge data submissions from multiple partners into a single workbook.

### **Cloud document processing workflow**

- Cloud storage file processing: Directly merge Excel files stored in AWS S3, Azure Blob, or Google Cloud Storage.  
- **Multi‑source data consolidation** – Combine files from different cloud locations into one workbook.  
- **Automated data pipelines** – Integrate the API into ETL processes to automate file merging.

### **Document‑management automation**

- **Version‑control consolidation** – Merge different versions of a project plan or budget workbook.  
- **Template data population** – Insert data files into standardized reporting templates.  
- **Regular report generation** – Automate weekly, monthly, and quarterly summary reports.

### **Cross‑platform collaboration**

- **Remote‑team collaboration** – Consolidate work submitted by dispersed team members.  
- **Customer data organization** – Merge order or feedback data from multiple customers.  
- **Supplier information summary** – Combine quotes or product information from several suppliers.

## Why should you use the Merge Remote Spreadsheet API?

- **Developer‑friendly** – Aspose.Cells Cloud provides SDKs for many languages, shortening development time and offering comprehensive documentation. Compared with building a custom solution, this reduces workload dramatically.  
- **Reduced labor costs** – Decreases the need for staff dedicated to manual document consolidation.  
- **Pay‑per‑use** – No upfront investment; you only pay for the API calls you actually use.  
- **Zero maintenance costs** – No servers to maintain, no software updates, and no compatibility concerns.

## How to Use the Merge Remote Spreadsheet API with SDKs

### Merge Remote Spreadsheet API Specification

The [Merge Remote Spreadsheet API Specification](https://reference.aspose.cloud/cells/#/DataProcessingController/MergeRemoteSpreadsheet) describes the REST interface that can be called directly from any HTTP client.

## Excel API SDK

### Use Aspose.Cells Cloud SDKs

Using an SDK is the fastest way to develop, as it abstracts low‑level details and lets you merge a spreadsheet into another spreadsheet with a short code snippet.  
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