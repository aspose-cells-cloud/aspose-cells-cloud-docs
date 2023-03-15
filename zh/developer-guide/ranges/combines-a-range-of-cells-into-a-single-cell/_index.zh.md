---
title: 将 Cells 的范围组合成单个 Cel
second_title: Aspose.Cells Cloud Documen
linktitle: 合并
type: docs
url: /zh/ranges/merge/
aliases: [/combines-a-range-of-cells-into-a-single-cell/]
keywords: Merge a range of cells into a single cell
description: Aspose.Cells Cloud REST API 支持将一系列单元格合并为 Excel 工作表上的单个单元格。 SDK支持多种开发语言。它们包括 Android、C#、Go、Java、NodeJS、Perl、PHP、Python、Ruby 和 swift
weight: 20
---
此 REST API 指示将一系列单元格合并到 Excel 工作表上的单个单元格中。
            
 
## RSET API
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/merge
 
```
请求参数为：
 
|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|姓名|细绳|小路|工作簿名称|
|工作表名称|细绳|小路|工作表名称|
|范围||身体|工作表中的范围|
|文件夹|细绳|询问|工作簿文件夹。|
|存储名称|细绳|询问|存储名称。|
 
这[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeMerge)定义了一个可公开访问的编程接口，并允许您直接从 Web 浏览器执行 REST 交互。
 
您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例显示如何使用 cURL 调用 Cloud API。
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/merge" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
-d "{ \"ColumnCount\": 7, \"ColumnWidth\": 19, \"FirstColumn\": 0, \"FirstRow\": 9, \"Name\": \"string\", \"RefersTo\": \"string\", \"RowCount\": 1, \"RowHeight\": 15, \"Worksheet\": \"Sheet1\"}"
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

{{< tabs tabTotal="4" tabID="4" tabName1="PHP" tabName2="Ruby" tabName3="Objective C" tabName4="Go" >}}

{{< tab tabNum="1" >}}



{{< /tab >}}

{{< tab tabNum="2" >}}



{{< /tab >}}

{{< tab tabNum="3" >}}



{{< /tab >}}

{{< tab tabNum="4" >}}



{{< gist "aspose-cells-cloud-gists" "b7ea0337f3f9c6d9e8eed4b0d6bfff63" >}}

{{< /tab >}}

{{< /tabs >}}



