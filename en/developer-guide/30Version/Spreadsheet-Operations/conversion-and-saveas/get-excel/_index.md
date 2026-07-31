---
title: "Aspose.Cells Cloud – Convert Excel Workbook to PDF, CSV, HTML, and More (GET /cells/{name})"
second_title: "Document"
linktitle: "Convert Excel"
type: docs
url: /get-different-formats-files/
aliases:
  - /export-excel-workbook-to-different-file-formats/
  - /export-different-formats/
keywords: "Aspose.Cells, Excel conversion, convert Excel, PDF, CSV, HTML, ODS, JSON, image formats, spreadsheet export, API, REST"
description: "Learn how to retrieve an Excel workbook in any format (PDF, CSV, HTML, PNG, etc.) using Aspose.Cells Cloud REST API. Includes cURL, SDK samples, authentication, and response details."
weight: 10
ArticleTitle: "Aspose.Cells Cloud – Convert Excel Workbook to PDF, CSV, HTML, and More (GET /cells/{name})"
---

This REST API retrieves an Excel workbook in a different format.

## REST API

```
GET https://api.aspose.cloud/v3.0/cells/{name}
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### **Query Parameters**

| Parameter Name        | Type   | Description                                                                                                                                                          | Default |
| --------------------- | ------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------- |
| format                | string | Target file format (e.g., CSV, XLS, HTML, MHTML, ODS, PDF, XML, TXT, TIFF, XLSB, XLSM, XLSX, XLTM, XLTX, XPS, PNG, JPG, GIF, EMF, BMP, MD, Numbers, WMF, SVG, etc.). | –       |
| password              | string | Password required to open the Excel file.                                                                                                                            | –       |
| isAutoFit             | bool   | Automatically fits rows and columns width.                                                                                                                           | false   |
| onlySaveTable         | bool   | When **true**, only table data is saved. Accepts `true` or `false`.                                                                                                  | false   |
| outPath               | string | Path to save the result. For a single file, include the filename and extension; for multiple files, specify only the folder.                                         | –       |
| outStorageName        | string | Name of the storage where the output file will be saved.                                                                                                             | –       |
| checkExcelRestriction | bool   | Checks Excel restrictions when modifying cells or related objects.                                                                                                   | false   |
| region                | string | Regional settings applied to the workbook.                                                                                                                           | –       |
| pageWideFitOnPerSheet | bool   | Fits the page width to each worksheet when converting to PDF.                                                                                                        | false   |
| pageTallFitOnPerSheet | bool   | Fits the page height to each worksheet when converting to PDF.                                                                                                       | false   |
| onePagePerSheet       | bool   | Generates one PDF page per worksheet.                                                                                                                                | false   |
| folder                | string | Folder path of the original workbook.                                                                                                                                | –       |
| storageName           | string | Name of the storage where the source file is located.                                                                                                                | –       |

### Response

**Success (200)** 

- The API returns a **[Workbook](/cells/workbook/)** object that contains workbook structure info when the `format` query parameter is omitted.

- The API returns the converted file in the requested format when the `format` query parameter specifies a file type.

```http
HTTP/1.1 200 OK
Content-Type: application/pdf
Content-Disposition: attachment; filename="book1.pdf"
Content-Length: 123456

(binary PDF data)
```

**Response Status Codes**

| Code | Meaning                     | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Compression succeeded; response contains compressed file details. |
| 400  | Bad Request                 | Missing or invalid parameters (e.g., unsupported file type). |
| 401  | Unauthorized                | Invalid or missing JWT token. |
| 413  | Payload Too Large           | Uploaded file exceeds size limit. |
| 500  | Internal Server Error       | Unexpected server error. |

> **Notes:**  
> - Large workbooks may take longer to convert; consider increasing the request timeout.  
> - Some formats (e.g., `ODS`) are not supported for certain Excel features such as macros.

## How to Use the GetWorkBook API with SDKs

> **Prerequisites:**  
> - A valid **JWT access token** obtained via the Aspose.Cells authentication flow.  
> - The source workbook must be stored in a supported Aspose storage or supplied directly in the request.  
> - Ensure the API version (`v3.0`) matches the latest released version.

### GetWorkBook API Specification

The <a href="https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook" rel="noopener noreferrer">OpenAPI Specification</a> defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

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

### Use Aspose.Cells Cloud SDKs

Using an SDK is the fastest way to develop. An SDK abstracts low‑level details so you can focus on your project tasks. Please check the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

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

- <a href="https://apireference.aspose.cloud/cells/#/Workbook/ConvertWorkbook" rel="noopener noreferrer">Convert Workbook (POST)</a>  
- <a href="https://apireference.aspose.cloud/cells/#/Workbook/SaveAs" rel="noopener noreferrer">Save As (GET)</a>

---

_Last Updated: 2024-12-01_

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Aspose.Cells Cloud – Convert Excel Workbook to PDF, CSV, HTML, and More (GET /cells/{name})",
  "description": "Documentation for the Aspose.Cells Cloud GET /cells/{name} endpoint that converts Excel workbooks to various formats such as PDF, CSV, HTML, and more.",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "datePublished": "2024-12-01",
  "keywords": "Aspose.Cells, Excel conversion, PDF, CSV, HTML, API, REST, cloud",
  "url": "https://docs.aspose.cloud/cells/get-different-formats-files/",
  "publisher": {
    "@type": "Organization",
    "name": "Aspose"
  }
}
</script>