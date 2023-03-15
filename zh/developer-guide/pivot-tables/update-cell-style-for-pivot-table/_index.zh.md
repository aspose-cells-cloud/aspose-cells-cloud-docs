---
title: 更新数据透视表的单元格样式
second_title: Aspose.Cells Cloud Documen
linktitle: 格式
type: docs
url: /zh/pivot-tables/format/
aliases: [/update-cell-style-for-pivot-table/]
keywords: Update cell style for a pivot table
description: Aspose.Cells Cloud REST API 支持更新数据透视表的单元格样式。 SDK支持多种开发语言。它们包括 Android、C#、Go、Java、NodeJS、Perl、PHP、Python、Ruby 和 swift
weight: 90
---
此 REST API 指示数据透视表的更新单元格 `style`。
 
## RSET API
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/Format
 
```
请求参数为：
 
|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|姓名|细绳|小路|文档名称。|
|工作表名称|细绳|小路|工作表名称。|
|数据透视表索引|整数|小路|数据透视表索引|
|柱子|整数|询问||
|排|整数|询问||
|风格||身体|在请求正文中设置 dto 样式。|
|需要重新计算|布尔值|询问|错误的|
|文件夹|细绳|询问|文档的文件夹。|
|存储名称|细绳|询问|存储名称。|
 
这[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/PivotTables/PostPivotTableCellStyle)定义了一个可公开访问的编程接口，并允许您直接从 Web 浏览器执行 REST 交互。
 
您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例显示如何使用 cURL 调用 Cloud API。
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "http://api.aspose.com/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0/Format?column=1&row=1" \
-X POST \
-d '{"Font":{"Name":"Arial", "Size":10}}'  \
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
 
 
 
{{< tabs tabTotal="1" tabID="4" tabName1="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "3236805d26482f06f4656b14f2d00d79" >}}

{{< /tab >}}

{{< /tabs >}}




