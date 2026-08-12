---
title: "Aspose.Cells Cloud Web API - Convert a Spreadsheet to another format - Free Online Tool"
second_title: "Document"
ArticleTitle: "How to Convert a Spreadsheet to another format: Step-by-Step Guide"
linktitle: "Convert Spreadsheet"
type: docs
url: /convert-spreadsheet/
keywords: "Aspose, Aspose.Cells, spreadsheet conversion, Excel to PDF, Excel API, cloud file conversion"
description: "Convert a spreadsheet file to another format using the Aspose.Cells Cloud API."
weight: 100
---

Convert a local spreadsheet/Excel file to another format with the Aspose.Cells Cloud Web API.

## **Convert Spreadsheet API**

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/spreadsheet
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### **Request Parameters:**

| Parameter Name | Type   | Path/Query String/HTTPBody | Description                                                                                  |
| :------------- | :----- | :------------------------- | :------------------------------------------------------------------------------------------- |
| Spreadsheet    | File   | FormData                   | Upload the spreadsheet file to be converted.                                                 |
| format         | String | Query                      | (Required) The desired output format (e.g., “XLSX”, “PDF”, “CSV”).                           |
| outPath        | String | Query                      | (Optional) The folder path where the converted workbook will be stored. The default is null. |
| outStorageName | String | Query                      | Specify an output file storage name.                                                         |
| fontsLocation  | String | Query                      | Use custom fonts for the spreadsheet.                                                        |
| region         | String | Query                      | Specify the spreadsheet region setting.                                                      |
| password       | String | Query                      | The password for opening the spreadsheet file if it is protected.                            |

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

**Success status**

- **200 OK** – The conversion succeeded and the response body contains the converted file stream.
- The `Content-Type` header reflects the MIME type of the requested output format (e.g., `application/pdf` for PDF).

**HTTP Status Codes**

| Code | Meaning               | Description                                                       |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK                    | Filter applied successfully; response contains operation details. |
| 400  | Bad Request           | Missing or invalid parameters (e.g., unsupported file type).      |
| 401  | Unauthorized          | Invalid or missing JWT token.                                     |
| 413  | Payload Too Large     | Uploaded file exceeds size limit.                                 |
| 500  | Internal Server Error | Unexpected server error.                                          |

## Format

