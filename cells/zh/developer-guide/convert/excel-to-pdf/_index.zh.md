---
title: Excel 至 PD
second_title: Aspose.Cells Cloud Documen
linktitle: Excel 至 PD
type: docs
url: /zh/convert/excel-to-pdf/
aliases: [/convert-excel-file-to-pdf-in-cloud/]
keywords: Convert excel files to pdf files
description: Aspose.Cells Cloud REST API 支持将excel文件转换为pdf文件。 SDK支持多种开发语言。它们包括 Android、C#、Go、Java、NodeJS、Perl、PHP、Python、Ruby 和 swift
weight: 80
---
这个 REST API `saveas` excel 文件到 PDF。

[POST /cells/{名称}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) API 可让您将 MS Excel 文件另存为具有附加设置的 PDF 文件，并将结果保存到存储器中。

这个 REST API `convert` excel 文件到 PDF。

[PUT /细胞/转换](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)API 可让您使用其他设置将 MS Excel 文件转换为 PDF 文件，并将结果保存到响应中。

这个 REST API `export` excel 文件到 PDF。

[获取/单元格/{名称}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook  )API 可让您使用其他设置将 MS Excel 文件转换为 PDF 文件，并将结果保存到响应中。

## 休息 API


|**API**|**类型**|**描述**|**招摇链接**|
|:- |:- |:- |:- |
|/细胞/转换|放|将工作簿从请求内容转换为某种格式|[PutConvert工作簿](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)|
|/细胞/{名称}|得到|将工作簿导出为其他格式。|[获取工作簿](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)|
|/cells/{名称}/saveAs|邮政|将工作簿导出为格式|[后文档另存为](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)|



这些[PutConvert工作簿](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook), [获取工作簿](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook), [后文档另存为](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)API 定义了一个可公开访问的编程接口，并允许您直接从 Web 浏览器执行 REST 交互。

您可以使用**cURL**用于轻松访问 Aspose.Cells Web 服务的命令行工具。以下示例显示如何使用 cURL 调用 Cloud API。




{{< tabs tabTotal="3" tabID="11" tabName11="Convert Workbook API" tabName12="Get Workbook format API" tabName13="Save  Workbook as format API" >}}

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





## 云 SDK 系列

使用 SDK 是加速开发的最佳方式。 SDK 负责处理底层细节，让您专注于项目任务。请查看[GitHub 仓库](https://github.com/aspose-cells-cloud)有关 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例演示如何使用各种 SDK 调用 Aspose.Cells Web 服务：


{{< tabs tabTotal="3" tabID="3" tabName1="C#" tabName2="Java" tabName3="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// For complete examples and data files, please go to https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet/
Aspose.Cells.Cloud.SDK.Api.CellsApi cellsApi = new CellsApi("your client id", "your client secret");
var response = cellsApi.CellsWorkbookPutConvertWorkbook( File.OpenRead(@".\TestData\datasource.xlsx"), "pdf", null, null);
Assert.IsInstanceOf<System.IO.Stream>(response, "response is System.IO.Stream");

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
// For complete examples and data files, please go to https://github.com/aspose-cells-cloud/aspose-cells-cloud-java/
try{
    CellsApi api = new CellsApi(System.getenv("CellsCloudTestClientId"),System.getenv("CellsCloudTestClientSecret"));
    File response = api.cellsWorkbookPutConvertWorkbook(
        new File("TestData\\Book1.xlsx"), "pdf", null, null);
} catch (ApiException e) {
    e.printStackTrace();
}	

```
{{< /tab >}}

{{< tab tabNum="3" >}}

```go
// For complete examples and data files, please go to https://github.com/aspose-cells-cloud/aspose-cells-cloud-go/
CellsAPI := NewCellsApiService(clientId, clientSecret)
args := new(CellsWorkbookPutConvertWorkbookOpts)
args.Format = "pdf"
file, err := os.Open("TestData\\Book1.xlsx")
if err != nil {
	return
}
localVarReturnValue, httpResponse, err := CellsAPI.CellsWorkbookPutConvertWorkbook(file, args)
if err != nil {
	t.Error(err)
} else if httpResponse.StatusCode < 200 || httpResponse.StatusCode > 299 {
	t.Fail()
} else {
	fmt.Printf("\t TestCellsPutConvertWorkbook - %d\n", httpResponse.StatusCode)
}
```

{{< /tab >}}

{{< /tabs >}}
