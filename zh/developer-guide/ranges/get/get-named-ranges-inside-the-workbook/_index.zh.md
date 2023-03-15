---
title: 在 Excel workboo 上获取命名范围
second_title: Aspose.Cells Cloud Documen
linktitle: 南
type: docs
url: /zh/ranges/get/name/
aliases: [/get-named-ranges-inside-the-workbook/]
keywords: Get cells data based on named range on an Excel worksheet
description: Aspose.Cells Cloud REST API 支持根据 Excel 工作表上的命名范围获取单元格数据。 SDK支持多种开发语言。它们包括 Android、C#、Go、Java、NodeJS、Perl、PHP、Python、Ruby 和 swift
weight: 10
---
此 REST API 表示读取工作表范围信息。
 
## RSET API
 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/ranges
 
```
请求参数为：
 
|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|姓名|细绳|小路|文档名称。|
|文件夹|细绳|询问|文档文件夹。|
|存储名称|细绳|询问|存储名称。|
 
这[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Worksheets/GetNamedRanges)定义了一个可公开访问的编程接口，并允许您直接从 Web 浏览器执行 REST 交互。
 
您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例显示如何使用 cURL 调用 Cloud API。
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/ranges" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}}
 
{{< tab tabNum="2" >}}
 
```bash
{

  "Ranges": {

    "RangeList": [

      {

        "ColumnCount": 7,

        "ColumnWidth": 8.428571428571429,

        "FirstColumn": 1,

        "FirstRow": 9,

        "Name": "data",

        "RefersTo": "=Sheet1!$B$10:$H$10",

        "RowCount": 1,

        "RowHeight": 15,

        "Worksheet": "Sheet1"

      }

    ]

  },

  "Code": 200,

  "Status": "OK"

}
 
```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## 云 SDK 系列
 
使用 SDK 是加速开发的最佳方式。 SDK 负责处理底层细节，让您专注于项目任务。请查看[GitHub 仓库](https://github.com/aspose-cells-cloud)有关 Aspose.Cells Cloud SDK 的完整列表。
 
以下代码示例演示如何使用各种 SDK 调用 Aspose.Cells Web 服务：
 
 
{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="Ruby" tabName3="Go" >}}

{{< tab tabNum="1" >}}



{{< /tab >}}

{{< tab tabNum="2" >}}



{{< /tab >}}

{{< tab tabNum="3" >}}



{{< gist "aspose-cells-cloud-gists" "c75da9aa06645e27e899a9fb6cdc134c" >}}

{{< /tab >}}

{{< /tabs >}}
