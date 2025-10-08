---
title: 删除文件 - Excel AP
second_title: Documen
linktitle: 删除文件
type: docs
url: /zh/delete-file/
keywords: Delete file, Excel API, REST API, Office Cloud, Spreadsheet management, File deletion, Cloud storage, API usag
description: 了解如何使用 Aspose.Cells API 删除 Excel 中的文件。本指南提供有关 deleteFile API 端点、请求参数和响应结构的详细信息
weight: 100
kwords: 删除文件、Excel API、REST API、Office 云、电子表格管理、文件删除、云存储、API 使用
---
## **Excel API : 删除文件**

```
DELETE http://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

### **功能描述**

这**删除文件**API 允许用户从云存储中删除指定的文件，确保资源和数据的有效管理。

### 请求参数**删除文件**API 是

|参数名称|类型|路径/查询字符串/HTTP 正文|描述|
|:- |:- |:- |:- |
|小路|细绳|小路|需要删除的文件的路径。|
|存储名称|细绳|询问|文件所在存储的名称。如果使用默认存储，则为可选。|
|版本号|细绳|询问|要删除的文件的版本 ID（如果适用）。|

### **响应描述**

```json
{
Void
}
```

## OpenAPI 规范

这[OpenAPI 规范](https://reference.aspose.cloud/cells/#/FileController/DeleteFile)定义一个可公开访问的编程接口，并允许您直接从 Web 浏览器执行 REST 交互。

## Excel API SDK

使用 SDK 是加速开发的最佳方式。SDK 负责管理底层细节，让您专注于项目任务。请查看[GitHub 存储库](https://github.com/aspose-cells-cloud)以获取 Aspose.Cells Cloud SDKs 的完整列表。

以下代码示例演示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：
