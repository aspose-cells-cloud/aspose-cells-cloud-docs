---
title: "Convert an Excel File to Different Formats"
second_title: "Aspose.Cells Cloud Document"
linktitle: "Convert Spreadsheet "
type: docs
url: /convert-a-spread-file-to-different-formats/
keywords: "Convert excel files to kinds of format files."
description: "Aspose.Cells Cloud REST API support conversion excel files to kinds of format files. SDK support kinds of development languages. They include Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby, and swift."
weight: 10
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdown, Convert Excel
---

This REST API indicates to `convert` an Excel file to a different format. It supports different formats. It can also set page setup and save options before converting.

**Request Body Parameter**

|Parameter Name|Type|Description|
| :- | :- | :- |
|[ConvertWorkbookOptions](/cells/convert-workbook-options/)|object | Convert Workbook Options. |

**Response**

[FileInfo](/cells/file-info/)

## REST API

|**API**|**Type**|**Description**|**Swagger Link**|
| :- | :- | :- | :- |
|/cells/convert|POST|Converts workbook from request content to some format|[PostConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PostConvertWorkBook)|

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Workbook/PostConvertWorkBook) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use **cURL** command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```java

curl -X POST "https://api.aspose.cloud/v3.0/cells/convert" 
     -H "accept: multipart/form-data" 
     -H "Content-Type: multipart/form-data" 
     -H "x-aspose-client: curl" 
     -d {}
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```

{
  "Filename": "filename",
  "FileSize": xxxx,
  "FileContent": "File Content: base64_encoded_string"
}

```

## Cloud SDK Family

Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

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
