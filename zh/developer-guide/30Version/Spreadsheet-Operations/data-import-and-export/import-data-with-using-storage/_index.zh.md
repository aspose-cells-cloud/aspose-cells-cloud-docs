---
title: "使用存储导入数据"
second_title: "文档"
linktype: "使用存储导入数据"
type: docs
url: /zh/import-data-with-using-storage/
aliases:
  - /import-data-into-excel-worksheet/
  - /import-data-into-worksheet/
  - /import-data-in-excel-worksheet/
  - /import-data/
  - /import/with-using-storage/
description: "使用存储导入数据：通过 Aspose.Cells Cloud API 从各种存储源将数据导入 Excel 工作表。支持通过 HTTPS 导入 JSON、CSV 及其他格式。"
keywords: "Aspose.Cells Cloud、Excel、导入数据、REST API、云存储、JSON、CSV、PDF、Markdown、HTTPS"
weight: 10
ArticleTitle: "使用存储导入数据 - Aspose.Cells Cloud API 文档"
---

此 REST API 用于将数据导入 Excel 文件。

## PostImportData API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

### **安全性与身份验证**

Aspose.Cells Cloud API 采用安全机制，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

### 请求参数说明

| 参数名称      | 类型   | 位置   | 描述                                             |
| ------------- | ------ | ------ | ------------------------------------------------ |
| name          | string | path   | Excel 文件的名称。                               |
| folder        | string | query  | 文件所在存储中的文件夹路径。                     |
| storageName   | string | query  | 存储服务的名称。                                 |
| importData    | object | body   | 包含待导入数据的 JSON 对象。                     |

**导入数据选项参数**请参阅[参考链接](/cells/import/#import-data-option-parameter)。

**前提条件**：您必须在 `Authorization` 请求头中提供有效的 JWT 令牌，并确保目标工作簿已存在于指定的存储位置。

### 响应示例

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP 状态码说明**

| 状态码 | 含义               | 描述                                             |
|--------|--------------------|--------------------------------------------------|
| 200    | OK（成功）         | 筛选器应用成功；响应包含操作详细信息。           |
| 400    | Bad Request（请求错误） | 参数缺失或无效（例如不支持的文件类型）。         |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                             |
| 413    | Payload Too Large（载荷过大） | 上传的文件超出大小限制。                         |
| 500    | Internal Server Error（内部服务器错误） | 服务器发生意外错误。                             |

## 如何结合 SDK 使用 PostImportData API

### PostImportData API 规范

<a href="https://apireference.aspose.cloud/cells/#/Workbook/PostImportData" rel="noopener noreferrer">OpenAPI 规范</a> 定义了一个公开可访问的编程接口，让您可直接通过网页浏览器发起 REST 调用。

您可使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用云 API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/importdata" \
     -X POST \
     -d '{"Data":[1,2,4],"DestinationWorksheet":"Sheet1","FirstRow":1,"FirstColumn":2,"IsVertical":true,"IsInsert":true,"importDataType":"IntArray"}' \
     -H "Content-Type: application/json" \
     -H "Accept: application/json" \
     -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加快开发进度的最佳方式。SDK 封装了底层细节，使您能专注于业务逻辑。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用 PHP SDK 调用 Aspose.Cells Web 服务：
---