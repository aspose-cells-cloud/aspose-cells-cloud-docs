---
title: 获取 Excel 文件为其他格式
second_title: Aspose.Cells Cloud Documen
linktitle: 葛
type: docs
url: /zh/export-different-formats/
aliases: [/export-excel-workbook-to-different-file-formats/]
keywords: Get excel files to kinds of format files
description: Aspose.Cells Cloud REST API 支持将excel文件转换为各种格式文件。 SDK支持多种开发语言。它们包括 Android、C#、Go、Java、NodeJS、Perl、PHP、Python、Ruby 和 swift
weight: 10
---
此 REST API 表示将 `get` excel 文件转换为不同格式的文件。


**查询参数**

|参数名称|类型|描述|
|:- |:- |:- |
|格式|细绳|文件格式(csv/xls/html/mhtml/ods/pdf/xml/txt/tiff/xlsb/xlsm/xlsx/xltm/xltx/xps/png/jpg/gif/emf/bmp/md/Numbers/wmf/svg )|
|密码|细绳||
|是自动调整|细绳|真假|
|仅保存表|细绳|真假|
|出路|细绳|新的文件位置。|
|文件夹|细绳|原始工作簿文件夹。|
|存储名称|细绳|存储名称。|



## 休息 API

|**API**|**类型**|**描述**|**招摇链接**|
|:- |:- |:- |:- |
|/细胞/{名称}|得到|将工作簿导出为其他格式。|[获取工作簿](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)|


这[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)定义了一个可公开访问的编程接口，并允许您直接从 Web 浏览器执行 REST 交互。

您可以使用**cURL**用于轻松访问 Aspose.Cells Web 服务的命令行工具。以下示例显示如何使用 cURL 调用 Cloud API。


{{< tabs tabTotal="1" tabID="11" tabName11="Request" >}}

{{< tab tabNum="11" >}}

```bash

curl -X PUT "https://api.aspose.cloud/v3.0/cells/book1.xlsx?format=pdf" -H "accept: multipart/form-data" -H "Content-Type: multipart/form-data" -H "x-aspose-client: Containerize.Swagger"}
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
Aspose.Cells.Cloud.SDK.Api.LiteCellsApi liteCellsApi = new Aspose.Cells.Cloud.SDK.Api.LiteCellsApi("your client id", "your client secret");
IDictionary<string, Stream> mapFiles = new Dictionary<string, Stream>();
mapFiles.Add("assemblytest.xlsx", File.OpenRead(@".\TestData\assemblytest.xlsx"));
mapFiles.Add("datasource.xlsx", File.OpenRead(@".\TestData\datasource.xlsx"));
Aspose.Cells.Cloud.SDK.Model.FilesResult filesResult = liteCellsApi.PostExport(files, "Workbook", "pdf");
Assert.IsNotNull(filesResult);


```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
// For complete examples and data files, please go to https://github.com/aspose-cells-cloud/aspose-cells-cloud-java/
try{
    LiteCellsApi liteApi = new LiteCellsApi(System.getenv("CellsCloudTestClientId"),System.getenv("CellsCloudTestClientSecret"));
    String AssemblyTestXlsx = "assemblytest.xlsx";
    String DataSourceXlsx = "datasource.xlsx";
    HashMap<String,File> fileMap = new HashMap<String,File>();
    fileMap.put(AssemblyTestXlsx , new File("TestData\\" + AssemblyTestXlsx));
    fileMap.put(DataSourceXlsx , new File("TestData\\" + DataSourceXlsx) );
    FilesResult response = liteApi.postExport(fileMap, "workbook","pdf");
} catch (ApiException e) {
    e.printStackTrace();
}		

```
{{< /tab >}}

{{< tab tabNum="3" >}}

```go
// For complete examples and data files, please go to https://github.com/aspose-cells-cloud/aspose-cells-cloud-go/
LiteCellsAPI := NewLiteCellsApiService(clientId, clientSecret)

var fileMap map[string]string
fileMap = make(map[string]string)
fileMap["Book1.xlsx"] = "TestData\\Book1.xlsx"
fileMap["Book2.xlsx"] = "TestData\\Book2.xlsx"
postOpts := new(PostExportOpts)
postOpts.Format = "pdf"
postOpts.ObjectType = "workbook"
_, httpResponse, err := LiteCellsAPI.PostExport(fileMap, postOpts)
if err != nil {
	t.Error(err)
} else if httpResponse.StatusCode < 200 || httpResponse.StatusCode > 299 {
	t.Fail()
} else {
	fmt.Printf("\tTestCellsPostExport \n")
}


```

{{< /tab >}}

{{< /tabs >}}
