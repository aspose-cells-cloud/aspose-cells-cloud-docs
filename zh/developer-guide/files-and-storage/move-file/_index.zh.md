---
title: 移动文件
second_title: Documen
linktitle: 移动文件
type: docs
url: /zh/move-file/
keywords: Move file, Aspose.Cells API, File Management, Excel API, REST API, Cloud Storage, Spreadsheet Manipulatio
description: 了解如何使用 MoveFile API 管理 Aspose.Cells 云存储中的文件
weight: 100
kwords: Excel, Office 云, REST API, 电子表格, PDF, CSV, Json, Markdown, 移动文件, 文件管理, 云存储
---
## **Excel API：移动文件**

```
PUT http://api.aspose.cloud/v4.0/cells/storage/file/move/{srcPath}
```

### **功能描述**

这**移动文件**API 允许您在 Aspose.Cells 云存储中将文件从一个位置移动到另一个位置。这对于有效地组织文件和管理存储尤其有用。

### 请求参数**移动文件**API 是

|参数名称|类型|路径/查询字符串/HTTP 正文|描述|
|---------------|--|------------------------|--------------------------------------|
|源路径|细绳|小路|要移动的文件的源路径。|
|目标路径|细绳|询问|文件将被移动到的目标路径。|
|源存储名称|细绳|询问|源存储名称（如果适用）。|
|目标存储名称|细绳|询问|目标存储名称（如果适用）。|
|版本号|细绳|询问|文件的版本 ID（如果适用）。|

### **响应描述**

```json
{
Void
}
```

## OpenAPI 规范

这[OpenAPI 规范](https://reference.aspose.cloud/cells/#/FileController/MoveFile)定义一个可公开访问的编程接口，并允许您直接从 Web 浏览器执行 REST 交互。

## Excel API SDK

使用 SDK 是加速开发的最佳方式。SDK 负责处理底层细节，让您专注于项目任务。请查看[GitHub 存储库](https://github.com/aspose-cells-cloud)以获取 Aspose.Cells Cloud SDKs 的完整列表。

以下代码示例演示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：
