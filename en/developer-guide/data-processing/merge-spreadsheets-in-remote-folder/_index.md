---  
title: "Aspose.Cells Cloud Web API – Merge Matching Spreadsheets in Remote Folder to 30+ Formats"  
second_title: "Document"  
ArticleTitle: "Merge matching spreadsheet files into a single file in a remote folder."  
linktitle: "Merge Spreadsheets in Remote Folder"  
type: docs  
url: /merge-spreadsheets-in-remote-folder/  
keywords: "merge matching spreadsheet files remote folder, Aspose.Cells Cloud merge API, batch merge Excel files cloud, merge spreadsheets to PDF, CSV, JSON, cloud folder spreadsheet merger, remote Excel file merging, merge matching files multiple formats, Aspose merge API, automate Excel file merging"  
description: "Combine spreadsheet files stored in Aspose Cloud storage into one file. Supports over 30 output formats such as PDF, CSV, JSON, XLSX, ODS, XPS, and more."  
weight: 100  
---  

Merge matching spreadsheet files from a remote cloud folder and export to 30+ supported formats like PDF, CSV, JSON, ODS, and XPS using Aspose.Cells Cloud API.  

## **Merge Spreadsheets in Remote Folder API**

### API Endpoint  

```http
PUT https://api.aspose.cloud/v4.0/cells/merge/remote-spreadsheets
```  

**Authentication** – The request must include an OAuth 2.0 bearer token:  

```
Authorization: Bearer <access_token>
```  

### **Request Parameters:**  

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
| :- | :- | :- | :- |
| folder | String | Query | The source folder path in cloud storage where the spreadsheet files to be merged are located. |
| fileMatchExpression | String | Query | A string expression or pattern to filter and select matching files in the source folder for merging (e.g., `"*report*.xlsx"`). |
| outFormat | String | Query | Specifies the output file format after merging (e.g., `PDF`, `CSV`, `JSON`, `XLSX`). Supports 30+ common formats. |
| mergeInOneSheet | Boolean | Query | When `true`, merges content from all matched files into a single worksheet; when `false`, each file’s content is kept in separate worksheets. |
| storageName | String | Query | *(Optional)* The name of the cloud storage where source files reside. If omitted, the default cloud storage is used. |
| outPath | String | Query | *(Optional)* Specifies the target folder path in cloud storage where the merged file will be saved. If omitted, the merged file is saved in the source folder. |
| outStorageName | String | Query | The name of the cloud storage where the output merged file will be saved. |
| fontsLocation | String | Query | *(Optional)* Specifies a custom folder path containing font files to ensure proper text rendering when exporting to PDF or image formats. |
| region | String | Query | *(Optional)* Sets the locale/region for number, date, and currency formatting in the output file (e.g., `"en-US"`, `"de-DE"`). |
| password | String | Query | *(Optional)* If any matched spreadsheet file is password‑protected, provide the password to open the file. |

**Full Request Example (cURL)**  

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/merge/remote-spreadsheets?folder=MyFolder&fileMatchExpression=*.xlsx&outFormat=PDF&mergeInOneSheet=true" \
     -H "Authorization: Bearer <access_token>" \
     -H "Accept: application/json"
```  

## **Response**  

```json
[
  {
    "Name": "MergedResult.pdf",
    "Url": "https://storage.aspose.cloud/v4.0/files/MergedResult.pdf",
    "Size": 124578
  }
]
```  

### Error Codes  

- **400 Bad Request**: Invalid Aspose.Cells Cloud API URI or query parameters.  
- **401 Unauthorized**: Invalid or missing access token, or incorrect client‑id/secret.  
- **404 Not Found**: The specified spreadsheet file or folder cannot be accessed.  
- **500 Server Error**: The spreadsheet encountered an internal processing anomaly.  

**Error Response Schema**  

| Code | Message | RequestId |
| ---- | ------- | --------- |
| 400 | Bad request – check URI and parameters. | `string` |
| 401 | Unauthorized – verify OAuth token. | `string` |
| 404 | Resource not found – confirm file/folder path. | `string` |
| 500 | Internal server error – see logs for details. | `string` |

## Where should we use the Merge Spreadsheet in remote folder API?  

Use this API when you need to merge multiple data files together.

## Why should you use the Merge Spreadsheet in remote folder API?  

- **Developer friendliness** – Aspose.Cells Cloud provides SDK libraries for many languages, enabling rapid development with comprehensive documentation.  
- **Reduced labor costs** – Eliminates the need for dedicated staff to consolidate documents.  
- **Pay‑per‑use model** – You only pay for the API calls you actually make.  
- **Zero maintenance costs** – No servers to manage, no software updates, and no compatibility concerns.  

## How to Use the Merge Spreadsheet in remote folder API with SDKs  

### Merge Spreadsheet in remote folder API Specification  

The [Merge Spreadsheet in remote folder API Specification](https://reference.aspose.cloud/cells/#/DataProcessingController/MergeSpreadsheetsInRemoteFolder) provides a publicly accessible programming interface allowing REST interactions directly from a web browser.  

### Use Aspose.Cells Cloud SDKs  

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to merge matching spreadsheet files into files in a remote folder with short code. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.  

The following code examples illustrate how to interact with Aspose.Cells web services using various SDKs:  
{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MergeSpreadsheetsInRemoteFolder.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MergeSpreadsheetsInRemoteFolder.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MergeSpreadsheetsInRemoteFolder.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MergeSpreadsheetsInRemoteFolder.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MergeSpreadsheetsInRemoteFolder.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MergeSpreadsheetsInRemoteFolder.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MergeSpreadsheetsInRemoteFolder.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MergeSpreadsheetsInRemoteFolder.go" >}}  
{{</tab>}}  
{{< /tabs >}}  