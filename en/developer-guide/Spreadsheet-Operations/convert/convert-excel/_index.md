---
title: "Convert Excel"
second_title: "Aspose.Cells Cloud Document"
linktitle: "Convert"
type: docs
url: /convert/excel-to-different-formats/
aliases: [/convert-excel-workbook-to-different-file-formats/]
keywords: "Convert excel files to kinds of format files."
description: "Aspose.Cells Cloud REST API support conversion excel files to kinds of format files. SDK support kinds of development languages. They include Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby, and swift."
weight: 10
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdwon, Convert Excel
---

This REST API indicates to `convert` excel file to different format file.

The request is an HTTP request with multipart content (see [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) or [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). The first part of the multipart content contains the data file and the second contains save options.

**Query Parameter**

|Parameter Name|Type|Description|
| :- | :- | :- |
|format|string| file format(csv/xls/html/mhtml/ods/pdf/xml/txt/tiff/xlsb/xlsm/xlsx/xltm/xltx/xps/png/jpg/gif/emf/bmp/md/Numbers/wmf/svg) |

**Request Body Parameter**

|Parameter Name|Type|Description|
| :- | :- | :- |
|datafile|data file | The data file save into the first part of the multipart content.|
|SaveOptions|Object | Save option save into the second part of the multipart content.|

## REST API

|**API**|**Type**|**Description**|**Swagger Link**|
| :- | :- | :- | :- |
|/cells/convert|PUT|Converts workbook from request content to some format|[PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)|

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use **cURL** command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL.

{{< tabs tabTotal="1" tabID="11" tabName11="Request" >}}

{{< tab tabNum="11" >}}

```bash

curl -X PUT "https://api.aspose.cloud/v3.0/cells/convert?format=html" -H "accept: multipart/form-data" -H "Content-Type: multipart/form-data" -H "x-aspose-client: Containerize.Swagger" -d {"File":{}}
```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK Family

Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="3" tabID="3" tabName1="C#" tabName2="Java" tabName3="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// For complete examples and data files, please go to https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet/

CellsApi cellsApi = new CellsApi(System.getenv("CellsCloudTestClientId"),System.getenv("CellsCloudTestClientSecret"));
var request = new PutConvertWorkbookRequest( file: new Dictionary<string, Stream> { {"Book1.xlsx", File.OpenRead("Book1.xlsx") }},   format: "pdf" );
cellsApi.PutConvertWorkbook(request);

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
// For complete examples and data files, please go to https://github.com/aspose-cells-cloud/aspose-cells-cloud-java/
    PutConvertWorkbookRequest request = new PutConvertWorkbookRequest();
    request.setFormat("pdf");
    HashMap<String,File> fileMap = new HashMap<String,File>(); 
    fileMap.put(localName ,CellsApiUtil.GetFileHolder(localName) ); 
    request.setFile(fileMap);
    this.api.putConvertWorkbook(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```go

instance := NewCellsApiService(os.Getenv("ProductClientId"), os.Getenv("ProductClientSecret"))
request := PutConvertWorkbookRequest{File: map[string]string{"Book1.xlsx": "TestData/Book1.xlsx"}, Format: "pdf"}
instance.PutConvertWorkbook(&request)

```

{{< /tab >}}

{{< /tabs >}}