| **Out Format**                                                                                         | **Description**                                                                                                              |
| :----------------------------------------------------------------------------------------------------- | :--------------------------------------------------------------------------------------------------------------------------- |
| <a href="https://docs.fileformat.com/spreadsheet/xls/" rel="noopener noreferrer">XLS</a>               | Excel 95/5.0 - 2003 Workbook.                                                                                                |
| <a href="https://docs.fileformat.com/spreadsheet/xlsx/" rel="noopener noreferrer">XLSX</a>             | The Office Open XML SpreadsheetML File Format.                                                                               |
| <a href="https://docs.fileformat.com/spreadsheet/xlsb/" rel="noopener noreferrer">XLSB</a>             | Excel Binary Workbook.                                                                                                       |
| <a href="https://docs.fileformat.com/spreadsheet/xlsm/" rel="noopener noreferrer">XLSM</a>             | Excel Macro-Enabled Workbook.                                                                                                |
| <a href="https://docs.fileformat.com/spreadsheet/xlt/" rel="noopener noreferrer">XLT</a>               | Excel 97 - Excel 2003 Template.                                                                                              |
| <a href="https://docs.fileformat.com/spreadsheet/xltx/" rel="noopener noreferrer">XLTX</a>             | Excel Template.                                                                                                              |
| <a href="https://docs.fileformat.com/spreadsheet/xltm/" rel="noopener noreferrer">XLTM</a>             | Excel Macro-Enabled Template.                                                                                                |
| <a href="https://docs.fileformat.com/spreadsheet/xlam/" rel="noopener noreferrer">XLAM</a>             | An Excel Macro-Enabled Add-In file that's used to add new functions to Excel.                                                |
| <a href="https://docs.fileformat.com/spreadsheet/csv/" rel="noopener noreferrer">CSV</a>               | CSV (Comma Separated Value) file.                                                                                            |
| <a href="https://docs.fileformat.com/spreadsheet/tsv/" rel="noopener noreferrer">TSV</a>               | TSV (Tab-separated values) file.                                                                                             |
| <a href="https://docs.fileformat.com/word-processing/txt/" rel="noopener noreferrer">TXT</a>           | Delimited plain-text file.                                                                                                   |
| <a href="https://docs.fileformat.com/web/html/" rel="noopener noreferrer">HTML</a>                     | HTML format.                                                                                                                 |
| <a href="https://docs.fileformat.com/web/mhtml/" rel="noopener noreferrer">MHTML</a>                   | MHTML file.                                                                                                                  |
| <a href="https://docs.fileformat.com/spreadsheet/ods/" rel="noopener noreferrer">ODS</a>               | ODS (OpenDocument Spreadsheet).                                                                                              |
| SpreadsheetML                                                                                          | Excel 2003 XML file.                                                                                                         |
| <a href="https://docs.fileformat.com/spreadsheet/numbers/" rel="noopener noreferrer">Numbers</a>       | The document is created by Apple's “Numbers” application, which is part of the iWork suite for macOS and iOS.                |
| <a href="https://docs.fileformat.com/web/json/" rel="noopener noreferrer">JSON</a>                     | JavaScript Object Notation.                                                                                                  |
| <a href="https://docs.fileformat.com/spreadsheet/dif/" rel="noopener noreferrer">DIF</a>               | Data Interchange Format.                                                                                                     |
| <a href="https://docs.fileformat.com/database/dbf/" rel="noopener noreferrer">DBF</a>                  | The file with a .dbf extension is a database file used by the dBASE database-management system.                              |
| <a href="https://docs.fileformat.com/pdf/" rel="noopener noreferrer">PDF</a>                           | Adobe Portable Document Format.                                                                                              |
| <a href="https://docs.fileformat.com/page-description-language/xps/" rel="noopener noreferrer">XPS</a> | XML Paper Specification format.                                                                                              |
| <a href="https://docs.fileformat.com/page-description-language/svg/" rel="noopener noreferrer">SVG</a> | Scalable Vector Graphics format.                                                                                             |
| <a href="https://docs.fileformat.com/image/tiff/" rel="noopener noreferrer">TIFF</a>                   | Tagged Image File Format.                                                                                                    |
| <a href="https://docs.fileformat.com/image/png/" rel="noopener noreferrer">PNG</a>                     | Portable Network Graphics format.                                                                                            |
| <a href="https://docs.fileformat.com/image/bmp/" rel="noopener noreferrer">BMP</a>                     | Bitmap Image format.                                                                                                         |
| <a href="https://docs.fileformat.com/image/emf/" rel="noopener noreferrer">EMF</a>                     | Enhanced Metafile format.                                                                                                    |
| <a href="https://docs.fileformat.com/image/jpeg/" rel="noopener noreferrer">JPEG</a>                   | JPEG is a type of image format that is saved using lossy compression.                                                        |
| <a href="https://docs.fileformat.com/image/gif/" rel="noopener noreferrer">GIF</a>                     | Graphics Interchange Format.                                                                                                 |
| <a href="https://docs.fileformat.com/word-processing/md/" rel="noopener noreferrer">MARKDOWN</a>       | Represents a Markdown document.                                                                                              |
| <a href="https://docs.fileformat.com/spreadsheet/sxc/" rel="noopener noreferrer">SXC</a>               | An XML-based format used by OpenOffice and StarOffice.                                                                       |
| <a href="https://docs.fileformat.com/spreadsheet/fods/" rel="noopener noreferrer">FODS</a>             | This is an Open Document format stored as flat XML.                                                                          |
| <a href="https://docs.fileformat.com/word-processing/docx/" rel="noopener noreferrer">DOCX</a>         | A well-known format for Microsoft Word documents that combines XML and binary files.                                         |
| <a href="https://docs.fileformat.com/presentation/pptx/" rel="noopener noreferrer">PPTX</a>            | The PPTX format is based on the Microsoft PowerPoint Open XML presentation file format.                                      |
| <a href="https://docs.fileformat.com/database/sql/" rel="noopener noreferrer">SqlScript</a>            | Structured Query Language.                                                                                                   |
| <a href="https://docs.fileformat.com/web/xhtml/" rel="noopener noreferrer">XHtml</a>                   | XHTML is a text-based file format with markup in XML, using a reformulation of HTML 4.0.                                     |
| <a href="https://docs.fileformat.com/ebook/epub/" rel="noopener noreferrer">Epub</a>                   | Files with a .epub extension are an e-book format that provides a standard digital publication for publishers and consumers. |
| <a href="https://docs.fileformat.com/web/xml/" rel="noopener noreferrer">Xml</a>                       | XML stands for Extensible Markup Language; it is similar to HTML but uses tags to define objects.                            |
| <a href="https://docs.fileformat.com/spreadsheet/ots/" rel="noopener noreferrer">Ots</a>               | Open Document Template Sheet (OTS) file.                                                                                     |
| <a href="https://docs.fileformat.com/ebook/azw3/" rel="noopener noreferrer">AZW3</a>                   | AZW is a digital e-book file format developed by Amazon for Kindle devices. AZW3, also known as Kindle Format 8 (KF8).       |

