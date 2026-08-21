---
title: "移除远程电子表格中的重复子字符串"
ArticleTitle: "移除远程电子表格中的重复子字符串 – Aspose.Cells Cloud API"
second_title: "文档"
linktitle: "移除远程电子表格中的重复子字符串"
type: docs
url: /zh/cells/{name}/worksheets/{worksheet}/range/{range}/content/remove/duplicate-substrings
aliases: []
keywords: "Aspose.Cells, 移除重复子字符串, API"
description: "用于在工作簿指定范围内的单元格中查找并移除重复子字符串的 API。"
weight: 1
---

## Aspose.Cells Cloud Web 服务的“移除远程电子表格中的重复子字符串”功能

该功能可在选定范围内的每个单元格中查找并移除重复的子字符串，支持用户自定义或预设分隔符，同时保留公式、格式和数据验证规则。

**重复项检测机制**  
1. 每个单元格的值将根据所选分隔符拆分为子字符串。  
2. 工具会比较**同一单元格内**的子字符串，并仅保留每个重复项的**首次出现**。  
3. 清理后的子字符串将使用相同的分隔符重新拼接，并写回原单元格。  

**分隔符选项**  
- 预设列表：逗号、分号、空格、制表符、换行符  
- `自定义`（Custom）——输入任意字符；多个字符被视为单一复合分隔符  
- `TreatConsecutiveDelimitersAsOne`（将连续分隔符视为一个）——将相邻分隔符合并为单一分隔符  

仅处理字符串类型单元格；数字、布尔值和公式在拆分前会先转换为字符串（公式会被丢弃）。返回已清理单元格的数量及更新后的工作簿流。

### Web API 端点

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/range/{range}/content/remove/duplicate-substrings
```

### **安全与身份验证**

Aspose.Cells Cloud API 安全可靠，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称 | 类型 | 路径/查询字符串/HTTP 请求体 | 描述 |
|----------|------|-----------------------------|------|
| name | string | 路径 | （必填）需检索的工作簿文件名称。 |
| worksheet | string | 路径 | 指定电子表格中的工作表。 |
| range | string | 路径 | 指定电子表格中的工作表区域。 |
| delimiters | string | 查询字符串 | 用于拆分单元格值的分隔符（例如逗号、分号、空格、制表符、换行符）。必填项。 |
| treatConsecutiveDelimitersAsOne | boolean | 查询字符串 | 将相邻分隔符合并为单一分隔符。默认值：true。可选。 |
| caseSensitive | boolean | 查询字符串 | 在检测重复项时执行区分大小写的比较。可选。 |
| folder | string | 查询字符串 | （可选）工作簿所在文件夹路径。默认值：null。 |
| storageName | string | 查询字符串 | （可选）若使用自定义云存储，则指定存储名称。 |
| region | string | 查询字符串 | 电子表格区域/语言设置（例如 `zh-CN`、`en-US`）。可选。 |
| password | string | 查询字符串 | 打开电子表格文件所需的密码。可选。 |

### 请求体参数

| 参数名称 | 类型 | 描述 |
| -------------- | ---- | ----------- |
| - | - | 此操作无需请求体。 |

### **响应**

```json
{
  "code": 200,
  "status": "OK",
  "cellsCount": 123,
  "file": "base64编码的工作簿流"
}
```

**响应状态码**

| 状态码 | 含义 | 描述 |
|--------|------|------|
| 200 | OK（成功） | 操作成功；返回已清理单元格数量及更新后的工作簿流。 |
| 400 | Bad Request（错误请求） | 请求参数缺失或无效。 |
| 401 | Unauthorized（未授权） | 身份验证失败，或 JWT 令牌缺失/无效。 |
| 413 | Payload Too Large（请求体过大） | 请求超出允许的大小限制。 |
| 500 | Internal Server Error（服务器内部错误） | 服务器发生意外错误。 |

## 如何使用 SDK 调用“移除远程电子表格中的重复子字符串”功能

### “移除远程电子表格中的重复子字符串” API 规范

[“移除远程电子表格中的重复子字符串”API 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/RemoveDuplicateSubstringsInRemoteSpreadsheet) 定义了公开可用的编程接口，允许您直接通过 Web 浏览器执行 REST 交互。

您可使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}
{< tab tabNum="1" >}
```bash
# 使用 HTTPS 以建立安全连接
curl -v "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/range/A1:C10/content/remove/duplicate-substrings?delimiters=comma%2Csemicolon&treatConsecutiveDelimitersAsOne=true&caseSensitive=false" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```
{< /tab >}
{< tab tabNum="2" >}
```json
{
  "code": 200,
  "status": "OK",
  "cellsCount": 123,
  "file": "base64编码的工作簿流"
}
```
{< /tab >}
{< /tabs >}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加速开发的最快方式。SDK 封装了底层细节，让您专注于项目任务。请查阅 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 仓库</a> 获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Cloud Web 服务：
`[待定]`
---