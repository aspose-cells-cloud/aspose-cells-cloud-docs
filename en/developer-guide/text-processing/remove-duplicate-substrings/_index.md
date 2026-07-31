---
title: "Aspose.Cells Cloud Remove Duplicate Substrings Web API - Deduplicate Repeated Text in Excel"
second_title: "Document"
ArticleTitle: "Excel Duplicate Substring Remover – Clean Repeated Text in Cells"
linktitle: "Remove Duplicate Substrings"
type: docs
url: /remove-duplicate-substrings/
keywords: "Aspose.Cells, duplicate substrings, Excel duplicate substring remover, text cleaning, cloud API"
description: "Remove duplicate substrings from Excel cells using Aspose.Cells Cloud API while preserving formatting, data validation, and workbook structure."
weight: 100
---

Remove duplicate substrings from Excel cells with intelligent detection. Keep original formatting intact while eliminating redundant text using Aspose.Cells deduplication API.

## **Introduction**: Remove Unwanted Characters with Precision

The Repeat Substring Cleaner API removes duplicate substrings within individual cells of an Excel range while preserving cell formatting, data validation, and other workbook structures. It processes each cell independently, keeping only the first occurrence of each duplicate substring.

**Prerequisites** – To use this API you must have an active Aspose Cloud account, a valid JWT access token, and the workbook you wish to process uploaded to Aspose Cloud storage or included in the request payload.

### **Data Source Options**

| Field      | Type   | Required | Description                                             |
| ---------- | ------ | -------- | ------------------------------------------------------- |
| `workbook` | file   | Yes      | Excel workbook file (.xlsx, .xlsm)                     |
| `range`    | string | Yes      | Target range to process (e.g., "A1:D100", "Sheet1!A:D") |

### **Delimiter Options**

| Field                               | Type    | Default    | Description                                                                                                                                               |
| ----------------------------------- | ------- | ---------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `delimiters`                        | string  | `"preset"` | Options: `preset`, `custom`, `comma`, `semicolon`, `space`, `tab`, `line-break` or a custom delimiter string (multiple characters are treated as a composite) |
| `treatConsecutiveDelimitersAsOne`  | boolean | `false`    | Collapse adjacent delimiters into a single separator                                                                                                      |
| `caseSensitive`                    | boolean | `false`    | Determines whether the comparison is case‑sensitive. When `false`, case is ignored during duplicate detection.                                            |

## **RemoveDuplicateSubstrings API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/content/remove/duplicate-substrings
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### The request parameters of **RemoveDuplicateSubstrings** API are

| Parameter Name                  | Type    | Path/Query String/HTTPBody | Description                                                                                                                                                                       |
| :------------------------------ | :------ | :------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet                     | File    | FormData                   | The spreadsheet file to be processed. Supported formats include XLSX, XLS, ODS, CSV, etc.                                                                                         |
| delimiters                      | String  | Query                      | Specifies one or more delimiter characters used to split cell content into substrings for duplicate detection and removal. Multiple delimiters can be specified (e.g., `",;"`). |
| treatConsecutiveDelimitersAsOne | Boolean | Query                      | When set to `true`, consecutive delimiter characters are treated as a single separator. When `false`, each delimiter is processed individually.                                   |
| caseSensitive                   | Boolean | Query                      | When `true`, duplicate detection considers letter case (e.g., "Text" ≠ "text"). When `false`, case is ignored during duplicate comparison.                                        |
| worksheet                       | String  | Query                      | _(Optional)_ The name of the worksheet where duplicate substring removal will be applied. If omitted, the operation applies to the first worksheet.                               |
| range                           | String  | Query                      | _(Optional)_ The cell range where duplicate substring removal will be applied (e.g., `"A1:C10"`). If omitted, the operation applies to all used cells in the specified worksheet. |
| outPath                         | String  | Query                      | _(Optional)_ The cloud storage folder path where the processed workbook will be saved. If omitted, the file is saved in the source folder.                                        |
| outStorageName                  | String  | Query                      | The name of the cloud storage where the output file will be stored.                                                                                                               |
| region                          | String  | Query                      | _(Optional)_ Sets the locale for text processing, which may affect delimiter interpretation and case‑sensitivity rules for certain languages (e.g., `"en-US"`, `"tr-TR"`).        |
| password                        | String  | Query                      | _(Optional)_ If the uploaded spreadsheet is password‑protected, provide the password to open and process the file.                                                                |

**Example request (cURL)**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/content/remove/duplicate-substrings?delimiters=comma&caseSensitive=false" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@Sample.xlsx" \
     -F "range=A1:D100"
```

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

The response returns a file stream containing the processed workbook. The stream can be saved directly to disk or streamed to a client application.

### **Status Code**

| Code | Meaning                                 | Description                                                                                     |
|------|-----------------------------------------|-------------------------------------------------------------------------------------------------|
| 200  | OK                                      | The request succeeded and the processed workbook is returned.                                   |
| 202  | Accepted                                | The request is accepted for asynchronous processing.                                            |
| 400  | Bad Request                             | The request is malformed or contains invalid parameters.                                        |
| 401  | Unauthorized                            | Authentication failed or token is missing/invalid.                                              |
| 404  | Not Found                               | The specified workbook or resource could not be found.                                          |
| 500  | Internal Server Error                   | An unexpected error occurred on the server side.                                                |

**Rate‑Limit Note** – The API is subject to standard Aspose Cloud rate limits. Exceeding the allowed number of calls within a given time window will result in a `429 Too Many Requests` response. Refer to your account dashboard for specific limits.

## Where should we use the Remove Duplicate Substrings API?

- **Data Cleaning & Standardization Scenarios**: Clean up tags like `"VIP,Premium,VIP,Gold"` → `"VIP,Premium,Gold"`.
- **Technical & Operational Data**: Clean log entries with repeated error codes, remove duplicate bin/rack identifiers, and so on.
- **Content & Media Management**: Deduplicate skill tags, remove redundant certification entries.

## Why should you use the Remove Duplicate Substrings API?

- **Automate Manual Tasks**: Eliminate tedious editing and reduce human error.  
- **Preserve Data Integrity**: Cell colors, fonts, borders, and conditional formatting remain unchanged; drop‑down lists and validation rules are preserved.  
- **Flexible Processing**: Delimiter‑agnostic with optional case‑sensitivity control and header protection.  
- **Developer‑Friendly**: Aspose.Cells Cloud provides SDK libraries in multiple languages, enabling quick development with comprehensive documentation.  
- **Cost‑Effective**: The operation is performed in the cloud, avoiding the need to store intermediate files locally.  

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/RemoveDuplicateSubstrings) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the best way to accelerate development. The SDK handles the underlying details, allowing you to simply implement duplicate‑substring removal for cells with minimal code. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples illustrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_RemoveCharactersWithFirstNCharacters.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_RemoveCharactersWithFirstNCharacters.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_RemoveCharactersWithFirstNCharacters.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_RemoveCharactersWithFirstNCharacters.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_RemoveCharactersWithFirstNCharacters.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_RemoveCharactersWithFirstNCharacters.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_RemoveCharactersWithFirstNCharacters.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_RemoveCharactersWithFirstNCharacters.go" >}}
{{</tab>}}
{{< /tabs >}}