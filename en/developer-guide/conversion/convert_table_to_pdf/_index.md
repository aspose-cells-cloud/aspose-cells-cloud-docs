---
title: "Convert Table to PDF"
ArticleTitle: "Convert Table to PDF – Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "Convert Table to PDF"
type: docs
url: /cells/convert/table/pdf
aliases: []
keywords: "Convert Table PDF, Aspose.Cells, API"
description: "Converts a table of a spreadsheet on a local drive to a PDF file using Aspose.Cells Cloud."
weight: 1000
---

## The Convert Table to PDF of Aspose.Cells Cloud Web Services

This operation reads a spreadsheet file from the local file system, converts its specified table to a PDF document, and returns the converted result. It works entirely on the cloud server, so no intermediate upload to cloud storage is required. The API supports optional parameters for output location, custom fonts, auto‑fitting rows/columns, regional settings, and password‑protected workbooks.

### Web API Endpoint

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/pdf
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name   | Type   | Path/Query String/HTTP Body | Description                                                                                                                                                     |
|------------------|--------|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | File   | FormData                    | Upload spreadsheet file.                                                                                                                                         |
| worksheet        | String | Query                       | Worksheet name of spreadsheet.                                                                                                                                  |
| tableName        | String | Query                       | Table name.                                                                                                                                                      |
| outPath          | String | Query                       | (Optional) The folder path where the workbook is stored. The default is null.                                                                                  |
| outStorageName   | String | Query                       | Output file Storage Name.                                                                                                                                       |
| fontsLocation    | String | Query                       | Use Custom fonts.                                                                                                                                               |
| AutoRowsFit      | Boolean| Query                       | (Optional) Autofits all rows in worksheets.                                                                                                                    |
| AutoColumnsFit   | Boolean| Query                       | (Optional) Autofits all columns in worksheets.                                                                                                                 |
| region           | String | Query                       | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior.                         |
| password         | String | Query                       | The password for opening spreadsheet file.                                                                                                                      |

### Request Body Parameter

| Parameter Name | Type | Description |
|----------------|------|-------------|
| *None* | *None* | *No JSON body is required; the file is sent via multipart/form-data.* |

### **Response**

```json
{
  "file": "<binary PDF content>"
}
```

**Response Status Codes**

| Code | Meaning | Description |
|------|---------|-------------|
| 200 | OK | The table was successfully converted to PDF; the response body contains the PDF file stream. |
| 400 | Bad Request | Invalid request parameters or malformed URL. |
| 401 | Unauthorized | Authentication has failed, or no credentials were provided. |
| 404 | Not Found | Source file not accessible or worksheet/table not found. |
| 413 | Payload Too Large | The uploaded spreadsheet exceeds the allowed size limit. |
| 500 | Internal Server Error | An error occurred while converting the spreadsheet to PDF. |

## How to Use the Convert Table to PDF with SDKs

### Convert Table to PDF Specification

The [Convert Table to PDF API Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToPdf) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the cURL command-line tool to access Aspose.Cells Cloud web services easily. The following example shows how to make calls to the Cloud API with cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}

{< tab tabNum="1" >}

```bash
# Use HTTPS for a secure connection
curl -v "https://api.aspose.cloud/v4.0/cells/convert/table/pdf?worksheet={worksheet}&tableName={tableName}&outPath={outPath}&outStorageName={outStorageName}&fontsLocation={fontsLocation}&AutoRowsFit={AutoRowsFit}&AutoColumnsFit={AutoColumnsFit}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/pdf" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "file": "<binary PDF content>"
}
```

{< /tab >}

{< /tabs >}

### Use Aspose Cells Cloud SDKs

Using an SDK is the fastest way to accelerate development. An SDK abstracts low‑level details, allowing you to focus on your project tasks. Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells Cloud web services using various SDKs:
```csharp
// SDK example code for C#
var apiInstance = new ConversionApi();
var file = File.ReadAllBytes("sample.xlsx");
var response = apiInstance.ConvertTableToPdf(
    file,
    worksheet: "Sheet1",
    tableName: "Table1",
    outPath: null,
    outStorageName: null,
    fontsLocation: null,
    AutoRowsFit: null,
    AutoColumnsFit: null,
    region: null,
    password: null);
File.WriteAllBytes("output.pdf", response);
```

```java
// SDK example code for Java
ConversionApi apiInstance = new ConversionApi();
byte[] file = Files.readAllBytes(Paths.get("sample.xlsx"));
byte[] result = apiInstance.convertTableToPdf(
    file,
    "Sheet1",
    "Table1",
    null,
    null,
    null,
    null,
    null,
    null,
    null);
Files.write(Paths.get("output.pdf"), result);
```

```python
# SDK example code for Python
api_instance = conversion_api.ConversionApi()
with open("sample.xlsx", "rb") as f:
    file_bytes = f.read()
pdf_bytes = api_instance.convert_table_to_pdf(
    file=file_bytes,
    worksheet="Sheet1",
    table_name="Table1")
with open("output.pdf", "wb") as out_file:
    out_file.write(pdf_bytes)
```

`[TBD]`