---
title: "Aspose.Cells Cloud Web API - 将 Excel 中的文本转换为数字并清理特殊字符"
second_title: "文档"
ArticleTitle: "Excel 数据清理工具 - 将文本转换为数字并移除不需要的字符"
linktitle: "转换文本"
type: docs
url: /zh/convert-text/
keywords: "Aspose.Cells 文本转换, Excel 文本转数字, 移除 Excel 特殊字符, 替换 Excel 换行符, 规范化带重音字符, Excel 数据清理 API"
description: "使用 Aspose.Cells Cloud API 将文本格式的数字转换为数值，替换不需要的字符和换行符，并将带重音字符规范化为标准字母。"
weight: 100
---

使用 Aspose.Cells API 清理 Excel 数据：将文本格式的数字转换为数值、替换不需要的字符和换行符，并将带重音字符规范化为标准字母。

## 概述

**一键将数字形式的文本转换为数值、清除垃圾数据、替换重音字符——仅需一次调用，无需任何公式。**

- **将以文本形式存储的数字转换为数值**：将以文本格式存储的数字数据转换为真正的数值，确保计算准确及数据表示正确。
- **替换特定字符**：一次性替换所选单元格中指定字符的所有出现次数，以统一数据格式。
- **将换行符替换为空格、逗号或分号**：通过将换行符替换为空格、逗号或分号，提升可读性，使数据呈现更整洁、美观。
- **替换带重音字符**：若数据包含多种语言，可将“é”或“ü”等带重音字符替换为对应的无重音字符，增强一致性与清晰度。

## **ConvertText API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/content/convert/text
```

### **安全与认证**

Aspose.Cells Cloud API 安全可靠，需使用<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的认证方式</a>。

```bash
-H "Authorization: Bearer {access_token}"
```

### **convertText** API 的请求参数如下：

| 参数名称         | 类型   | 路径/查询字符串/HTTP 请求体 | 描述                                                                                                                                                   |
| ---------------- | ------ | --------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Spreadsheet      | 文件   | FormData                    | 待处理的电子表格文件。支持格式包括 XLSX、XLS、ODS、CSV 等。                                                                                           |
| convertTextType  | 字符串 | 查询字符串                  | 指定要应用的文本转换类型，例如将文本格式数字转换为数值，或把带重音字符转换为无重音等价字符。                                                           |
| sourceCharacters | 字符串 | 查询字符串                  | 指定需从文本中替换或移除的字符、字符串或模式（例如 `"é,è,ê"`、`"#N/A"`、`"\\n"` 表示换行符）。                                                       |
| targetCharacters | 字符串 | 查询字符串                  | 指定用于替换源字符的替换字符或字符串（例如 `"e"` 表示重音字母替换，`""` 表示删除，`" "` 表示换行符替换为空格）。                                      |
| worksheet        | 字符串 | 查询字符串                  | _（可选）_ 应用文本转换的工作表名称。若省略，则操作应用于第一个工作表。                                                                               |
| range            | 字符串 | 查询字符串                  | _（可选）_ 应用文本转换的单元格范围（例如 `"A1:C10"`）。若省略，则操作应用于指定工作表中所有已用单元格。                                             |
| outPath          | 字符串 | 查询字符串                  | _（可选）_ 处理后工作簿保存到的云存储文件夹路径。若省略，则文件保存在源文件所在文件夹。                                                               |
| outStorageName   | 字符串 | 查询字符串                  | 输出文件将存储到的云存储名称。                                                                                                                         |
| region           | 字符串 | 查询字符串                  | _（可选）_ 设置文本转换规则的区域设置，尤其适用于语言特定的字符处理（例如 `"en-US"`、`"fr-FR"`）。                                                    |
| password         | 字符串 | 查询字符串                  | _（可选）_ 若上传的电子表格受密码保护，请提供密码以打开并处理该文件。                                                                                 |

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

### 错误代码

- **400 Bad Request（错误请求）**：Aspose.Cells Cloud API 的 URI 无效。
- **401 Unauthorized（未授权）**：访问令牌无效，或客户端 ID 和密钥无效。
- **404 Not Found（未找到）**：电子表格文件无法访问。
- **500 Server Error（服务器错误）**：电子表格在获取计算数据时发生异常。

## Convert Text API 的典型应用场景

- **数字格式修正**：将以文本形式存储的数字（例如 “123.45”）转换为可用于计算的数值格式。
- **特殊字符清理**：从数据中移除不必要的特殊符号、多余空格或不可见字符。
- **换行符处理**：将单元格中的换行符替换为空格或其他分隔符。
- **重音字符规范化**：将带重音字母（例如 “é”、“ñ”）转换为标准字母（“e”、“n”）。
- **CSV 文件预处理**：在将 CSV 文件导入 Excel 之前，统一文本格式。

## 为何应使用 Convert Text API？

- **自动格式转换**：通过一次请求批量将文本格式数字转换为可计算数值。
- **字符标准化**：统一处理特殊字符、变音符号及编码问题。
- **数据一致性**：确保整个数据集中文本格式完全一致。
- **开发者友好**：Aspose.Cells Cloud 提供多种编程语言的 SDK 库，便于快速开发，并提供详尽文档。相比自行构建文本处理方案，可大幅减少开发工作量。
- **成本效益高**：无需预先上传工作簿即可进行文本转换，节省存储空间并降低成本。

## OpenAPI 规范

[OpenAPI 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/ConvertText) 定义了公开可访问的编程接口，允许您直接通过网页浏览器执行 REST 交互。

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加速开发的最佳方式。SDK 处理底层细节，使您只需极少代码即可实现单元格文本转换功能。  
请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同语言的 SDK 调用 Aspose.Cells Web 服务：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertText.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertText.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertText.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertText.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertText.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertText.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertText.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertText.go" >}}
{{</tab>}}
{{< /tabs >}}