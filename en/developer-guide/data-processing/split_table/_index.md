---
title: "Split Table"
ArticleTitle: "Split Table – Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "Split Table"
type: docs
url: /cells/split/table
aliases: []
keywords: "Aspose.Cells, Split Table, API"
description: "API to split a table in a spreadsheet by column values."
weight: 1
---

## The SplitTable of Aspose.Cells Cloud Web Services

This method performs a split operation on the source table by grouping rows according to the distinct values in the specified column. Each group of data (for each unique split value) is then processed as a separate data unit. The export destination is controlled by two key boolean parameters:
- Determines the workbook structure. If `true`, each split unit is saved into a separate workbook file. If `false`, each unit becomes a new worksheet within the current workbook.
- Determines the output packaging. When set to `true` and combined with `toNewWorkbook` = `true`, the method generates multiple individual files and returns them as a ZIP archive. When `false`, all data is consolidated into a single file (either a multi‑sheet workbook or a single file as per other settings).

### Web API Endpoint

```http
PUT https://api.aspose.cloud/v4.0/cells/split/table
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name   | Type    | Path/Query String/HTTP Body | Description                                                                                                                                                                   |
|------------------|---------|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | File    | FormData                    | Upload spreadsheet file.                                                                                                                                                      |
| worksheet        | String  | Query                       | Worksheet containing the table.                                                                                                                                               |
| tableName        | String  | Query                       | Data table that needs to be split.                                                                                                                                           |
| splitColumnName  | String  | Query                       | Column name to split by.                                                                                                                                                      |
| saveSplitColumn  | Boolean | Query                       | Whether to keep the data in the split column.                                                                                                                                 |
| splitRowNumber   | Integer | Query                       | [TBD]                                                                                                                                                                          |
| toNewWorkbook    | Boolean | Query                       | Export destination control: true - Creates new workbook files containing the split data; false - Adds a new worksheet to the current workbook.                              |
| toMultipleFiles  | Boolean | Query                       | true - Exports table data as **multiple separate files** (returned as ZIP archive); false - Stores all data in a **single file** with multiple sheets. Default: false. |
| outPath          | String  | Query                       | (Optional) The folder path where the workbook is stored. The default is null.                                                                                                 |
| outStorageName   | String  | Query                       | Output file Storage Name.                                                                                                                                                     |
| fontsLocation    | String  | Query                       | Use Custom fonts.                                                                                                                                                              |
| region           | String  | Query                       | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior.                                      |
| password         | String  | Query                       | The password for opening spreadsheet file.                                                                                                                                   |

### Request Body Parameter

| Parameter Name | Type | Description |
| -------------- | ---- | ----------- |
| Spreadsheet    | File | Upload spreadsheet file. |

### **Response**

```json
{
  "file": "binary stream (ZIP archive or workbook depending on parameters)"
}
```

**Response Status Codes**

| Code | Meaning | Description |
|------|---------|-------------|
| 200  | OK      | The split operation completed successfully. The response contains the generated file (ZIP archive or workbook). |
| 400  | Bad Request | Invalid URL or request parameters. |
| 401  | Unauthorized | Authentication has failed, or no credentials were provided. |
| 404  | Not Found | Source file not accessible. |
| 413  | Payload Too Large | The request payload exceeds the allowed size. |
| 500  | Internal Server Error | The spreadsheet has encountered an anomaly in obtaining data. |

## How to Use the SplitTable with SDKs

### SplitTable Specification

The [SplitTable API Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/SplitTable) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the cURL command-line tool to access Aspose.Cells Cloud web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
# Use HTTPS for a secure connection
curl -v "https://api.aspose.cloud/v4.0/cells/split/table?worksheet=Sheet1&tableName=MyTable&splitColumnName=Category&saveSplitColumn=true&splitRowNumber=1&toNewWorkbook=true&toMultipleFiles=true&outPath=output%2Ffolder&outStorageName=MyStorage&fontsLocation=%2Fcustom%2Ffonts&region=en-US&password=SecretPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "file": "binary stream (ZIP archive or workbook depending on parameters)"
}
```

{{< /tab >}}

{{< /tabs >}}

### Use Aspose Cells Cloud SDKs

Using an SDK is the fastest way to accelerate development. An SDK abstracts low-level details, allowing you to focus on your project tasks. Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose Cells Cloud web services using various SDKs:
`[TBD]`