---
title: 在 Excel 工作表上添加形状
second_title: Aspose.Cells Cloud Documen
linktitle: 广告
type: docs
url: /zh/shapes/add/
aliases: [/add-a-shape-inside-the-worksheet/]
keywords: Add shape on an Excel workshee
description: Aspose.Cells Cloud REST API 支持在 Excel 工作表上添加形状。 SDK支持多种开发语言。它们包括 Android、C#、Go、Java、NodeJS、Perl、PHP、Python、Ruby 和 swift
weight: 30
---
此 REST API 指示在 Excel 工作表上添加形状。
 
## RSET API
 
```bash
 
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes
 
```
请求参数为：
 
|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|姓名|细绳|小路|文档名称。|
|工作表名称|细绳|小路|工作表名称。|
|形状DTO||身体||
|图纸类型|细绳|询问|形状对象类型|
|左上行|整数|询问|左上行索引。|
|左上列|整数|询问|左上列索引。|
|顶部|整数|询问|表示 Spinner 相对于其左行的垂直偏移量，以像素为单位。|
|左边|整数|询问|表示 Spinner 相对于其左列的水平偏移量，以像素为单位。|
|宽度|整数|询问|表示 Spinner 的高度，以像素为单位。|
|高度|整数|询问|表示 Spinner 的宽度，以像素为单位。|
|文件夹|细绳|询问|文档的文件夹。|
|存储名称|细绳|询问|存储名称。|
 
这[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Shapes/PutWorksheetShape)定义了一个可公开访问的编程接口，并允许您直接从 Web 浏览器执行 REST 交互。
 
您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例显示如何使用 cURL 调用 Cloud API。
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes?DrawingType=arc&upperLeftRow=1&upperLeftColumn=1&top=1&left=1&width=100&height=100" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}}
 
{{< tab tabNum="2" >}}
 
```bash
{
"Code": 200,
"Status": "OK"
}
 
```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## 云 SDK 系列
 
使用 SDK 是加速开发的最佳方式。 SDK 负责处理底层细节，让您专注于项目任务。请查看[GitHub 仓库](https://github.com/aspose-cells-cloud)有关 Aspose.Cells Cloud SDK 的完整列表。
 
以下代码示例演示如何使用各种 SDK 调用 Aspose.Cells Web 服务：
 
 
{{< tabs tabTotal="5" tabID="4" tabName1="C#" tabName2="Java" tabName3="Perl" tabName4="Go" tabName5="Swift" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-PutWorksheetShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example-PutWorksheetShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example-PutWorksheetShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "34f478cae8c02848db0e376bd592a087" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "f342d1e6f85982e0429fcd9bed8b11a8" "Example-PutWorksheetShape.swift" >}}

{{< /tab >}}

{{< /tabs >}}
