---
title: "Aspose.Cells Cloud – 将表格转换为 HTML"
description: "借助 Aspose.Cells Cloud API 快速将 Excel 表格转换为 HTML 格式 — 安全可靠、保留格式、易于集成。"
keywords: "Aspose.Cells, Excel 转 HTML, 表格转 HTML, 云 API, 电子表格转换"
weight: 100
date: 2026-07-30
last_updated: 2026-07-30
version: "v4.0"
url: /convert-table-to-html/
type: docs
---

**快速概览**：此端点读取本地 Excel 工作簿，提取指定的**表格**，将其转换为**HTML**文件，并以可下载流的形式返回结果。无需先上传至 Aspose Cloud 存储空间。

## ConvertTableToHTML API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/html
```

### **安全性与身份验证**

Aspose.Cells Cloud API 采用安全机制，需要 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数

| 参数名             | 位置      | 类型       | 是否必需 | 描述                                                                 |
| ------------------ | --------- | ---------- | -------- | -------------------------------------------------------------------- |
| **Spreadsheet**    | Form‑Data | `File`     | **是**   | 包含待转换表格的 Excel 工作簿文件。                                 |
| **worksheet**      | Query     | `String`   | **是**   | 存放该表格的工作表名称。                                             |
| **tableName**      | Query     | `String`   | **是**   | 待转换表格的确切名称。                                               |
| **outPath**        | Query     | `String`   | 否       | Aspose Cloud 存储中用于保存 HTML 文件的文件夹路径（可选）。          |
| **outStorageName** | Query     | `String`   | 否       | 输出文件的存储名称（可选）。                                         |
| **fontsLocation**  | Query     | `String`   | 否       | 包含转换所需自定义字体的文件夹路径。                                 |
| **region**         | Query     | `String`   | 否       | 区域标识符（例如 `zh-CN`、`en-US`、`fr-FR`），影响数字/日期格式化。 |
| **password**       | Query     | `String`   | 否       | 打开受保护工作簿所需的密码。                                         |
| **AutoRowsFit**    | Query     | `Boolean`  | 否       | 是否自动调整工作表中所有行高（`true`/`false`）。                    |
| **AutoColumnsFit** | Query     | `Boolean`  | 否       | 是否自动调整工作表中所有列宽（`true`/`false`）。                    |

### **响应**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**HTTP 状态码**

| 状态码 | 含义             | 描述                                           |
| ------ | ---------------- | ---------------------------------------------- |
| 200    | OK（成功）       | 操作成功执行；响应包含操作详情。              |
| 400    | Bad Request（请求错误） | 缺失或无效的参数（例如不支持的文件类型）。    |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                          |
| 413    | Payload Too Large（载荷过大） | 上传的文件超过大小限制。                     |
| 500    | Internal Server Error（内部服务器错误） | 服务器发生意外错误。                       |

## 何时使用“将表格转换为 HTML”API？

- **动态网页内容**：将价格表、排期表或产品列表直接嵌入网页或内容管理系统（CMS）中。
- **邮件模板**：生成可在各类邮件客户端中一致渲染的 HTML 片段，适用于订单摘要或报表。
- **仪表板与报告工具**：展示实时电子表格数据，无需加载完整工作簿或使用重量级表格组件。
- **文档预览**：提供电子表格特定部分的快速预览，同时保留原始格式。

## 如何通过 SDK 使用“将表格转换为 HTML”API？

### Convert Table to HTML API 规范

[Convert Table to HTML API 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToHTML) 提供公开可访问的编程接口，允许直接通过 Web 浏览器发起 REST 请求。

您可使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/html?worksheet=Sheet1&tableName=Table1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.html
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 编码)",
  "contentType": "MIME 类型",
  "fileDownloadName": "可选文件名"
}
```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是最快捷的开发方式，它抽象了底层细节，使您只需少量代码即可完成电子表格表格数据到 CSV 文件的转换。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：