---
title: "Excel to PDF"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /convert/excel-to-pdf/
aliases: [/convert-excel-file-to-pdf-in-cloud/]
keywords: "REST API, convert, spreadsheets, excel, pdf"
description: "Cells.Cloud API for Excel operate: convert excel file to html file."
weight: 80
---

Aspose provides a high-fidelity API to programmatically convert Excel documents to PDF format and in the opposite directions with professional quality. The combined use of Adobe and Microsoft Office technologies has a lot to offer to the end-user.

These major document formats, including XLSX, XLS, XLSB, and ODS, are capable of encapsulating almost any type of data including text, tables, raster and vector graphics, video, audio, and also support a wide range of formatting features.

Despite similarities, Excel and PDF documents have considerable differences in operational capabilities.

Excel document formats are great for collaborative development, but they aren’t always the best choice for distributing, as they can be easily modified without the author’s permission. PDF documents, in contrast, support multilevel security options and are difficult to extract information. Overall Adobe’s technology makes the forgery of PDF documents a complex task.

You may require to convert an editable XLSX or XLS to an immutable PDF in order to protect the Excel file against undesirable modifications.

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



{{< tabs tabTotal="3" tabID="3" tabName1="C#" tabName2="Go" tabName3="Swift" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "00860c8ef58cebd673190e304b6ddbdf" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "3f950cf3a2682cfa62dbfa542257b744" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cloud" "701965adeefa90bfc9b8ddf2bf7eba20" >}}

{{< /tab >}}

{{< /tabs >}}
