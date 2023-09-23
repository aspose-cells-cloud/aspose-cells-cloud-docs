---
title: 列表对象插入切片器
description: 为列表对象插入切片器。
url: /zh/list-objects/insert-slicer/
weight: 20
---
此 REST API 表示在 Excel 工作表上插入列表对象的切片器。

## RSET API

```bash

POST http://api.aspose.cloud/v3.0//cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/InsertSlicer

```

请求参数为：

|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|姓名|细绳|小路||
|工作表名称|细绳|小路||
|列表对象索引|整数|小路||
|列索引|整数|询问||
|目标单元名称|细绳|询问||
|文件夹|细绳|询问||
|存储名称|细绳|询问||



这[开放API规范](https://reference.aspose.cloud/cells/#/ListObjectsController/PostWorksheetListObjectInsertSlicer)定义了一个可公开访问的编程接口，并允许您直接从 Web 浏览器执行 REST 交互。

您可以使用cURL命令行工具轻松访问Aspose.Cells Web服务。以下示例展示如何使用 cURL 呼叫云端 API。

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
{{< tab tabNum="1" >}}
```powershell
curl -v "http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/InsertSlicer" \
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