## Where should you use the Convert Spreadsheet API?

- **Legacy System Migration**: Convert thousands of legacy XLS files to XLSX for modern systems.
- **Archive Standardization**: Normalize various spreadsheet formats (XLS, XLSM, ODS, CSV) to a single format for archival.
- **Office Suite Interoperability**: Convert Excel files to formats compatible with LibreOffice, Google Sheets, or Apple Numbers.
- **Data Source Normalization**: Convert various spreadsheet formats to CSV or JSON for database ingestion.
- **Web Publishing**: Convert financial models to HTML for web display.

## Why should you use the Convert Spreadsheet API?

- **Developer-Friendly**: Aspose.Cells Cloud offers SDK libraries in multiple languages, enabling quick development and comes with comprehensive documentation. Compared with building custom chart-rendering solutions, this significantly reduces development workload.
- **Cost-Effective**: You can convert table data without first uploading the workbook, which saves storage space and reduces costs.
- **Comprehensive Format Support**: Convert between 20+ spreadsheet formats.
- **Preserve Data Fidelity & Formatting.**

## How to Use the Convert Spreadsheet API with SDKs?

The following code examples demonstrate how to use the Convert Spreadsheet API with various SDKs.

### Convert Spreadsheet API Specification

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertSpreadsheet" rel="noopener noreferrer">Convert Spreadsheet API Specification</a> defines a publicly accessible programming interface, allowing you to perform REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert?format=pdf \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/file.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="file.pdf"
Content-Length: 8423

```

{{< /tab >}}

{{< /tabs >}}

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away low-level details, allowing you to convert a spreadsheet file to another format with concise code. Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertWorkbook.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertWorkbook.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertWorkbook.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertWorkbook.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertWorkbook.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertWorkbook.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertWorkbook.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertWorkbook.go" >}}
{{</tab>}}
{{< /tabs >}}

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "WebAPI",
  "name": "Convert Spreadsheet",
  "description": "Convert a spreadsheet file to another format using Aspose.Cells Cloud.",
  "url": "https://api.aspose.cloud/v4.0/cells/convert/spreadsheet",
  "documentation": "https://docs.aspose.cloud/cells/convert-spreadsheet/",
  "targetPlatform": "Web",
  "authenticationType": "OAuth2",
  "operation": [
    {
      "@type": "HttpOperation",
      "httpMethod": "PUT",
      "urlTemplate": "/cells/convert/spreadsheet",
      "description": "Convert a spreadsheet to the specified format."
    }
  ]
}
</script>
