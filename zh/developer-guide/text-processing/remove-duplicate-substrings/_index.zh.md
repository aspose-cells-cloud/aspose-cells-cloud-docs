---
title: "Aspose.Cells Cloud 移除重复子字符串 Web API —— 清除 Excel 中重复文本"
second_title: "文档"
ArticleTitle: "Excel 重复子字符串清除工具 —— 清理单元格中的重复文本"
linktype: "docs"
url: /zh/remove-duplicate-substrings/
keywords: "Aspose.Cells, 重复子字符串, Excel API, 文本清理, 云服务"
description: "通过 Aspose.Cells Cloud API 移除 Excel 单元格中的重复子字符串，同时保留原有格式和数据验证规则。"
weight: 100
---

使用智能检测功能清除 Excel 单元格中的重复子字符串。利用 Aspose.Cells 去重 API，在保留原始格式的同时消除冗余文本。

## **简介**：精确清除不必要字符

重复子字符串清除 API 可在 Excel 范围内对单个单元格进行处理，移除重复子字符串，同时保留单元格格式、数据验证及其他工作簿结构。它独立处理每个单元格，仅保留每组重复子字符串的首次出现项。

### **数据源选项**

| 字段       | 类型   | 是否必需 | 描述                                  |
| ---------- | ------ | -------- | ------------------------------------- |
| `workbook` | 文件   | 是       | Excel 工作簿文件（.xlsx、.xlsm 等）   |
| `range`    | 字符串 | 是       | 待处理的目标范围（例如："A1:D100"、"Sheet1!A:D"） |

### **分隔符选项**

| 字段                                | 类型    | 默认值     | 描述                                                                                                                                               |
| ----------------------------------- | ------- | ---------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| `delimiters`                        | 字符串  | `"preset"` | 可选值：`preset`、`custom`、`comma`、`semicolon`、`space`、`tab`、`line-break`，或自定义分隔符字符串（多个字符视为复合分隔符）                    |
| `treatConsecutiveDelimitersAsOne`  | 布尔值  | `false`    | 将相邻分隔符合并为单一分隔符                                                                                                                       |
| `caseSensitive`                    | 布尔值  | `false`    | 指定比较是否区分大小写。当设为 `false` 时，重复检测忽略大小写                                                                                      |

## **RemoveDuplicateSubstrings API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/content/remove/duplicate-substrings
```

### **安全性与身份验证**

Aspose.Cells Cloud API 采用安全机制，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

```bash
-H "Authorization: Bearer {access_token}"
```

### **RemoveDuplicateSubstrings API 请求参数**

| 参数名称                        | 类型    | 路径/查询字符串/HTTP 请求体 | 描述                                                                                                                                                         |
| :------------------------------ | :------ | :------------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet                     | 文件    | FormData                   | 待处理的电子表格文件。支持格式包括 XLSX、XLS、ODS、CSV 等。                                                                                                 |
| delimiters                      | 字符串  | 查询字符串                 | 指定用于将单元格内容分割为子字符串以进行重复检测与清除的一个或多个分隔符。可指定多个分隔符（例如 `",;"`）。                                                  |
| treatConsecutiveDelimitersAsOne | 布尔值  | 查询字符串                 | 若设为 `true`，连续的分隔符将被视为单一分隔符；若为 `false`，每个分隔符单独处理。                                                                           |
| caseSensitive                   | 布尔值  | 查询字符串                 | 若为 `true`，重复检测考虑字母大小写（例如 "Text" ≠ "text"）；若为 `false`，重复比较时忽略大小写。                                                           |
| worksheet                       | 字符串  | 查询字符串                 | （可选）指定重复子字符串清除操作所应用的工作表名称。若省略，则默认应用于第一个工作表。                                                                       |
| range                           | 字符串  | 查询字符串                 | （可选）指定重复子字符串清除操作所应用的单元格范围（例如 `"A1:C10"`）。若省略，则默认应用于指定工作表中所有已用单元格。                                     |
| outPath                         | 字符串  | 查询字符串                 | （可选）指定处理后工作簿保存至的云存储路径。若省略，则文件保存在源文件夹中。                                                                                 |
| outStorageName                  | 字符串  | 查询字符串                 | 指定输出文件所存储的云存储名称。                                                                                                                             |
| region                          | 字符串  | 查询字符串                 | （可选）设置文本处理区域设置（locale），可能影响某些语言的分隔符解析及大小写敏感规则（例如 `"en-US"`、`"tr-TR"`）。                                           |
| password                        | 字符串  | 查询字符串                 | （可选）若上传的电子表格受密码保护，请提供密码以打开并处理该文件。                                                                                           |

**示例请求（cURL）**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/content/remove/duplicate-substrings?delimiters=comma&caseSensitive=false" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@Sample.xlsx" \
     -F "range=A1:D100"
```

### **响应示例**

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

### **状态码说明**

| 状态码 | 含义                     | 描述                                                                 |
|--------|--------------------------|----------------------------------------------------------------------|
| 200    | 成功（OK）               | 请求成功，返回已处理的工作簿。                                       |
| 202    | 已接受（Accepted）       | 请求已接受，将进行异步处理。                                         |
| 400    | 错误请求（Bad Request）  | 请求格式错误或包含无效参数。                                         |
| 401    | 未授权（Unauthorized）   | 身份验证失败或缺少/无效的令牌。                                      |
| 404    | 未找到（Not Found）      | 找不到指定的工作簿或资源。                                           |
| 500    | 内部服务器错误（Internal Server Error） | 服务器端发生意外错误。                                               |

## 应用场景：Remove Duplicate Substrings API 的典型用途

- **数据清洗与标准化**：清理标签，如 `"VIP,Premium,VIP,Gold"` → `"VIP,Premium,Gold"`。
- **技术与运营数据**：清理日志中重复的错误代码、去除重复的仓位/货架编号等。
- **内容与媒体管理**：移除重复的技能标签、清除冗余的认证条目等。

## 为何选择 Remove Duplicate Substrings API？

- **自动化人工任务**：消除繁琐的手动编辑，降低人为错误风险。  
- **保持数据完整性**：单元格颜色、字体、边框及条件格式保持不变；下拉列表和验证规则不受影响。  
- **灵活处理方式**：支持任意分隔符、可选大小写敏感控制及表头保护功能。  
- **开发者友好**：Aspose.Cells Cloud 提供多种编程语言的 SDK 库，配合详尽文档，可快速开发。  
- **高性价比**：操作在云端完成，无需本地存储中间文件。  

## OpenAPI 规范

[OpenAPI 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/RemoveDuplicateSubstrings) 定义了公开可访问的编程接口，允许您直接通过 Web 浏览器发起 REST 请求。

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加速开发的最佳方式。SDK 封装了底层细节，您仅需少量代码即可实现单元格重复子字符串清除功能。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，了解完整的 Aspose.Cells Cloud SDK 列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_RemoveCharactersWithFirstNCharacters.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_RemoveCharactersWithFirstNCharacters.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_RemoveCharactersWithFirstNCharacters.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_RemoveCharactersWithFirstNCharacters.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_RemoveCharactersWithFirstNCharacters.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_RemoveCharactersWithFirstNCharacters.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_RemoveCharactersWithFirstNCharacters.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_RemoveCharactersWithFirstNCharacters.go" >}}
{{</tab>}}
{{< /tabs >}}