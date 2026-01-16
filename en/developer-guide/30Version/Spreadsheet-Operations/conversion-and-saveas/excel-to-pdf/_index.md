---
title: "Excel to PDF"
second_title: "Document"
linktitle: "Excel to PDF"
type: docs
url: /convert-excel-file-to-pdf-file/
aliases: [/convert-excel-file-to-pdf-in-cloud/,/convert/excel-to-pdf/]
keywords: "Excel to PDF conversion, Aspose.Cells Cloud, spreadsheet to PDF, REST API, SDK support"
description: "Use Aspose.Cells Cloud REST API to convert Excel spreadsheets into PDF files. The service supports multiple SDKs (Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby, Swift) for seamless integration."
weight: 80
---

This REST API converts a spreadsheet file to a PDF‑format file.

**Query Parameter**

| Parameter Name          | Type   | Description                                                                                     |
| :-                      | :-     | :-                                                                                               |
| password                | string | The password required to open the Excel file.                                                   |
| storageName             | string | The name of the storage where the file is located.                                               |
| checkExcelRestriction   | bool   | Whether to check restrictions of the Excel file when the user modifies cell‑related objects.   |

**Request Body Parameter**

| Parameter Name | Type | Description                                                                      |
| :-             | :-   | :-                                                                                |
| datafile       | file | The data file saved as the first part of the multipart content.                  |

**Response**

[FileInfo](/cells/file-info/)

## REST API Specification

| **API**               | **Type** | **Description**                         | **Swagger Link**                                                                 |
| :-                    | :-       | :-                                       | :-                                                                            |
| /cells/convert/pdf    | POST     | Convert a spreadsheet to a PDF file.    | [PostConvertWorkbookToPDF](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPDF) |

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPDF) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the **cURL** command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```java
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/pdf" 
     -H "accept: multipart/form-data" 
     -H "Content-Type: multipart/form-data" 
     -H "x-aspose-client: curl" 
     -d {"File":{}}
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

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK handles low‑level details, allowing you to focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

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

| **API**                | **Type** | **Description**                                                     | **Swagger Link**                                                                 |
| :-                     | :-       | :-                                                                   | :-                                                                            |
| /cells/convert         | PUT      | Converts a workbook from request content to a specified format.    | [PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) |

[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) API lets you save an MS Excel file as a PDF with additional settings and store the result in the storage.

This REST API converts an Excel file to PDF.

[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) API lets you convert an MS Excel file to PDF with additional settings and return the result in the response.

[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook) API lets you convert an MS Excel file to PDF with additional settings and return the result in the response.

These [PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook), [GetWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook), and [PostDocumentSaveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) APIs define a publicly accessible programming interface and allow you to perform REST interactions directly from a web browser.