---
title: "Aspose.Cells Cloud – Convert Excel Workbook to PDF, CSV, HTML, and More (GET /cells/{name})"
second_title: "Document"
linktitle: "Convert Excel"
type: docs
url: /get-different-formats-files/
aliases:
  - /export-excel-workbook-to-different-file-formats/
  - /export-different-formats/
keywords: "Aspose.Cells, Excel conversion, convert Excel, PDF, CSV, HTML, ODS, JSON, image formats, spreadsheet export"
description: "Learn how to retrieve an Excel workbook in any format (PDF, CSV, HTML, PNG, etc.) using Aspose.Cells Cloud REST API. Includes cURL, SDK samples, authentication, and response details."
weight: 10
---

This REST API retrieves an Excel workbook in a different format.  

**Version:** v3.0 | **Last Updated:** 2024‑11‑01  

**Query Parameters**

| Parameter Name            | Type   | Description                                                                                                                                                     | Default |
|---------------------------|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|---------|
| format                    | string | Target file format (e.g., CSV, XLS, HTML, MHTML, ODS, PDF, XML, TXT, TIFF, XLSB, XLSM, XLSX, XLTM, XLTX, XPS, PNG, JPG, GIF, EMF, BMP, MD, Numbers, WMF, SVG, etc.). | – |
| password                  | string | Password required to open the Excel file.                                                                                                                       | – |
| isAutoFit                 | bool   | Automatically fits rows and columns width.                                                                                                                      | false |
| onlySaveTable             | bool   | When **true**, only table data is saved. Accepts `true` or `false`.                                                                                             | false |
| outPath                   | string | Path to save the result. For a single file, include the filename and extension; for multiple files, specify only the folder.                                   | – |
| outStorageName            | string | Name of the storage where the output file will be saved.                                                                                                        | – |
| checkExcelRestriction     | bool   | Checks Excel restrictions when modifying cells or related objects.                                                                                              | false |
| region                    | string | Regional settings applied to the workbook.                                                                                                                      | – |
| pageWideFitOnPerSheet     | bool   | Fits the page width to each worksheet when converting to PDF.                                                                                                   | false |
| pageTallFitOnPerSheet     | bool   | Fits the page height to each worksheet when converting to PDF.                                                                                                  | false |
| onePagePerSheet           | bool   | Generates one PDF page per worksheet.                                                                                                                            | false |
| folder                    | string | Folder path of the original workbook.                                                                                                                            | – |
| storageName               | string | Name of the storage where the source file is located.                                                                                                            | – |

## REST API

**Authentication**  
All requests must include a valid OAuth 2.0 access token. Obtain a token by calling the `/connect/token` endpoint with your client ID and secret, then add the header:

```http
Authorization: Bearer <access_token>
```

**Endpoint**

| API               | Type | Description                     | Swagger Link |
|-------------------|------|---------------------------------|--------------|
| /cells/{name}     | GET  | Exports a workbook to another format. | [GetWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook) |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

### Quick‑Start (Step‑by‑Step)

1. **Obtain an access token** – Follow the authentication steps above.  
2. **Make the request** – Use the example request below, replacing `<access_token>` and file name as needed.  
3. **Save or stream the result** – The API returns the converted file as a binary stream (e.g., PDF).  

### Example Request

You can use the **cURL** command‑line tool to access Aspose.Cells web services. The following example shows a correct GET request with the required authorization header.

{{< tabs tabTotal="1" tabID="11" tabName11="Request" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/book1.xlsx?format=pdf" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: Containerize.Swagger"
```

{{< /tab >}}

{{< /tabs >}}

### Sample Response

**Success (200)** – The API returns the converted file in the requested format.

```http
HTTP/1.1 200 OK
Content-Type: application/pdf
Content-Disposition: attachment; filename="book1.pdf"
Content-Length: 123456

(binary PDF data)
```

**Error (4xx/5xx)** – Example of a JSON error object when the source file is not found.

```json
{
  "error": {
    "code": "FileNotFound",
    "message": "The file 'book1.xlsx' does not exist."
  }
}
```

## Cloud SDK Family

Using an SDK is the fastest way to develop. An SDK abstracts low‑level details so you can focus on your project tasks. Please check the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}

**See Also**

- [Convert Workbook (POST)](https://apireference.aspose.cloud/cells/#/Workbook/ConvertWorkbook)  
- [Save As (GET)](https://apireference.aspose.cloud/cells/#/Workbook/SaveAs)  