---
title: "Excel to Docx"
second_title: "Aspose.Cells Cloud Document"
linktitle: "Excel to Docx"
type: docs
url: /convert/excel-to-docx/
aliases: [/convert-excel-file-to-docx-in-cloud/]
keywords: "Convert excel files to docx files."
description: "Aspose.Cells Cloud REST API support conversion excel files to docx files. SDK support kinds of development languages. They include Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby, and swift."
weight: 90
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdwon, Excel to Docx
---

This REST API `saveas` excel file to Docx.

[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) API lets you save MS Excel file as Docx file with additional settings and save the result to the storage.

This REST API `convert` excel file to Docx.

[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) API lets you convert MS Excel file to Docx file with additional settings and save the result to the response.

This REST API `export` excel file to Docx.

[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook  ) API lets you convert MS Excel file to Docx file with additional settings and save the result to the response.

## REST API

|**API**|**Type**|**Description**|**Swagger Link**|
| :- | :- | :- | :- |
|/cells/convert|PUT|Converts workbook from request content to some format|[PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)|
|/cells/{name}|GET|Exports workbook to other format.|[GetWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)|
|/cells/{name}/saveAs|POST|Export workbook to Format|[PostDocumentSaveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)|

These APIs define a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use **cURL** command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL.

{{< tabs tabTotal="3" tabID="11" tabName11="convert" tabName12="saveas" tabName13="export">}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/convert?format=docx" \
-X PUT \
-d {"File":{}} \
-H "Content-Type:  multipart/form-data" \
-H "Accept:  multipart/form-data" \
-H "Authorization: Bearer <jwt token>"

```

{{< /tab >}}
{{< tab tabNum="12" >}}

```bash

curl -v "https://api.aspose.cloud/v3.0/cells/book1.xlsx/saveas?newfilename=book1.docx" \
-X POST \
-d "{'SaveFormat':'docx'}" \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```

{{< /tab >}}
{{< tab tabNum="13" >}}

```bash

curl -v "https://api.aspose.cloud/v3.0/cells/book1.xlsx?format=docx" \
-X GET \
-d "{'SaveFormat':'docx', 'ExportImagesAsBase64': 'true'}" \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"


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
var request = new PutConvertWorkbookRequest( file: new Dictionary<string, Stream> { {"Book1.xlsx", File.OpenRead("Book1.xlsx") }},   format: "docx" );
cellsApi.PutConvertWorkbook(request);

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
// For complete examples and data files, please go to https://github.com/aspose-cells-cloud/aspose-cells-cloud-java/
    PutConvertWorkbookRequest request = new PutConvertWorkbookRequest();
    request.setFormat("docx");
    HashMap<String,File> fileMap = new HashMap<String,File>(); 
    fileMap.put(localName ,CellsApiUtil.GetFileHolder(localName) ); 
    request.setFile(fileMap);
    this.api.putConvertWorkbook(request);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```go

instance := NewCellsApiService(os.Getenv("ProductClientId"), os.Getenv("ProductClientSecret"))
request := PutConvertWorkbookRequest{File: map[string]string{"Book1.xlsx": "TestData/Book1.xlsx"}, Format: "docx"}
instance.PutConvertWorkbook(&request)

```

{{< /tab >}}

{{< /tabs >}}
