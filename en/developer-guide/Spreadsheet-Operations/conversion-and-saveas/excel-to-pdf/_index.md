---
title: "Excel to PDF"
second_title: "Aspose.Cells Cloud Document"
linktitle: "Excel to PDF"
type: docs
url: /convert-excel-file-to-pdf-file/
aliases: [/convert-excel-file-to-pdf-in-cloud/,/convert/excel-to-pdf/]
keywords: "Convert excel files to pdf files."
description: "Aspose.Cells Cloud REST API support conversion excel files to pdf files. SDK support kinds of development languages. They include Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby, and swift."
weight: 80
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdwon, Excel to PDF
---

This REST API `saveas` excel file to PDF.

[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) API lets you save MS Excel file as PDF file with additional settings and save the result to the storage.

This REST API `convert` excel file to PDF.

[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) API lets you convert MS Excel file to PDF file with additional settings and save the result to the response.

This REST API `export` excel file to PDF.

[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook  ) API lets you convert MS Excel file to PDF file with additional settings and save the result to the response.

## REST API

|**API**|**Type**|**Description**|**Swagger Link**|
| :- | :- | :- | :- |
|/cells/convert|PUT|Converts workbook from request content to some format|[PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)|
|/cells/{name}|GET|Exports workbook to other format.|[GetWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)|
|/cells/{name}/saveAs|POST|Export workbook to Format|[PostDocumentSaveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)|

These [PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook), [GetWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook), [PostDocumentSaveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) APIs define a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use **cURL** command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL.

{{< tabs tabTotal="3" tabID="11" tabName11="Convert Workbook API"  tabName12="Get Workbook format API" tabName13="Save  Workbook as format API" >}}

{{< tab tabNum="11" >}}

```bash

curl -X PUT "https://api.aspose.cloud/v3.0/cells/convert?format=pdf" -H "accept: multipart/form-data" -H "Content-Type: multipart/form-data" -H "x-aspose-client: Containerize.Swagger" -d {"File":{}}



```

{{< /tab >}}
{{< tab tabNum="12" >}}

```bash

curl -X PUT "https://api.aspose.cloud/v3.0/cells/book1.xlsx?format=pdf" -H "accept: multipart/form-data" -H "Content-Type: multipart/form-data" -H "x-aspose-client: Containerize.Swagger"}


```

{{< /tab >}}

{{< tab tabNum="13" >}}

```java

curl -X POST "https://api.aspose.cloud/v3.0/cells/sampleBook.xlsx/SaveAs?newfilename=sample.pdf&isAutoFitRows=true&isAutoFitColumns=true" -H "accept: multipart/form-data" 



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
