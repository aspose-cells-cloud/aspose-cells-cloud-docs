---
title: 范围排序
second_title: Aspose.Cells Cloud Documen
linktitle: 索尔
type: docs
keywords: Range Sort
url: /zh/ranges/sort/
description: 设置单元格区域周围的轮廓边框。
weight: 20
kwords: Excel, Office 云, REST API, 电子表格, PDF, CSV, Json, Markdwon, 范围排序
---
此 REST API 表示范围排序。

## 重置 API


```bash

POST http://api.aspose.cloud/v3.0//cells/{name}/worksheets/{sheetName}/ranges/sort

```

请求参数为：

|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|姓名|细绳|小路|工作簿名称。|
|工作表名称|细绳|小路|工作表名称。|
|范围操作|班级|身体|范围排序请求|
|文件夹|细绳|询问|原始工作簿文件夹。|
|存储名称|细绳|询问|存储名称。|



这[OpenAPI 规范](https://reference.aspose.cloud/cells/#/RangesController/PostWorksheetCellsRangeSort)定义一个可公开访问的编程接口，并允许您直接从 Web 浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例显示如何使用 cURL 调用云 API。

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
{{< tab tabNum="1" >}}
```powershell
curl -v "http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/sort" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
```
{{< /tab >}}
{{< tab tabNum="2" >}}
```powershell

```
{{< /tab >}}

{{< /tabs >}}

## Cloud SDK 系列

使用 SDK 是加快开发速度的最佳方式。SDK 负责处理底层细节，让您专注于项目任务。请查看 GitHub 存储库以获取 Aspose.Cells 云 SDK 的完整列表。

以下代码示例演示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

