---
title: "Aspose.Cells Cloud – 替换本地 Excel 文件中的文本（查找与替换 API）"
second_title: "文档"
ArticleTitle: "批量替换本地 Excel 文件中的文本 – 查找与替换 API"
linktitle: "替换电子表格内容"
type: docs
url: /replace-spreadsheet-content/
keywords: "替换 Excel 中的文本, Aspose.Cells 查找与替换, 本地电子表格 API, Excel 文件替换, API 替换内容"
description: "无需上传至云端即可替换本地 Excel 工作簿中的文本。使用 Aspose.Cells Cloud 查找与替换 API，单次调用即可更新指定范围、工作表或整个文件。"
weight: 100
---

无需上传至云端即可替换本地 Excel 电子表格文件中的指定文本。利用 Aspose.Cells Cloud 查找与替换 API 实现离线编辑，高效更新工作簿内容。

## **替换电子表格内容 API**

### **Web API**

```http
PUT https://api.aspose.cloud/v4.0/cells/replace/content
```

### **安全性与身份验证**

Aspose.Cells Cloud API 安全可靠，需要使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

```bash
-H "Authorization: Bearer {access_token}"
```

### **请求参数：**

| 参数名称     | 类型   | 路径/查询字符串/HTTP 请求体 | 描述                                                                                                                                               |
| :----------- | :----- | :-------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet  | 文件   | FormData                    | 待处理的本地电子表格文件。支持格式包括 XLSX、XLS、ODS、CSV 等。                                                                                  |
| searchText   | 字符串 | 查询字符串                  | 要在指定工作表和单元格区域中查找的文本字符串。                                                                                                   |
| replaceText  | 字符串 | 查询字符串                  | 将替换指定范围内所有 `searchText` 出现位置的文本字符串。                                                                                         |
| worksheet    | 字符串 | 查询字符串                  | _（可选）_ 执行查找与替换操作的工作表名称。若省略，则操作应用于第一个工作表。                                                                    |
| cellArea     | 字符串 | 查询字符串                  | _（可选）_ 指定的单元格范围（例如 `"A1:D20"`、`"B5:F15"`），在该范围内执行文本查找与替换。若省略，则操作应用于指定工作表中所有已用单元格。       |
| region       | 字符串 | 查询字符串                  | _（可选）_ 设置文本处理的区域设置，可能影响查找操作中的大小写敏感性和字符编码（例如 `"en-US"`、`"fr-FR"`）。                                     |
| password     | 字符串 | 查询字符串                  | _（可选）_ 若上传的电子表格受密码保护，请提供密码以打开并处理文件。                                                                              |

### **响应**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream",
      "Name": "file"
    }
  }
]
```

响应为包含更新后工作簿的二进制流。请将其以适当的文件扩展名（例如 `.xlsx`）保存。

### **错误代码**

- **400 Bad Request（错误请求）** – Aspose.Cells Cloud API URI 无效或参数格式错误。
- **401 Unauthorized（未授权）** – 访问令牌无效或缺失；请获取新的令牌。
- **404 Not Found（未找到）** – 电子表格文件无法访问，或指定的工作表不存在。
- **500 Server Error（服务器错误）** – 处理电子表格时发生内部错误；如问题持续存在，请联系技术支持。

## 替换电子表格内容 API 的适用场景

- **批量处理本地 Excel 文件** – 自动化处理存储在本地的多个工作簿中的查找与替换任务。
- **本地数据处理流程** – 将 API 集成至定期任务中，在报告归档或分发前对其进行修改。
- **本地报告生成** – 无需上传云端，即可向模板工作簿中动态插入值。

## 为何应使用替换电子表格内容 API？

- **开发者友好** – Aspose.Cells Cloud 提供多种编程语言的 SDK 库，支持快速开发并配有详尽文档；相比自研方案，可显著减少开发工作量。
- **降低人工成本** – 减少对专人执行手动文档整合的需求。
- **按需付费** – 无需前期投入，仅为您实际使用的 API 调用次数付费。
- **零维护成本** – 无需维护服务器、无需软件更新、无需担心兼容性问题。
- **保留复杂 Excel 格式** – 替换操作后，原始工作簿的格式、公式和图表均保持不变。

## 如何使用 SDK 调用替换电子表格内容 API

### OpenAPI 规范

[OpenAPI 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/ReplaceSpreadsheetContent) 定义了公开可访问的编程接口，允许您直接从网页浏览器发起 REST 请求。

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加速开发的最快方式。SDK 负责处理底层细节，使您能够以最少代码实现替换内容操作。请参阅官方 **Aspose.Cells Cloud SDK GitHub 仓库**，了解支持的完整编程语言列表。

以下代码示例展示了如何通过多种 SDK 与 Aspose.Cells Web 服务进行交互：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ReplaceTextInLocalFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ReplaceTextInLocalFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ReplaceTextInLocalFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ReplaceTextInLocalFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ReplaceTextInLocalFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ReplaceTextInLocalFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ReplaceTextInLocalFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ReplaceTextInLocalFile.go" >}}
{{</tab>}}
{{< /tabs >}}