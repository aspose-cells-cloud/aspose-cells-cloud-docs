---
title: "Aspose.Cells Cloud 替换 Web API — 更新远程工作表中的文本"
second_title: "文档"
articleTitle: "使用 Aspose.Cells Cloud API 在远程工作表中查找并替换文本"
linktype: "replace-content-in-remote-worksheet"
type: docs
url: /zh/replace-content-in-remote-worksheet/
keywords: "Aspose.Cells, 替换文本, 远程工作表, Excel API, 云电子表格, 查找并替换, REST API"
description: "替换存储在 Aspose Cloud 中的 Excel 文件特定工作表中的文本。支持密码保护的工作簿、区域感知搜索以及批量更新。"
weight: 100
---

替换远程 Excel 文件中特定工作表内的指定文本。使用 Aspose.Cells 查找与替换 API 高效更新目标电子表格工作表的内容，实现精准编辑。

## **远程工作表内容替换 API**

### **Web API**

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/replace/content
```

### **安全性与身份验证**

Aspose.Cells Cloud API 安全可靠，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

```bash
-H "Authorization: Bearer {access_token}"
```

### **请求参数**

| 参数名称     | 类型   | 路径 / 查询字符串 / HTTP 请求体 | 描述                                                                                                                                                     |
| :----------- | :----- | :----------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name         | 字符串 | 路径                           | 存储在云存储中、待修改的工作簿文件名（例如 `"sales_report.xlsx"`、`"budget_2024.xls"`）。                                                               |
| worksheet    | 字符串 | 路径                           | 将执行查找与替换操作的特定工作表名称（例如 `"Q1_Sales"`、`"Sheet1"`）。                                                                                  |
| searchText   | 字符串 | 查询字符串                     | 在指定工作表中搜索的文本字符串。除非进一步限定，否则搜索将应用于工作表中的所有单元格。                                                                  |
| replaceText  | 字符串 | 查询字符串                     | 将替换工作表中所有匹配 `searchText` 的文本字符串。                                                                                                       |
| folder       | 字符串 | 查询字符串                     | 源工作簿所在的云存储文件夹路径（例如 `"/reports/monthly/"`、`"/finance/"`）。                                                                            |
| storageName  | 字符串 | 查询字符串                     | _（可选）_ 自定义云存储的名称（例如 `"CorporateS3"`、`"AzureArchive"`）。若省略，则使用账户默认的云存储。                                                 |
| region       | 字符串 | 查询字符串                     | _（可选）_ 设置文本处理的区域设置，可能影响字符编码及工作表内与语言相关的搜索行为（例如 `"zh-CN"`、`"en-GB"`）。                                         |
| password     | 字符串 | 查询字符串                     | _（可选）_ 若工作簿受密码保护，请提供密码以打开并修改文件。                                                                                             |

**示例请求（cURL）**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/sales_report.xlsx/worksheets/Sheet1/replace/content?searchText=OldValue&replaceText=NewValue&folder=/reports" \
     -H "Authorization: Bearer {access_token}"
```

### **响应**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### **错误代码**

| 代码 | 描述               | 出现时机                                               |
|------|--------------------|--------------------------------------------------------|
| 400  | 错误请求           | 请求 URI 格式错误或缺少必需参数。                     |
| 401  | 未授权             | 缺失、无效的访问令牌，或客户端凭证错误。             |
| 404  | 未找到             | 无法找到指定的工作簿或工作表。                        |
| 500  | 内部服务器错误     | 处理请求时发生意外错误。                              |

## 应在何处使用远程电子表格中工作表内容替换 API？

- **批量云文件更新**：修改存储在 AWS S3、Azure Blob 等云存储中的多个 Excel 文件内容。
- **动态填充云模板**：批量为存储在云端的报表模板填充动态数据。
- **跨区域文件同步**：实现不同地理区域中云存储 Excel 文件内容的一致性同步。

## 为何应使用远程电子表格中工作表内容替换 API？

- **开发者友好**：Aspose.Cells Cloud 提供多种语言的 SDK 库，便于快速开发，并配有详尽文档。相比自行构建图表渲染解决方案，可大幅降低开发工作量。
- **降低人工成本**：减少专职文档整合人员的需求。
- **按需付费**：无需前期投入，仅对实际调用的 API 接口计费。
- **零维护成本**：无需维护服务器、更新软件或处理兼容性问题。

## 如何使用 SDK 调用远程电子表格中工作表内容替换 API

### **OpenAPI 规范**

[OpenAPI 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/ReplaceContentInRemoteRange) 定义了公开可访问的编程接口，允许您直接从 Web 浏览器发起 REST 请求。

### **使用 Aspose.Cells Cloud SDK**

使用 SDK 是加速开发的最佳方式。SDK 处理底层细节，使您仅需少量代码即可实现电子表格工作表内容替换功能。  
请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 与 Aspose.Cells Web 服务进行交互：