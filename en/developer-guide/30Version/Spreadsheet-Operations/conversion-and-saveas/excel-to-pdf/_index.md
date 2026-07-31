---
title: "Convert Excel to PDF – Aspose.Cells Cloud API"
ArticleTitle: "Convert Excel to PDF – Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "Convert Excel to PDF"
type: docs
url: /convert-excel-file-to-pdf-file/
aliases: [/convert-excel-file-to-pdf-in-cloud/, /convert/excel-to-pdf/]
keywords: "Aspose, Cells, Excel, PDF, conversion, Cloud API"
description: "Learn how to convert Excel workbooks to PDF with Aspose.Cells Cloud REST API. Includes cURL, SDK samples (C#, Java, Python) and authentication guide."
weight: 80
---

This REST API converts a spreadsheet file to a PDF‑format file. **Prerequisites:** Obtain a valid JWT access token, ensure the source Excel file is stored in a supported storage, and have appropriate permissions to invoke the conversion endpoint.

## REST API

```http
POST https://api.aspose.cloud/v3.0/cells/convert/pdf
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### **Query Parameter**

| Parameter Name        | Type   | Description                                                                     |
| :-------------------- | :----- | :------------------------------------------------------------------------------ |
| password              | string | Password to open the Excel file.                                                |
| storageName           | string | The name of the storage where the file is located.                              |
| checkExcelRestriction | bool   | Whether to enforce Excel file restrictions when modifying cell‑related objects. |

`checkExcelRestriction` defaults to `false` if omitted.

### **Request Body Parameter**

| Parameter Name | Type | Description                                                     |
| :------------- | :--- | :-------------------------------------------------------------- |
| datafile       | file | The data file saved as the first part of the multipart content. |

### **Response**

[FileInfo](/cells/file-info/)

The response returns a JSON object with file metadata. The PDF file itself can be downloaded using the provided `FileContent` (base64) or via the `FileInfo` link. The API returns a JSON object of type **FileInfo**:

- **FileInfo** – object containing the name, size, and base‑64‑encoded content of the generated **PDF** file.

```json
{
  "Filename": "example.pdf",
  "FileSize": 12345,
  "FileContent": "base64_encoded_string"
}
```

#### HTTP Status Codes

| Status Code | Description |
|------------|-------------|
| 200 OK | File converted successfully; response contains PDF file information. |
| 400 Bad Request | Invalid request parameters or malformed file. |
| 401 Unauthorized | Missing or invalid access token. |
| 500 Internal Server Error | Server‑side error during conversion. |



## How to Use the PostConvertWorkbookToPDF API with SDKs

### PostConvertWorkbookToPDF API Specification


The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPDF) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

**Request Headers**

| Header        | Type   | Description                                            |
| :------------ | :----- | :----------------------------------------------------- |
| Authorization | string | Bearer token obtained via JWT authentication.         |
| Content-Type  | string | Must be `multipart/form-data` for file upload.        |
| Accept        | string | `application/json` to receive the response metadata. |

You can use the **cURL** command‑line tool to access Aspose.Cells web services easily. Include an access token in the `Authorization` header, then run the request below.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/pdf" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "Authorization: Bearer <access_token>" \
     -F "datafile=@sample.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "xxxxxx.pdf",
  "FileSize": xxxx,
  "FileContent": "File Content: base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}


### Use Aspose.Cells Cloud SDKs


Using an SDK can simplify development by handling low‑level details. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:
{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToPDF.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToPDF.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToPDF.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToPDF.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToPDF.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToPDF.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToPDF.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToPDF.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Other APIs that implement this function

| **API**        | **Type** | **Description**                                                 | **Swagger Link**                                                                            |
| :------------- | :------- | :-------------------------------------------------------------- | :------------------------------------------------------------------------------------------ |
| /cells/convert | PUT      | Converts a workbook from request content to a specified format. | [PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) |

[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) API lets you save an MS Excel file as a PDF with additional settings and store the result in the storage.

This REST API converts an Excel file to PDF.

[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) API lets you convert an MS Excel file to PDF with additional settings and return the result in the response.

[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook) API lets you convert an MS Excel file to PDF with additional settings and return the result in the response.

These [PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook), [GetWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook), and [PostDocumentSaveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) APIs define a publicly accessible programming interface and allow you to perform REST interactions directly from a web browser.

For additional conversion options, see the [Save Options](/cells/save-options/) page.