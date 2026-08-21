---
title: "Aspose.Cells Cloud 替换 Web API — 更新远程电子表格中的文本"
second_title: "文档"
ArticleTitle: "批量替换云 Excel 文件中的文本 — 查找与替换 API"
linktitle: "替换远程电子表格内容"
type: docs
url: /replace-content-in-remote-spreadsheet/
keywords: "Aspose.Cells Cloud、替换内容、远程电子表格、查找与替换 API、云 Excel、批量文本替换"
description: "使用 Aspose.Cells Cloud 查找与替换 API 批量更新远程 Excel 工作簿中的文本。安全的 HTTPS 端点、OAuth2 身份验证，以及即用型 SDK 示例，便于快速集成。"
weight: 100
---

在云端存储的远程 Excel 文件中执行批量文本替换。使用 Aspose.Cells 云电子表格查找与替换 API 高效定位并更新特定文本字符串。


## **远程电子表格内容替换 API**

### **Web API**

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/replace/content
```

### **安全性与身份验证**

Aspose.Cells Cloud API 具备高安全性，需要<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

```bash
-H "Authorization: Bearer {access_token}"
```

### 请求参数

| 参数名称        | 类型   | 位置   | 描述                                                                                                                                                 |
| --------------- | ------ | ------ | ---------------------------------------------------------------------------------------------------------------------------------------------------- |
| **name**        | 字符串 | 路径   | 待修改、存储于云存储中的工作簿文件名称（例如 `"report.xlsx"`）。                                                                                     |
| **searchText**  | 字符串 | 查询   | 需在整个工作簿中查找的字符串。搜索区分大小写，除非受其他参数限制，否则将应用于所有工作表。                                                           |
| **replaceText** | 字符串 | 查询   | 将用于替换所有 `searchText` 出现位置的字符串。                                                                                                      |
| **folder**      | 字符串 | 查询   | 存放源工作簿的云存储文件夹路径（例如 `"/documents/quarterly/"`）。                                                                                  |
| **storageName** | 字符串 | 查询   | _（可选）_ 自定义云存储的名称（例如 `"MyS3Bucket"`）。若未指定，则使用账户默认配置的存储。                                                          |
| **region**      | 字符串 | 查询   | _（可选）_ 区域标识符，可能影响字符编码及语言相关的搜索行为（例如 `"en-US"`）。                                                                     |
| **password**    | 字符串 | 查询   | _（可选）_ 打开受保护工作簿所需的密码。                                                                                                             |

### 响应

成功响应通常返回操作状态及已完成的替换数量：

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### 错误代码

- **400 Bad Request（错误请求）** — 无效的 Aspose.Cells Cloud API URI。
- **401 Unauthorized（未授权）** — 缺失或无效的 OAuth 2.0 访问令牌。
- **404 Not Found（未找到）** — 无法访问指定的电子表格文件。
- **500 Server Error（服务器错误）** — 处理请求时发生意外的服务器端问题。

## 何时应使用远程电子表格内容替换 API？

- **批量云文件更新** — 修改存储于云存储（如 AWS S3 或 Azure Blob）中的多个 Excel 文件内容。
- **动态填充云模板** — 使用最新数据填充存储于云端的报表模板。
- **跨区域文件同步** — 确保不同地理区域的云存储中 Excel 文件内容保持一致。

## 为何选择远程电子表格内容替换 API？

- **开发者友好** — Aspose.Cells Cloud 提供多种编程语言的 SDK 库，相比自行构建定制解决方案，可显著降低开发工作量。
- **降低人工成本** — 无需专人手动整合文档。
- **按使用量付费** — 无需前期投入，仅需为实际调用的 API 请求付费。
- **零维护成本** — 无需管理服务器、无需软件更新、无兼容性顾虑。
- **保留所有单元格格式、公式及图表** — 文本替换后，操作将保留原始工作簿的布局与计算逻辑。

## 如何使用 SDK 调用远程电子表格内容替换 API

### OpenAPI 规范

[OpenAPI 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/ReplaceContentInRemoteRange)定义了公开可访问的编程接口，可让您直接通过网页浏览器执行 REST 交互。

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加速开发的最佳方式。SDK 封装了底层细节，使您能以最少代码实现电子表格中的内容替换功能。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何通过多种 SDK 调用 Aspose.Cells Web 服务：


---