---
title: "Advanced Convert Excel File"
second_title: "Document"
linktitle: "Advanced Convert"
type: docs
url: /advanced-convert-excel/
keywords: "Aspose.Cells, Excel conversion, Cloud API, SDK"
description: "The Aspose.Cells Cloud REST API provides powerful features for converting Excel workbooks to a wide range of formats, configuring page setup, save options, and print settings. SDKs are available for Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby, and Swift, enabling seamless integration across multiple platforms."
weight: 50
ArticleTitle: "Advanced Convert Excel File – Aspose.Cells Cloud API Guide"
---

## Advanced Cloud API for Excel Conversion

The Advanced Convert operation enables you to transform an Excel workbook into various output formats (PDF, HTML, CSV, etc.) while giving you fine‑grained control over page setup, save options, and print settings.  

**API Reference**  
- **Method:** `PUT`  
- **Endpoint:** `/cells/convert`  
- **Parameters:**  
  - `format` (string, required) – Desired output format (e.g., `pdf`, `html`).  
  - `outPath` (string, optional) – Path in cloud storage where the converted file will be saved.  
  - `options` (object, optional) – JSON object containing advanced conversion options such as `pageSetup`, `saveOptions`, and `printSettings`.  
- **Request Body Example:**  
  ```json
  {
    "format": "pdf",
    "outPath": "output/converted.pdf",
    "options": {
      "pageSetup": {
        "orientation": "Landscape",
        "paperSize": "A4"
      },
      "saveOptions": {
        "compress": true
      },
      "printSettings": {
        "printHeadings": false
      }
    }
  }
  ```  
- **Response:**  
  - `200 OK` – Conversion succeeded; response contains the converted file stream or a reference to the saved file.  
  - `400 Bad Request` – Invalid parameters or malformed request body.  
  - `401 Unauthorized` – Authentication failed or token missing.  
  - `500 Internal Server Error` – Server‑side error during conversion.  

### The ability to load spreadsheet files from multiple data sources

### Set Page Setup and Save Options

## Cloud SDK Family

Using an SDK helps accelerate development by handling low‑level details, allowing you to focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutConvertWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutConvertWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutConvertWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutConvertWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutConvertWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutConvertWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutConvertWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutConvertWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}