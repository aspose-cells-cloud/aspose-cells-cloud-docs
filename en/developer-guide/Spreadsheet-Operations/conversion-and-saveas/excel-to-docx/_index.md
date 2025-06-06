---
title: "Excel to Docx"
second_title: "Aspose.Cells Cloud Document"
linktitle: "Excel to Docx"
type: docs
url:  convert-excel-file-to-docx-file/
keywords: "Convert excel files to docx files."
description: "Aspose.Cells Cloud REST API support conversion excel files to csv files. SDK support kinds of development languages. They include Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby, and swift."
weight: 90
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdown, Excel to Docx
---

This REST API indicates to `convert` a spreadsheet file to a docx format file.

**Query Parameter**

|Parameter Name|Type|Description|
| :- | :- | :- |
|password|string| The password needed to open an Excel file. |
|storageName|string| The storage name where the file is situated. |
|checkExcelRestriction|bool| Whether check restriction of excel file when user modify cells related objects. |

**Request Body Parameter**

|Parameter Name|Type|Description|
| :- | :- | :- |
|datafile|data file | The data file save into the first part of the multipart content.|

**Response**

[FileInfo](/cells/file-info/)

## REST API Specification

|**API**|**Type**|**Description**|**Swagger Link**|
| :- | :- | :- | :- |
|/cells/convert/docx|POST|Convert a spreadsheet to a docx file.|[PostConvertWorkbookToDocx](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToDocx)|

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToDocx) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use **cURL** command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```java

curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/docx" 
     -H "accept: multipart/form-data" 
     -H "Content-Type: multipart/form-data" 
     -H "x-aspose-client: curl" 
     -d {"File":{}}
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```

{
  "Filename": "xxxxxx.docx",
  "FileSize": xxxx,
  "FileContent": "File Content: base64_encoded_string"
}

```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK Family

Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:
{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToDocx.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToDocx.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToDocx.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToDocx.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToDocx.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToDocx.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToDocx.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToDocx.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Other APIs implement this function

[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) API lets you save MS Excel file as CSV file with additional settings and save the result to the storage.

This REST API `convert` excel file to CSV.

[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) API lets you convert MS Excel file to CSV file with additional settings and save the result to the response.

This REST API `export` excel file to CSV.

[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook  ) API lets you convert MS Excel file to CSV file with additional settings and save the result to the response.
