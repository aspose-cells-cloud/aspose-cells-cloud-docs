---
title: "Excel to SQL"
second_title: "Document"
linktitle: "Excel to SQL"
type: docs
url: /convert-excel-file-to-sql-file/
keywords: "Aspose.Cells, Excel to SQL, cloud API, spreadsheet conversion, REST"
description: "Use Aspose.Cells Cloud REST API to convert Excel spreadsheets into SQL files. Supports multiple SDKs and programming languages for seamless integration into your applications."
weight: 100
ArticleTitle: "Convert Excel to SQL – Aspose.Cells Cloud API"
---

This REST API converts a spreadsheet file to an SQL format file.

**Prerequisites**  
To use this endpoint you must have a valid JWT token generated as described in the <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a> guide. The API supports Excel files up to the size limits defined in the service documentation and can handle password‑protected workbooks when the `password` query parameter is supplied.

## PostConvertWorkbookToSQL API

```http
POST https://api.aspose.cloud/v3.0/cells/convert/sql
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### **Query Parameter**

| Parameter Name        | Type   | Description                                                                             |
| --------------------- | ------ | --------------------------------------------------------------------------------------- |
| password              | string | Password required to open the Excel file.                                               |
| storageName           | string | Name of the storage where the file is stored.                                           |
| checkExcelRestriction | bool   | Indicates whether to check Excel file restrictions when modifying cell‑related objects. |

### **Request Body Parameter**

| Parameter Name | Type      | Description                                                                      |
| -------------- | --------- | -------------------------------------------------------------------------------- |
| datafile       | data file | The spreadsheet file to be converted, included as the first part of the request. |

### Response

The API returns a **FileInfo** object that contains the generated sql file.

| Field           | Type   | Description                                   |
| --------------- | ------ | --------------------------------------------- |
| **Filename**    | string | Name of the sql file (e.g., `example.sql`). |
| **FileSize**    | int    | Size of the file in bytes.                    |
| **FileContent** | string | Base64‑encoded content of the sql file.      |

[FileInfo](/cells/file-info/)

**HTTP Status Codes**

| Code | Meaning                     | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filter applied successfully; response contains operation details. |
| 400  | Bad Request                 | Missing or invalid parameters (e.g., unsupported file type). |
| 401  | Unauthorized                | Invalid or missing JWT token. |
| 413  | Payload Too Large           | Uploaded file exceeds size limit. |
| 500  | Internal Server Error       | Unexpected server error. |
## How to Use the PostConvertWorkbookToSQL API with SDKs

### PostConvertWorkbookToSQL API Specification

The <a href="https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToSQL" rel="noopener noreferrer">OpenAPI Specification</a> defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the **cURL** command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/sql" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: curl" \
     -d '{"File":{}}'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "example.sql",
  "FileSize": 1024,
  "FileContent": "base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

### Use Aspose.Cells Cloud SDKs

Using an SDK is the best way to speed up development. An SDK handles low‑level details, allowing you to focus on your project tasks. Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:
{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToSQL.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToSQL.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToSQL.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToSQL.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToSQL.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToSQL.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToSQL.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToSQL.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Other APIs Implementing This Function

- **[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)** – Saves a workbook in a different format and stores the result in the specified storage.

- **[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)** – Converts a workbook to another format with optional settings and returns the result in the response.

- **[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)** – Retrieves a workbook with optional conversion settings.

**Notes**  
- When converting password‑protected Excel files, ensure the `password` query parameter is supplied; otherwise the conversion will fail with a 400 error.  
- The service returns the SQL file content as Base64; decode it before saving to a `.sql` file.  

**Sample Files**  
Download a sample Excel workbook [here](https://example.com/sample.xlsx) and a pre‑generated SQL result [here](https://example.com/sample.sql) to test the API quickly.