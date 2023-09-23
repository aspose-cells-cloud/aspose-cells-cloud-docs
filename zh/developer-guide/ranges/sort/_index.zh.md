---
title: 范围排序
second_title: Aspose.Cells Cloud Documen
linktitle: 索尔
type: docs
keywords: Range Sort
url: /zh/ranges/sort/
description: 设置一系列单元格周围的轮廓边框。
weight: 20
---
这个REST API表示范围排序。

## RSET API


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



这[开放API规范](https://reference.aspose.cloud/cells/#/RangesController/PostWorksheetCellsRangeSort)定义了一个可公开访问的编程接口，并允许您直接从 Web 浏览器执行 REST 交互。

您可以使用cURL命令行工具轻松访问Aspose.Cells Web服务。以下示例展示如何使用 cURL 呼叫云端 API。

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

## 云SDK系列

使用 SDK 是加快开发速度的最佳方式。 SDK 负责处理底层细节，让您专注于项目任务。请查看 GitHub 存储库以获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例演示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

