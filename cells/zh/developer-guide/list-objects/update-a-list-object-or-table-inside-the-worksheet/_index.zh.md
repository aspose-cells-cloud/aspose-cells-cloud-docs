---
title: 更新 Excel 工作表中的列表对象
second_title: Aspose.Cells Cloud Documen
linktitle: 更新
type: docs
url: /zh/list-objects/update/
aliases: [/update-a-list-object-or-table-inside-the-worksheet/,/tables/update/]
keywords: Update a list object(table) in an Excel worksheet
description: Aspose.Cells Cloud REST API 支持更新 Excel 工作表中的列表对象（表）。 SDK支持多种开发语言。它们包括 Android、C#、Go、Java、NodeJS、Perl、PHP、Python、Ruby 和 swift
weight: 20
---
此 REST API 向 `update` 指示 `list object` 属性。

 
## RSET API
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}
 
```
请求参数为：
 
|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|姓名|细绳|小路|文档名称。|
|工作表名称|细绳|小路|工作表名称。|
|列表对象索引|整数|小路|列表对象索引|
|列表对象||身体|请求正文中的 listObject dto。|
|文件夹|细绳|询问|文档的文件夹。|
|存储名称|细绳|询问|存储名称。|
 
这[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/ListObjects/PostWorksheetListObject)定义了一个可公开访问的编程接口，并允许您直接从 Web 浏览器执行 REST 交互。
 
您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例显示如何使用 cURL 调用 Cloud API。
 
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}
 
{{< tab tabNum="11" >}}
 
```bash
 
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet7/listobjects/0" \
-X POST \
-d "{ \"link\": { \"Href\": \"string\", \"Rel\": \"string\", \"Title\": \"string\", \"Type\": \"string\" }, \"AutoFilter\": { \"link\": { \"Href\": \"string\", \"Rel\": \"string\", \"Title\": \"string\", \"Type\": \"string\" }, \"FilterColumns\": [ { \"FieldIndex\": 0, \"FilterType\": \"string\", \"MultipleFilters\": { \"MatchBlank\": true, \"MultipleFilterList\": [ {} ] }, \"ColorFilter\": { \"FilterByFillColor\": \"string\", \"Pattern\": \"string\", \"Color\": { \"Color\": { \"A\": 0, \"R\": 0, \"G\": 0, \"B\": 0 }, \"ColorIndex\": 0, \"IsShapeColor\": true, \"ThemeColor\": { \"ColorType\": \"string\", \"Tint\": 0 }, \"Type\": \"string\" }, \"ForegroundColorColor\": { \"Color\": { \"A\": 0, \"R\": 0, \"G\": 0, \"B\": 0 }, \"ColorIndex\": 0, \"IsShapeColor\": true, \"ThemeColor\": { \"ColorType\": \"string\", \"Tint\": 0 }, \"Type\": \"string\" }, \"BackgroundColor\": { \"Color\": { \"A\": 0, \"R\": 0, \"G\": 0, \"B\": 0 }, \"ColorIndex\": 0, \"IsShapeColor\": true, \"ThemeColor\": { \"ColorType\": \"string\", \"Tint\": 0 }, \"Type\": \"string\" } }, \"CustomFilters\": [ { \"FilterOperatorType\": \"string\" } ], \"DynamicFilter\": { \"DynamicFilterType\": \"string\" }, \"IconFilter\": { \"IconId\": 0, \"IconSetType\": \"string\" }, \"Top10Filter\": { \"Criteria\": \"string\", \"IsPercent\": true, \"IsTop\": true, \"Items\": 0 }, \"Visibledropdown\": \"string\" } ], \"Range\": \"string\", \"Sorter\": { \"CaseSensitive\": true, \"HasHeaders\": true, \"KeyList\": [ { \"Key\": 0, \"SortOrder\": \"string\", \"CustomList\": \"string\" } ], \"SortLeftToRight\": true } }, \"DisplayName\": \"string\", \"StartColumn\": 0, \"StartRow\": 0, \"EndColumn\": 0, \"EndRow\": 0, \"ListColumns\": [ { \"Name\": \"string\", \"TotalsCalculation\": \"string\" } ], \"ShowHeaderRow\": true, \"ShowTableStyleColumnStripes\": true, \"ShowTableStyleFirstColumn\": true, \"ShowTableStyleLastColumn\": true, \"ShowTableStyleRowStripes\": true, \"ShowTotals\": true, \"TableStyleName\": \"string\", \"TableStyleType\": \"string\"}" \
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
 
## 云 SDK 系列
 
使用 SDK 是加速开发的最佳方式。 SDK 负责处理底层细节，让您专注于项目任务。请查看[GitHub 仓库](https://github.com/aspose-cells-cloud)有关 Aspose.Cells Cloud SDK 的完整列表。
 
以下代码示例演示如何使用各种 SDK 调用 Aspose.Cells Web 服务：
 
 
 

{{< tabs tabTotal="4" tabID="4" tabName1="C#" tabName2="VB.NET" tabName3="Java" tabName4="Go" >}}

{{< tab tabNum="1" >}}

```java



```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java



```

{{< /tab >}}

{{< tab tabNum="3" >}}

```java



```

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "c76d8684f0bb9a96cb74f64433a43b88" >}}

{{< /tab >}}

{{< /tabs >}}
