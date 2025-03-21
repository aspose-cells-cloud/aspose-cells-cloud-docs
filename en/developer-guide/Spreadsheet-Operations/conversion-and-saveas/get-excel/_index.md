---
title: "Gets Excel file to other formats"
second_title: "Aspose.Cells Cloud Document"
linktitle: "Get Other Formats Files"
type: docs
url: /get different formats files/
aliases: [/export-excel-workbook-to-different-file-formats/, /export-different-formats/]
keywords: "Get excel files to kinds of format files."
description: "Aspose.Cells Cloud REST API support get excel files to kinds of format files. SDK support kinds of development languages. They include Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby, and swift."
weight: 10
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdwon, Gets Excel file to other formats
---

This REST API indicates to `get` excel file to different format file.

**Query Parameter**

|Parameter Name|Type|Description|
| :- | :- | :- |
|format|string| file format(csv/xls/html/mhtml/ods/pdf/xml/txt/tiff/xlsb/xlsm/xlsx/xltm/xltx/xps/png/jpg/gif/emf/bmp/md/Numbers/wmf/svg) |
|password|string||
|isAutoFit|string| true/false|
|onlySaveTable|string| true/false|
|outPath|string| new file position.|
|folder|string|Original workbook folder.|
|storageName|string|Storage name.|

## REST API

|**API**|**Type**|**Description**|**Swagger Link**|
| :- | :- | :- | :- |
|/cells/{name}|GET|Exports workbook to other format.|[GetWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)|

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use **cURL** command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL.

{{< tabs tabTotal="1" tabID="11" tabName11="Request" >}}

{{< tab tabNum="11" >}}

```bash

curl -X PUT "https://api.aspose.cloud/v3.0/cells/book1.xlsx?format=pdf" -H "accept: multipart/form-data" -H "Content-Type: multipart/form-data" -H "x-aspose-client: Containerize.Swagger"}
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
CellsApi cellsApi = new CellsApi(Environment.GetEnvironmentVariable("CellsCloudTestClientId"), Environment.GetEnvironmentVariable("CellsCloudTestClientSecret"));
var request = new GetWorkbookRequest(name:  "Book1.xlsx", format: "pdf", folder:  "TestData/In");
cellsApi.GetWorkbook(request);

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
// For complete examples and data files, please go to https://github.com/aspose-cells-cloud/aspose-cells-cloud-java/
GetWorkbookRequest request = new GetWorkbookRequest();
request.setName( "Book1.xlsx");
request.setFormat("pdf");
request.setFolder("TestData/In");
this.api.getWorkbook(request);

```

{{< /tab >}}

{{< tab tabNum="3" >}}

```go
// For complete examples and data files, please go to https://github.com/aspose-cells-cloud/aspose-cells-cloud-go/
instance := NewCellsApiService(os.Getenv("ProductClientId"), os.Getenv("ProductClientSecret"), "https://api.aspose.cloud", "v3.0")
localNameRequest := UploadFileRequest{UploadFiles: map[string]string{"Book1.xlsx": "TestData/Book1.xlsx"}, Path: "TestData/In/Book1.xlsx"}
instance.UploadFile(&localNameRequest)
request := GetWorkbookRequest{Name: "Book1.xlsx", Folder: "TestData/In/", Format: "csv"}
instance.GetWorkbook(&request)

```

{{< /tab >}}

{{< /tabs >}}
