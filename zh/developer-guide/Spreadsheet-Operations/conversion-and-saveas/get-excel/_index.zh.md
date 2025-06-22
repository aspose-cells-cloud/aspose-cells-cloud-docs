---
title: 将 Excel 文件转换为其他格式
second_title: Aspose.Cells Cloud Documen
linktitle: 获取 Exce
type: docs
url: /zh/get different formats files/
aliases: [/export-excel-workbook-to-different-file-formats/, /export-different-formats/]
keywords: Get excel files to kinds of format files
description: Aspose.Cells Cloud REST API 支持将 Excel 文件转换为多种格式的文件。SDK 支持多种开发语言，包括 Android、C#、Go、Java、NodeJS、Perl、PHP、Python、Ruby 和 Swift。
weight: 10
kwords: Excel、Office 云、REST API、电子表格、PDF、CSV、Json、Markdown、将 Excel 文件转换为其他格式
---
此 REST API 指示将 `get` excel 文件转换为不同格式的文件。

**查询参数**

|参数名称|类型|描述|
|:- |:- |:- |
|格式|细绳|文件格式：csv、xls、html、mhtml、ods、pdf、xml、txt、tiff、xlsb、xlsm、xlsx、xltm、xltx、xps、png、jpg、gif、emf、bmp、md、Numbers、wmf、svg等。|
|密码|细绳|打开 Excel 文件所需的密码。|
|是否自动调整|细绳|自动调整此工作簿的行宽和列宽。默认值为 false。|
|仅保存表|细绳|正确/错误|
|输出路径|细绳|保存结果的路径。如果是单个文件，`outPath` 应包含文件名和扩展名。如果是多个文件，`outPath` 应仅包含文件夹。|
|输出存储名称|细绳|保存的文件所在的存储名称。|
|检查Excel限制|布尔值|当用户修改单元格相关对象时是否检查Excel文件的限制。|
|地区|细绳|工作簿的区域设置。|
|页面宽度适合每张纸|布尔值|页面宽度适合工作表。|
|页面高度适合每张纸|布尔值|页面高度适合工作表。|
|每张纸一页|布尔值|转换为 PDF 格式时，每张纸一页。|
|文件夹|细绳|原始工作簿文件夹。|
|存储名称|细绳|文件所在的存储名称。|

## 休息 API

|**API**|**类型**|**描述**|**Swagger 链接**|
|:- |:- |:- |:- |
|/单元格/{名称}|得到|将工作簿导出为其他格式。|[获取工作簿](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)|

这[OpenAPI规范](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)定义一个可公开访问的编程接口，并允许您直接从 Web 浏览器执行 REST 交互。

您可以使用**cURL**命令行工具可轻松访问 Aspose.Cells 的 Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="1" tabID="11" tabName11="Request" >}}

{{< tab tabNum="11" >}}

```bash

curl -X PUT "https://api.aspose.cloud/v3.0/cells/book1.xlsx?format=pdf" -H "accept: multipart/form-data" -H "Content-Type: multipart/form-data" -H "x-aspose-client: Containerize.Swagger"}
```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK 系列

使用 SDK 是加速开发的最佳方式。SDK 负责处理底层细节，让您专注于项目任务。请查看[GitHub 存储库](https://github.com/aspose-cells-cloud)以获取 Aspose.Cells Cloud SDKs 的完整列表。

以下代码示例演示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}
