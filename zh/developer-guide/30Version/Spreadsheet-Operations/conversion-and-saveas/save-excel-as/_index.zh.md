---
title: 另存为 Excel
second_title: Documen
linktitle: 保存
type: docs
url: /zh/save-an-excel-file-as-other-formats-files/
aliases: [/convert-excel-workbook-to-different-file-formats/, /saveas-other-formats/]
keywords: Save excel files as kinds of format files
description: Aspose.Cells Cloud REST API 支持将 Excel 文件保存为多种格式。SDK 支持多种开发语言，包括 Android、C#、Go、Java、NodeJS、Perl、PHP、Python、Ruby 和 Swift。
weight: 30
kwords: Excel, Office 云, REST API, 电子表格, PDF, CSV, Json, Markdown, SaveAs Excel
---
此 REST API 指示 `save` excel 文件为不同格式的文件。

**路径参数**

|参数名称|类型|描述|
|:- |:- |:- |
|姓名|细绳|文件名。|

**查询参数**

|参数名称|类型|描述|
|:- |:- |:- |
|新文件名|细绳|新文件名|
|isAutoFitRows|细绳|自动调整此工作簿中的所有行。默认值为 false。|
|是否自动调整列|细绳|自动调整此工作簿的列宽。默认值为 false。|
|文件夹|细绳|原始工作簿文件夹。|
|存储名称|细绳|文件所在的存储名称。|
|输出存储名称|细绳|保存的文件所在的存储名称。|
|检查Excel限制|布尔值|当用户修改单元格相关对象时是否检查Excel文件的限制。|
|地区|细绳|工作簿的区域设置。|
|页面宽度适合每张纸|布尔值|页面宽度适合工作表。|
|页面高度适合每张纸|布尔值|页面高度适合工作表。|
|工作表名称|细绳|转换指定的工作表。|
|页面索引|细绳|转换指定页的工作表，sheetName为必填项。|
|每张纸一页|布尔值|转换为 PDF 格式时，每张纸一页。|

**请求主体参数**

|参数名称|类型|描述|
|:- |:- |:- |
|保存选项|目的|保存选项保存到多部分内容的第二部分。|

## 休息 API

|**API**|**类型**|**描述**|**资源链接**|
|:- |:- |:- |:- |
|/单元格/{名称}/saveAs|邮政|将工作簿导出为格式|[邮寄文件另存为](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)|

这[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)定义一个可公开访问的编程接口，并允许您直接从 Web 浏览器执行 REST 交互。

您可以使用**cURL**命令行工具可轻松访问 Aspose.Cells 的 Web 服务。以下示例展示了如何使用 cURL 调用云端 API。

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```java

curl -X POST "https://api.aspose.cloud/v3.0/cells/sampleBook.xlsx/SaveAs?newfilename=sample.pdf&isAutoFitRows=true&isAutoFitColumns=true" -H "accept: multipart/form-data" 

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```java

{
  "SaveResult": {
    "SourceDocument": {
      "Href": "test.xlsx",
      "Rel": null,
      "Title": null,
      "Type": null
    },
    "DestDocument": {
      "Href": "test.pdf",
      "Rel": null,
      "Title": null,
      "Type": null
    },
    "AdditionalItems": []
  },
  "Code": 200,
  "Status": "OK"
}

```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK 系列

使用 SDK 是加速开发的最佳方式。SDK 负责处理底层细节，让您专注于项目任务。请查看[GitHub 存储库](https://github.com/aspose-cells-cloud)以获取 Aspose.Cells Cloud SDKs 的完整列表。

以下代码示例演示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorkbookSaveAs.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorkbookSaveAs.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorkbookSaveAs.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorkbookSaveAs.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorkbookSaveAs.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorkbookSaveAs.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorkbookSaveAs.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorkbookSaveAs.go" >}}

{{< /tab >}}

{{< /tabs >}}
