---
title: "Aspose.Cells Cloud Excel 文本搜索 Web API — 在远程工作表中查找文本"
second_title: "文档"
ArticleTitle: "在远程 Excel 电子表格工作表中搜索文本 — 查找特定数据"
linktype: "docs"
url: /zh/search-content-in-remote-worksheet/
keywords: "Aspose Cells, Excel API, 文本搜索, 远程工作表"
description: "使用 Aspose.Cells Cloud API 在远程 Excel 工作表中搜索文本、数字或公式。支持不区分大小写及密码保护的文件。"
weight: 100
---

## **在远程工作表中搜索内容**

使用 Aspose.Cells Cloud API 以编程方式在任意 Excel 工作表中搜索特定文本。该服务可在存储于云端的远程文件中定位文本、数字或公式，从而支持自动化数据发现、内容分析及电子表格审计工作流。

### **Web API**

```curl
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/search/content
```

### **安全与身份验证**

Aspose.Cells Cloud API 安全可靠，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

```bash
-H "Authorization: Bearer {access_token}"
```

### **请求参数**

| 参数名称       | 类型    | 路径/查询字符串/HTTP 正文 | 描述                                                                                       |
| -------------- | ------- | ------------------------- | ------------------------------------------------------------------------------------------ |
| name           | 字符串  | 路径                      | **必填。** 目标工作簿的文件名（例如 `annual_report.xlsx`）。                               |
| worksheet      | 字符串  | 路径                      | **必填。** 进行搜索的工作簿中的工作表。                                                    |
| searchText     | 字符串  | 查询字符串                | **必填。** 要查找的确切文本字符串或数字。                                                  |
| ignoreCase     | 布尔值  | 查询字符串                | **可选。** 当为 `true` 时，搜索不区分大小写。默认值为 `false`。                            |
| folder         | 字符串  | 查询字符串                | **可选。** 包含工作簿的文件夹路径。若省略，则使用根文件夹。                                |
| storageName    | 字符串  | 查询字符串                | **可选。** 自定义配置的云存储名称。若省略，则使用默认存储。                                |
| region         | 字符串  | 查询字符串                | **可选。** 区域设置（例如 `ja-JP`），可能影响文本比较。                                    |
| password       | 字符串  | 查询字符串                | **可选。** 受保护工作簿的密码。若文件未加密，请省略此项。                                  |

### **响应**

```json
{
  "textItems": [
    {
      "cellName": "A1",
      "text": "合计",
      "occurrences": 1
    },
    {
      "cellName": "B5",
      "text": "合计",
      "occurrences": 2
    }
  ],
  "code": 200,
  "status": "OK"
}
```

- **textItems** — 匹配项数组。每项包含单元格地址（`cellName`）、匹配字符串（`text`）及该单元格中出现的次数（`occurrences`）。
- **code** — 服务返回的 HTTP 状态码。
- **status** — 结果的文本描述。

### **错误代码**

- **400 Bad Request（错误请求）** — API URI 无效或参数格式错误。
- **401 Unauthorized（未授权）** — 缺少或 OAuth 2.0 令牌无效。
- **404 Not Found（未找到）** — 无法定位工作簿或工作表。
- **500 Server Error（服务器错误）** — 处理请求时发生意外情况。

## 应在何处使用电子表格 API 的工作表内搜索内容功能？

- **工作簿合规性审计：** 快速在整个文件中定位敏感词（例如“机密”）。
- **跨工作表数据关联：** 查找在多张工作表中出现的项目编号或客户名称。
- **模板验证：** 生成报告后，确认占位符（例如 `{{Date}}`）已被替换。
- **历史数据挖掘：** 在旧版电子表格中搜索特定事件代码，以理解过往业务逻辑。

## 为何应使用电子表格 API 的工作表内搜索内容功能？

- **开发者友好：** 提供多种语言的 SDK，加速开发进程，并配有完整文档。
- **降低人工成本：** 减少人工数据整合所需的人力投入。
- **按需付费：** 仅对实际调用的 API 请求计费。
- **零维护负担：** 无需管理服务器、无需软件更新、无需担心兼容性问题。
- **保留复杂 Excel 格式：** 在导出结果为 PDF 或其他格式时保留复杂格式。

## 如何使用电子表格 API 的工作表内搜索功能（结合 SDK）

### OpenAPI 规范

[OpenAPI 规范](https://reference.aspose.cloud/cells/#/SearchControllor/SearchContentInRemoteWorksheet)定义了一个公开可访问的编程接口，可直接通过 Web 浏览器发起 REST 请求。

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加速开发的最佳方式。SDK 处理底层细节，使您仅需少量代码即可实现电子表格工作表中的内容搜索。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。