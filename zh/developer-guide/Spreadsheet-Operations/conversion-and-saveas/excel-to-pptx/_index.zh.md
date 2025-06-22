---
title: Excel 至 Ppt
second_title: Aspose.Cells Cloud Documen
linktitle: Excel 至 Ppt
type: docs
url: /zh/convert-excel-file-to-pptx-file/
keywords: Convert excel files to pptx files
description: Aspose.Cells Cloud REST API 支持将 Excel 文件转换为 PPTX 文件。SDK 支持多种开发语言，包括 Android、C#、Go、Java、NodeJS、Perl、PHP、Python、Ruby 和 Swift。
weight: 90
kwords: Excel、Office 云、REST API、电子表格、PDF、CSV、Json、Markdown、Excel 至 Pptx
---
此 REST API 指示将 `convert` 电子表格文件转换为 pptx 格式文件。

**查询参数**

|参数名称|类型|描述|
|:- |:- |:- |
|密码|细绳|打开 Excel 文件所需的密码。|
|存储名称|细绳|文件所在的存储名称。|
|检查Excel限制|布尔值|当用户修改单元格相关对象时是否检查Excel文件的限制。|

**请求体参数**

|参数名称|类型|描述|
|:- |:- |:- |
|数据文件|数据文件|数据文件保存到多部分内容的第一部分。|

**回复**

[文件信息](/cells/zh/file-info/)

## REST API 规范

|**API**|**类型**|**描述**|**Swagger 链接**|
|:- |:- |:- |:- |
|/单元格/转换/pptx|邮政|将电子表格转换为 pptx 文件。|[PostConvertWorkbookToPptx](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPptx)|

这[OpenAPI规范](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPptx)定义一个可公开访问的编程接口，并允许您直接从 Web 浏览器执行 REST 交互。

您可以使用**cURL**命令行工具可轻松访问 Aspose.Cells 的 Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```java

curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/pptx" 
     -H "accept: multipart/form-data" 
     -H "Content-Type: multipart/form-data" 
     -H "x-aspose-client: curl" 
     -d {"File":{}}
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```

{
  "Filename": "xxxxxx.pptx",
  "FileSize": xxxx,
  "FileContent": "File Content: base64_encoded_string"
}

```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK 系列

使用 SDK 是加速开发的最佳方式。SDK 负责处理底层细节，让您专注于项目任务。请查看[GitHub 存储库](https://github.com/aspose-cells-cloud)以获取 Aspose.Cells Cloud SDKs 的完整列表。

以下代码示例演示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：
{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToPptx.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToPptx.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToPptx.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToPptx.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToPptx.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToPptx.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToPptx.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToPptx.go" >}}

{{< /tab >}}

{{< /tabs >}}

## 其他API实现此功能

[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) API 允许您将 MS Excel 文件保存为带有附加设置的 Docx 文件，并将结果保存到存储中。

此 REST API `convert` excel 文件转换为 Docx。

[PUT /单元格/转换](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) API 允许您使用附加设置将 MS Excel 文件转换为 Docx 文件，并将结果保存到响应中。

此 REST API `export` excel 文件转换为 Docx。

[获取/单元格/{名称}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook  ) API 允许您使用附加设置将 MS Excel 文件转换为 Docx 文件，并将结果保存到响应中。
