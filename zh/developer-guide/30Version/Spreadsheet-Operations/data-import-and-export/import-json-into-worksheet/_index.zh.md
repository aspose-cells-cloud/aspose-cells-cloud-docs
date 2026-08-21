---
title: "将 JSON 数据导入 Excel"
second_title: "文档"
linktitle: "导入 JSON"
type: docs
url: /import-json-data-into-excel/
aliases: [/import/json/]
keywords: "Aspose.Cells Cloud, JSON 导入, Excel API, REST 导入 JSON, SDK 示例"
description: "了解如何使用 Aspose.Cells Cloud REST API 将 JSON 数据导入 Excel 工作表。包含端点详情、请求/响应示例以及适用于 .NET、Java 和 Python 的 SDK 代码。"
weight: 40
---

此 REST API **将 JSON 数据导入 Excel 工作表**。

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/importjson
```
### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

### **请求参数**

| 参数名称              | 位置         | 类型   | 描述                                                                                     |
| --------------------- | ------------ | ------ | ---------------------------------------------------------------------------------------- |
| name                  | 路径参数     | 字符串 | 工作簿文件的名称。                                                                       |
| importJsonRequest     | HTTP 请求体  | 类对象 | 包含 JSON 导入详细信息的请求负载。                                                       |
| password              | 查询字符串   | 字符串 | 打开受保护工作簿所需的密码。                                                             |
| folder                | 查询字符串   | 字符串 | 存放原始工作簿的文件夹。                                                                 |
| storageName           | 查询字符串   | 字符串 | 工作簿所在的存储空间名称。                                                               |
| outPath               | 查询字符串   | 字符串 | 导入完成后输出文件的路径。若省略，则更新后的工作簿将作为响应体返回。                     |
| outStorageName        | 查询字符串   | 字符串 | 输出文件所在的存储空间名称。                                                             |
| checkExcelRestriction | 查询字符串   | 字符串 | 标志位，指示是否强制执行 Excel 特定限制（true/false）。                                |

### **请求体示例**

```json
{
  "JsonFileSource": {
    "FilePath": "string"
  },
  "ImportPosition": {
    "SheetName": "string",
    "RowIndex": 0,
    "ColumnIndex": 0
  },
  "JsonContent": "string"
}
```

### 响应

成功请求将返回 **HTTP 200** 状态码，响应体类似如下 JSON：

```json
{
  "Code": 200,
  "Status": "OK"
}
```

可能的状态码说明：

| 状态码 | 含义                       |
| ------ | -------------------------- |
| 200    | 导入成功                   |
| 400    | 请求错误 — 缺少或数据无效  |
| 401    | 未授权 — 令牌无效或缺失    |
| 500    | 服务器内部错误             |


## 如何使用 SDK 调用 PostWorkbookImportJson API

### PostWorkbookImportJson API 规范

[OpenAPI 规范](https://reference.aspose.cloud/cells/#/DataProcessing/PostWorkbookImportJson) 定义了一个公开可访问的编程接口，允许您直接通过网页浏览器发起 REST 请求。

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加速开发的最高效方式。SDK 封装了底层细节，使您能专注于业务逻辑。有关 Aspose.Cells Cloud SDK 的完整列表，请访问 [GitHub 仓库](https://github.com/aspose-cells-cloud)。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：