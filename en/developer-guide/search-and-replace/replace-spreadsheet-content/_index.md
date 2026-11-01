---
title: "Replace Text in Excel Without Uploading – Find & Replace API"
description: "Replace Excel content locally using Aspose.Cells Cloud API—secure, batch find-and-replace without uploading files."
keywords: "Excel find replace, Aspose.Cells Cloud API, local spreadsheet processing, bulk text replacement"
linktitle: "Replace Spreadsheet Content"
url: /replace-spreadsheet-content/
type: docs
weight: 100
ArticleTitle: "Aspose.Cells Cloud Replace Spreadsheet Content API"
---
The **ReplaceSpreadsheetContent** API (`PUT https://api.aspose.cloud/v4.0/cells/replace/content`) enables cloud-based text replacement within local Excel spreadsheets without uploading files to cloud storage, supporting full-workbook or targeted replacements across all sheets and cells while preserving original formatting, formulas, and charts.

## Replace Text in Excel Without Uploading

Replace specified text within local Excel spreadsheet files without uploading them to the cloud. Use Aspose.Cells Cloud Find & Replace API to update content in workbooks efficiently—ideal for on-premise data pipelines, report generation, and batch processing—while preserving original formatting, formulas, and charts.

## The Replace Spreadsheet Content Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/replace/content
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer" target="_blank">JWT token-based authentication</a>.

### **Request Parameters:**

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| Spreadsheet | File | FormData | Upload spreadsheet file. |
| searchText | String | Query | Specify the search content. |
| replaceText | String | Query | Specify the replace content. |
| worksheet | String | Query | Specify the worksheet for the replace. |
| cellArea | String | Query | Specify the cell area for the replace. |
| region | String | Query | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior. |
| password | String | Query | The password for opening spreadsheet file. |

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
| 413 | Payload Too Large | The uploaded file exceeds the allowed size limit. |
| 500 | Server Error | The spreadsheet has encountered an anomaly in obtaining data. |

## Prerequisites

Before calling this API, ensure you have:

- An active [Aspose.Cells Cloud account](https://dashboard.aspose.cloud/)
- A valid **Client ID** and **Client Secret** (see [Get Your App Keys](/get-app-keys/))
- A local Excel file in a supported format (XLSX, XLS, ODS, CSV, etc.)

## Authentication

All Aspose.Cells Cloud APIs use JWT token-based authentication. Include the access token in the `Authorization` header:

```shell
-H "Authorization: Bearer {access_token}"
```

For step-by-step instructions, see [Authenticating API Requests](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## Request Parameters

| Parameter Name | Type   | Location              | Required | Description                                                                                                                                          |
| :------------- | :----- | :-------------------- | :------- | :--------------------------------------------------------------------------------------------------------------------------------------------------- |
| `Spreadsheet`  | File   | `multipart/form-data` | Yes      | Local spreadsheet file to process.                                                                                                                   |
| `searchText`   | String | Query                 | Yes      | Text string to search for.                                                                                                                           |
| `replaceText`  | String | Query                 | Yes      | Replacement text.                                                                                                                                    |
| `worksheet`    | String | Query                 | No       | Name of the worksheet to process. Defaults to the first worksheet.                                                                                   |
| `cellArea`     | String | Query                 | No       | Cell range (e.g., `"A1:D20"`, `"B5:F15"`). Defaults to all used cells in the worksheet.                                                              |
| `region`       | String | Query                 | No       | Locale identifier (e.g., `"en-US"`, `"fr-FR"`). Affects case sensitivity and locale-specific text handling.                                          |
| `password`     | String | `multipart/form-data` | No       | **Password for protected files.** _Do not send in query strings._ Include as a form field (e.g., `Content-Disposition: form-data; name="password"`). |

> 🔒 **Security Note**: Sending passwords in query strings is insecure (exposed in logs, proxies, and browser history). Always use the `password` field in the request body.

## Request Example (cURL)

```shell
# Step 1: Obtain JWT token
curl -v "https://api.aspose.cloud/connect/token" \
  -X POST \
  -d "grant_type=client_credentials&client_id=YOUR_CLIENT_ID&client_secret=YOUR_CLIENT_SECRET" \
  -H "Content-Type: application/x-www-form-urlencoded" \
  -H "Accept: application/json"

# Step 2: Call ReplaceSpreadsheetContent
curl -v "https://api.aspose.cloud/v4.0/cells/replace/content?searchText=old&replaceText=new&worksheet=Sheet1&cellArea=A1:C10" \
  -X PUT \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/file.xlsx" \
  -F "password=your_password" \
  --output "updated_file.xlsx"
```

## Response

Returns a binary stream containing the modified workbook. Save the response with the appropriate extension (e.g., `.xlsx`).

Example JSON schema for the _metadata_ (actual response is binary):

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="updated_file.xlsx"
```

## Error Handling

| Code  | Description                                                    |
| :---- | :------------------------------------------------------------- |
| `400` | Invalid URL, malformed parameters, or unsupported file format. |
| `401` | Invalid, expired, or missing access token.                     |
| `404` | Source file not found or specified worksheet does not exist.   |
| `500` | Internal server error during processing.                       |

## Where to Use This API

- **Batch processing of local Excel files**  
  Automate find-and-replace across hundreds of workbooks stored on-premises.

- **On-premise data pipelines**  
  Integrate into scheduled jobs (e.g., nightly report updates) without moving sensitive data to the cloud.

- **Dynamic template population**  
  Insert values into template workbooks (e.g., replacing `{{DATE}}` or `{{TOTAL}}`) without uploading.

> For large-scale batch operations, see [Batch File Operations](/batch-operations/).

## Why Use Aspose.Cells Cloud Find & Replace?

- **No infrastructure maintenance required**  
  Eliminate server management, software updates, and compatibility concerns.

- **Developer-friendly integration**  
  Use our official SDKs (C#, Java, PHP, Python, Node.js, Ruby, Perl, Go) to accelerate development.

- **Accurate and safe**  
  Preserves original workbook structure, formulas, charts, and styles.

- **Secure and compliant**  
  Supports password-protected files with secure parameter handling (no query-string secrets).

- **Cost-efficient**  
  Pay only for API calls used—no upfront investment.

## SDK Examples

Using an SDK abstracts HTTP details and simplifies file handling. Below are concise examples for major languages:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ReplaceTextInLocalFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ReplaceTextInLocalFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ReplaceTextInLocalFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ReplaceTextInLocalFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ReplaceTextInLocalFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ReplaceTextInLocalFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ReplaceTextInLocalFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ReplaceTextInLocalFile.go" >}}
{{</tab>}}
{{</tabs>}}

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/ReplaceSpreadsheetContent) defines this operation for direct REST interactions or code generation.
