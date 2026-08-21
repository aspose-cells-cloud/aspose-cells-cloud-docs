---
title: "Aspose.Cells Cloud 移除字符 Web API — 从 Excel 中删除自定义字符与子字符串（在线短代码）"
secondtitle: "文档"
articletitle: "Excel 文本清理工具 — 从选定区域删除字符与子字符串"
linktitle: "移除字符"
type: docs
url: /zh/remove-characters/
keywords: "Aspose.Cells, 移除字符, Excel API, 文本清理, 电子表格"
description: "从选定范围内的 Excel 单元格中移除自定义字符、字符集及子字符串。借助 Aspose.Cells API 精准删除特定位置的文本，实现数据清洗。"
weight: 100
---

通过删除选定单元格区域中的自定义字符、字符集或子字符串来清理 Excel 数据。使用 Aspose.Cells API 删除特定位置的文本，实现精准的数据格式化。

## 简介

轻松清理并标准化 Excel 数据，移除特定的不必要字符。本插件提供多种针对性方法，帮助您净化单元格内容：

- **移除自定义字符**  
  删除您定义的任意指定符号。只需在输入框中逐个输入字符，插件将立即从所选单元格中移除所有对应实例。非常适合清除唯一分隔符、拼写错误或特殊标记。

- **移除字符集（批量清理）**
  - **不可见字符（Non-printing Characters）** — 清除干扰分析与格式化的不可见字符（换行符、回车符、制表符，以及其他控制字符如 ASCII 0‑31、127、129、141、143、144、157）。
  - **文本字符（所有字母）** — 通过删除所有字母（A‑Z、a‑z），从选定区域中仅保留数字与符号。
  - **数字字符（所有数字）** — 删除所有数字（0‑9），提取纯文本内容，非常适合清洗产品名称或文本描述。
  - **符号** — 移除各类符号杂项，包括数学符号（如 ±、√）、几何符号（如 ∆、°）、技术符号、货币符号（如 £、¢）以及字母形符号（如 ™、®、©）。
  - **标点符号** — 删除句号、逗号、引号、连字符等所有标点，获得无标点的干净文本。

- **移除特定子字符串**  
  不仅限于单个字符，还可删除完整单词或特定字符序列。轻松移除数据集中常见的前缀、后缀或其他冗余文本短语。

**版本 4.0 — 更新于 2024-11-15**

## RemoveCharacters API

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/content/remove/characters
```

### **安全与身份验证**

Aspose.Cells Cloud API 安全可靠，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

```bash
-H "Authorization: Bearer {access_token}"
```

### 请求参数

| 参数名称          | 类型   | 位置               | 描述                                                                                                                                                                                                                      |
| ----------------- | ------ | ------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet       | 文件   | FormData           | 待处理的电子表格文件。支持格式包括 XLSX、XLS、ODS、CSV 等。                                                                                                                                                             |
| removeTextMethod  | 字符串 | Query（查询参数）  | 指定文本移除方式。选项：`None`（不移除）、`RemoveCustomCharacter`（移除自定义字符）、`RemoveCharacterSets`（移除字符集）、`RemoveSubString`（移除子字符串）。默认为 `None`。                                           |
| characterSets     | 字符串 | Query              | 当 `RemoveCharacterSets` 被选中时，指定需移除的预设字符集。选项：`NonPrintingCharacters`（不可见字符）、`TextCharacters`（所有字母）、`NumericCharacters`（所有数字）、`Symbols`（符号）、`PunctuationMarks`（标点）。可使用逗号组合多个字符集。 |
| removeCustomValue | 字符串 | Query              | 使用 `RemoveCustomCharacter` 或 `RemoveSubString` 时，指定需移除的自定义字符或子字符串。                                                                                                                                |
| worksheet         | 字符串 | Query（可选）      | 应用文本移除操作的工作表名称。**若省略，则默认处理工作簿中的第一张工作表。**                                                                                                                                             |
| range             | 字符串 | Query（可选）      | 应用文本移除操作的单元格区域（如 `"A1:C10"`）。**若省略，则操作将应用于指定工作表中的所有已用单元格。**                                                                                                                  |
| outPath           | 字符串 | Query（可选）      | 处理后工作簿的保存路径（云存储中的文件夹路径）。若省略，则保存在源文件所在文件夹。                                                                                                                                       |
| outStorageName    | 字符串 | Query（可选）      | 输出文件所存储的云存储名称。                                                                                                                                                                                              |
| region            | 字符串 | Query（可选）      | 设置字符集定义的区域设置（如 `"en-US"`、`"ja-JP"`）。                                                                                                                                                                    |
| password          | 字符串 | Query（可选）      | 若工作簿受密码保护，则提供相应密码。                                                                                                                                                                                      |

### 响应

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

### 错误码

- **400 Bad Request（错误请求）** — Aspose.Cells Cloud API URI 无效。
- **401 Unauthorized（未授权）** — 访问令牌无效，或客户端 ID/密钥错误。
- **404 Not Found（未找到）** — 电子表格文件不可访问。
- **500 Server Error（服务器错误）** — 电子表格在获取计算数据时发生异常。

## 移除字符 API 的适用场景

- **数据导入/导出** — 清理导入的 CSV/数据，移除不可见字符及格式错误。
- **数据库管理** — 标准化产品代码、ID 和名称，移除不必要符号或标点。
- **财务分析** — 剥离货币符号与文本字符，提取纯数字。
- **文本处理** — 移除换行符与制表符，便于文本分析与报告生成。
- **库存管理** — 清除产品名称中冗余的前缀或后缀。

## 为何选择移除字符 API？

- **节省时间** — 一次性批量移除多种字符类型，替代手动清理。
- **确保准确性** — 消除导致分析错误与格式问题的隐藏字符。
- **标准化数据** — 实现跨数据集与系统的格式一致性。
- **提升分析质量** — 按需提取纯数字或纯文本，获得干净、可直接分析的数据。
- **修复导入错误** — 移除导致数据库与公式失效的异常字符。
- **开发者友好** — Aspose.Cells Cloud 提供多种语言 SDK，配合详尽文档，可快速开发；相比自研方案，大幅降低开发工作量。
- **成本效益高** — 无需预先上传工作簿即可执行字符移除，节省存储空间与成本。

## OpenAPI 规范

[OpenAPI 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/RemoveCharacters) 定义了公开可访问的编程接口，支持您直接通过 Web 浏览器发起 REST 调用。

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加速开发的最佳方式。SDK 封装底层细节，使您能以最少代码实现单元格的 **移除字符** 功能。请访问 [GitHub 仓库](https://github.com/aspose-cells-cloud)，查看 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同语言的 SDK 调用 Aspose.Cells Web 服务：

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