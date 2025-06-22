---
title: 在 Excel 工作表中添加列表对象
second_title: Aspose.Cells Cloud Documen
linktitle: 广告
type: docs
url: /zh/list-objects/add/
aliases: [/add-a-list-object-or-table-inside-the-worksheet/,/tables/add/]
keywords: Add a list object(table) into an Excel worksheet
description: Aspose.Cells Cloud REST API 支持将列表对象（表格）添加到 Excel 工作表中。SDK 支持多种开发语言，包括 Android、C#、Go、Java、NodeJS、Perl、PHP、Python、Ruby 和 Swift。
weight: 10
kwords: Excel、Office 云、REST API、电子表格、PDF、CSV、Json、Markdown、在 Excel 工作表中添加列表对象
---
此 REST API 表示 Excel 工作表中的 `add a list object(table)`。

## 重新设置 API

```bash
 
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects
 
```

请求参数为：

|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|姓名|细绳|小路|文档名称。|
|工作表名称|细绳|小路|工作表名称。|
|起始行|整数|询问|列表范围的起始行。|
|起始列|整数|询问|列表范围的起始行。|
|结束行|整数|询问|列表范围的起始行。|
|结束列|整数|询问|列表范围的起始行。|
| hasHeaders|布尔值|询问|真的|
|列表对象||身体|列表对象|
|文件夹|细绳|询问|文档的文件夹。|
|存储名称|细绳|询问|存储名称。|

这[OpenAPI规范](https://apireference.aspose.cloud/cells/#/ListObjects/PutWorksheetListObject)定义一个可公开访问的编程接口，并允许您直接从 Web 浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells 的 Web 服务。以下示例展示了如何使用 cURL 调用云端 API。

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
 
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects?startRow=1&startColumn=1&endRow=10&endColumn=12&hasHeaders=true" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```bash
{
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

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetListObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetListObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetListObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetListObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetListObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetListObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetListObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetListObject.go" >}}

{{< /tab >}}

{{< /tabs >}}
