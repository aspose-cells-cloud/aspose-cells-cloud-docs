---
title: "从 Excel 中移除字符 — Aspose.Cells Cloud API（POST /cells/removecharacters）"
second_title: "文档"
linktitle: "移除字符"
type: docs
url: /excel-remove-characters/
keywords: "移除字符, Aspose.Cells, Excel API, 文本处理, 云服务"
description: "了解如何使用 Aspose.Cells Cloud API 从 Excel 工作表中移除字符、字符集或子字符串。包含请求结构、cURL 示例、SDK 代码及错误处理说明。"
weight: 100
ArticleTitle: "从 Excel 中移除字符 — Aspose.Cells Cloud API（POST /cells/removecharacters）"
---

## 通过 Web API 从 Excel 中移除字符

一套用于清理所选单元格中文本内容的完整工具集。该 API 可移除指定字符、预定义字符集或子字符串，确保工作表中的文本标准化且不含无关符号。

**前置条件**

- 一个已激活的 Aspose Cloud 账户。  
- 一个根据身份验证指南获取的有效 JWT 访问令牌。  
- 在调用此接口前，Excel 文件必须已上传至存储空间。  
- 支持的文件格式包括 `.xlsx`、 `.xls`、 `.xlsm` 及其他常见 Excel 类型。

```http
POST https://api.aspose.cloud/v3.0/cells/removecharacters
```

### **安全与身份验证**

Aspose.Cells Cloud API 安全可靠，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 功能说明

- **移除自定义字符** – 指定您希望删除的任意字符。在 _移除自定义字符_ 字段中输入每个目标字符，API 将删除所选单元格中所有这些字符的出现实例。  
- **移除字符集** – 可从预定义字符集中进行选择：  
  - **不可见字符** – 删除换行符及前 32 个不可见 ASCII 字符（0–31），以及额外码位（127、129、141、143、144、157）。  
  - **文本字符** – 删除所有字母。  
  - **数字字符** – 删除所有数字。  
  - **符号** – 删除数学、几何、技术、货币符号以及字母类符号，如 “?”, “1”, “™” 等。  
  - **标点符号** – 删除所有标点符号。  
- **移除子字符串** – 删除所选单元格中指定的任意子字符串（例如一个单词）。

### 请求参数

| 参数名称                | 类型  | 位置 | 描述                                                           |
| ----------------------- | ----- | ---- | -------------------------------------------------------------- |
| removeCharactersOptions | 类    | Body | 定义需移除的字符、字符集或子字符串的选项配置对象。             |

**`removeCharactersOptions` 结构体字段说明**

| 属性             | 类型    | 必填 | 描述                                                                                 |
| ---------------- | ------- | ---- | ------------------------------------------------------------------------------------ |
| Range            | string  | 是   | 采用 A‑1 表示法或命名区域的方式指定待处理单元格范围（例如 `"A1:C10"`）。               |
| CustomCharacters | string  | 否   | 包含待删除自定义字符的字符串（例如 `"@#$"`）。                                        |
| CharacterSet     | string  | 否   | 枚举值，指定预定义字符集类型（`"NonPrinting"`、`"Text"`、`"Numeric"`、`"Symbols"`、`"Punctuation"`）。 |
| Substring        | string  | 否   | 待移除的精确子字符串（例如 `"USD"`）。                                                |
| IgnoreCase       | boolean | 否   | 当值为 `true` 时，字符移除操作不区分大小写。                                          |

**示例 JSON 请求体**

```json
{
  "Range": "A1:B20",
  "CustomCharacters": "@#$",
  "CharacterSet": "NonPrinting",
  "Substring": "USD",
  "IgnoreCase": true
}
```

**示例 cURL 请求**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/removecharacters" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d '{
           "Range": "A1:B20",
           "CustomCharacters": "@#$",
           "CharacterSet": "NonPrinting",
           "Substring": "USD",
           "IgnoreCase": true
         }'
```

### **响应**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[合并后的文件名]",
    "Filesize" : [文件大小],
    "FileContent" : "[Base64字符串]"
}
```

**HTTP 状态码说明**

| 状态码 | 含义            | 描述                                       |
|------|-----------------|--------------------------------------------|
| 200  | OK（成功）       | 成功应用过滤；响应包含操作详情。               |
| 400  | Bad Request（错误请求） | 参数缺失或无效（如文件类型不支持）。             |
| 401  | Unauthorized（未授权） | JWT 令牌无效或缺失。                            |
| 413  | Payload Too Large（请求实体过大） | 上传文件大小超出限制。                         |
| 500  | Internal Server Error（服务器内部错误） | 发生意外服务器错误。                         |

## 如何使用 SDK 调用 PostRemoveCharacters API

### PostRemoveCharacters API 规范

完整的 <a href="https://reference.aspose.cloud/cells/#/TextProcessingController/PostRemoveCharacters" rel="noopener noreferrer">PostRemoveCharacters 接口 OpenAPI 规范</a> 定义了一个公开可用的编程接口，可让您直接通过 Web 浏览器发起 REST 请求。

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加速开发进程的最佳方式。SDK 会自动处理底层细节，使您能专注于项目核心任务。请查阅 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 仓库</a> 获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：
---