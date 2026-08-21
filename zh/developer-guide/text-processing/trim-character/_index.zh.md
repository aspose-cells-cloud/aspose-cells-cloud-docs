---
title: "Aspose.Cells Cloud 文本修剪 Web API — 删除多余空格和换行符"
second_title: "文档"
ArticleTitle: "Excel 数据清理工具 — 自动修剪字符、空格与换行符 — 在线版 & 短代码"
linktitle: "修剪字符"
type: docs
url: /zh/trim-character/
keywords: "Excel, 文本修剪, 删除空格, 换行符, Aspose.Cells, 数据清理, 电子表格, 规范单元格格式"
description: "使用 Aspose.Cells Cloud API 修剪 Excel 单元格中的多余空格、换行符及无需字符，确保电子表格数据整洁、一致。"
weight: 100
---

使用 Aspose.Cells 修剪字符 API，自动从 Excel 单元格中移除不必要的字符、多余空格及换行符，清理数据条目并统一电子表格格式。

## **功能概览**

- **修剪首尾空格**
  - 移除文本开头和结尾的多余空格
  - 提升数据呈现的整洁度与可读性
- **处理单词间多余空格**
  - 删除单词之间的多余空格
  - 解决多源数据导致的格式混乱问题

- **特殊空格清除**
  - 明确清除不换行空格（Non-breaking spaces）
  - 确保数据准确性与一致性

- **换行符管理**
  - 移除多余或全部换行符
  - 保持单元格内容结构清晰、专业美观

## **TrimCharacter API**

调用 API 前，请确保您已拥有有效的 Aspose Cloud 账户、`client_id`/`client_secret`，以及具有 **Cells** 范围权限的访问令牌（access token）。

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/content/trim
```

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，需通过 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

```bash
-H "Authorization: Bearer {access_token}"
```

### **trimCharacter API 请求参数**

| 参数名                  | 类型     | 路径/查询字符串/HTTP 请求体 | 描述                                                                                                                                                         |
| :---------------------- | :------- | :-------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Spreadsheet             | 文件     | FormData                    | 待处理的电子表格文件。支持格式包括 XLSX、XLS、ODS、CSV 等。                                                                                                 |
| trimContent             | 字符串   | 查询字符串                  | 指定需从单元格内容中修剪的特定字符或字符串，可为单个字符、多个字符或自定义模式。                                                                             |
| trimLeading             | 布尔值   | 查询字符串                  | 若为 `true`，则从每个单元格内容的开头移除指定字符。                                                                                                          |
| trimTrailing            | 布尔值   | 查询字符串                  | 若为 `true`，则从每个单元格内容的结尾移除指定字符。                                                                                                          |
| trimSpaceBetweenWordTo1 | 布尔值   | 查询字符串                  | 若为 `true`，则将单元格内单词之间连续的多个空格缩减为单个空格。                                                                                             |
| trimNonBreakingSpaces   | 布尔值   | 查询字符串                  | 若为 `true`，则从单元格内容中移除不换行空格字符（Unicode U+00A0）。                                                                                         |
| removeExtraLineBreaks   | 布尔值   | 查询字符串                  | 若为 `true`，则将单元格内连续的多个换行符缩减为单个换行符。                                                                                                 |
| removeAllLineBreaks     | 布尔值   | 查询字符串                  | 若为 `true`，则从单元格内容中移除所有换行符。                                                                                                               |
| worksheet               | 字符串   | 查询字符串                  | _（可选）_ 指定需应用文本修剪的工作表名称。若省略，默认作用于第一个工作表。                                                                                   |
| range                   | 字符串   | 查询字符串                  | _（可选）_ 指定需应用文本修剪的单元格范围（例如 `"A1:C10"`）。若省略，默认作用于指定工作表中的所有已用单元格。                                               |
| outPath                 | 字符串   | 查询字符串                  | _（可选）_ 指定处理后工作簿的云存储保存路径。若省略，默认保存至源文件所在文件夹。                                                                             |
| outStorageName          | 字符串   | 查询字符串                  | 输出文件所存储的云存储名称。                                                                                                                                  |
| region                  | 字符串   | 查询字符串                  | _（可选）_ 设置文本处理的区域语言环境，可能影响特定语言（如 `"en-US"`、`"ar-SA"`）中空格与换行符的处理方式。                                                 |
| password                | 字符串   | 查询字符串                  | _（可选）_ 若上传的电子表格受密码保护，请提供密码以打开并处理该文件。                                                                                         |

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

**成功响应示例（HTTP 200）**：API 返回包含已修剪工作簿的文件流。

### 错误代码

- **400 Bad Request（请求错误）**：Aspose.Cells Cloud API URI 无效。
- **401 Unauthorized（未授权）**：访问令牌无效，或 client_id / client_secret 不正确。
- **404 Not Found（未找到）**：电子表格文件无法访问。
- **500 Server Error（服务器错误）**：电子表格在获取计算数据时发生异常。

## Trim Character API 的典型应用场景

- **用户输入规范化**：清理手动输入的表格数据，移除多余空格与换行符。
- **客户数据库维护**：清理客户姓名、地址、联系方式等字段中的冗余空格及格式问题。
- **自动化报告清理**：生成自动化报告前，清理数据源格式。
- **数据迁移准备**：数据迁移至新系统前，统一格式并清理问题。

## 为何应使用 Trim Character API？

- **降低人力成本**：消除耗时的人工数据清理工作
- **减少错误成本**：避免因格式问题导致的分析错误
- **按使用付费**：无固定费用，仅按实际吞吐量计费
- **零基础设施投入**：无需维护服务器或软件
- **多格式支持**：支持 XLSX、XLS、CSV、ODS 等多种格式处理
- **开发者友好**：Aspose.Cells Cloud 提供多语言 SDK，开发便捷，并附带详尽文档；相比自研图表渲染方案，大幅降低开发工作量。
- **成本高效**：无需提前上传工作簿即可去除重复字符，节省存储空间并降低成本。

## OpenAPI 规范

[OpenAPI 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/TrimCharacter) 定义了公开可访问的编程接口，允许您直接从网页浏览器发起 REST 调用。

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加速开发的最佳方式。SDK 封装了底层细节，您只需极简代码即可实现单元格字符修剪功能。
请查阅 <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub 仓库</a> 获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：
{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_TrimTextInSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_TrimTextInSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_TrimTextInSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_TrimTextInSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_TrimTextInSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_TrimTextInSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_TrimTextInSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_TrimTextInSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}