---
title: "Aspose.Cells Cloud 按位置删除字符的 Web API — 从 Excel 的特定位置删除文本"
second_title: "文档"
ArticleTitle: "Excel 按位置字符删除器 — 在特定位置删除文本 — 在线 Shortcode"
linktitle: "按位置删除字符"
type: docs
url: /zh/remove-characters-by-position/
keywords: "Aspose.Cells Cloud、按位置删除字符、Excel 文本清理、删除前 N 个字符、删除后 N 个字符、删除标记前文本、删除标记后文本、删除两值之间文本"
description: "使用 Aspose.Cells Cloud Web API 根据位置从 Excel 单元格中删除字符 — 精确删除前/后 N 个字符，或删除指定标记前/后的文本。"
weight: 100
---

按位置从 Excel 单元格中删除字符：删除前/后 N 个字符，或删除指定标记前/后的文本。使用 Aspose.Cells Cloud Web API 实现精准文本清理。


## **简介**：按位置删除不需要的字符

**位置模式**

- `theFirstNCharacters` — 从文本开头删除 N 个字符
- `theLastNCharacters` — 从文本末尾删除 N 个字符
- `allCharactersBeforeText` — 删除首次出现指定子字符串之前的所有字符
- `allCharactersAfterText` — 删除首次出现指定子字符串之后的所有字符
- `BetweenValues` — 删除两个用户定义值之间的子字符串（可选同时删除分隔符本身）

**选项**

- `caseSensitive` — 确定对 `BeforeText`、`AfterText` 和 `BetweenValues` 的搜索是否区分大小写

## **RemoveCharactersByPosition API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/content/remove/characters
```

### **安全与身份验证**

Aspose.Cells Cloud API 安全可靠，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

```bash
-H "Authorization: Bearer {access_token}"
```

### **RemoveCharactersByPosition API 的请求参数**

| 参数名称                | 类型    | 路径/查询字符串/HTTP 正文 | 描述                                                                                                                                                             |
| ----------------------- | ------- | ------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet             | 文件    | FormData                  | 待处理的电子表格文件。支持格式包括 XLSX、XLS、ODS、CSV 等。                                                                                                    |
| Authorization           | 字符串  | 请求头                    | 用于身份验证的 Bearer 令牌（必需）。                                                                                                                             |
| theFirstNCharacters     | 整数    | 查询字符串                | 从每个选定单元格中文本开头删除的字符数（例如 `3` 表示删除前 3 个字符）。                                                                                         |
| theLastNCharacters      | 整数    | 查询字符串                | 从每个选定单元格中文本末尾删除的字符数（例如 `2` 表示删除后 2 个字符）。                                                                                          |
| allCharactersBeforeText | 字符串  | 查询字符串                | 删除每个单元格中指定文本字符串之前出现的所有字符。若该文本多次出现，则基于首次出现位置进行删除。                                                                  |
| allCharactersAfterText  | 字符串  | 查询字符串                | 删除每个单元格中指定文本字符串之后出现的所有字符。若该文本多次出现，则基于首次出现位置进行删除。                                                                   |
| worksheet               | 字符串  | 查询字符串                | （可选）应用字符删除操作的工作表名称。若省略，则操作应用于第一个工作表。                                                                                          |
| range                   | 字符串  | 查询字符串                | （可选）应用字符删除操作的单元格区域（例如 `"A1:C10"`）。若省略，则操作应用于指定工作表中所有已用单元格。                                                        |
| outPath                 | 字符串  | 查询字符串                | （可选）处理后工作簿保存到的云存储文件夹路径。若省略，则文件保存在源文件夹中。                                                                                    |
| outStorageName          | 字符串  | 查询字符串                | 输出文件将要存储到的云存储名称。                                                                                                                                   |
| region                  | 字符串  | 查询字符串                | （可选）设置文本处理的区域设置，对特定语言的字符位置和编码尤其重要（例如 `"en-US"`、`"zh-CN"`）。                                                                 |
| password                | 字符串  | 查询字符串                | （可选）若上传的电子表格受密码保护，请提供密码以打开并处理该文件。                                                                                                |

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

- **200 OK** — 请求成功，并返回已处理的文件。
- **400 Bad Request**：Aspose.Cells Cloud API URI 无效。
- **401 Unauthorized**：访问令牌无效，或客户端 ID 和密钥无效。
- **404 Not Found**：电子表格文件不可访问。
- **500 Server Error**：电子表格在获取计算数据时发生异常。

## 应在何处使用按位置删除字符 API？

- **数据标准化**：清理产品编码（删除前导零或后缀）、电话号码（删除国家代码）
- **文本提取**：从日志文件中提取关键信息（删除时间戳或前缀）
- **文件处理**：整理文件名（删除统一前缀或日期后缀）
- **数据解析**：处理结构化文本（提取方括号或特定标记之间的内容）
- **数据库管理**：清理导入数据（删除固定格式的页眉/页脚字符）

## 为何应使用按位置删除字符 API？

- **精准高效**：直接按位置删除，无需使用复杂的正则表达式。
- **灵活配置**：五种定位模式配合大小写敏感选项，覆盖多样化场景。
- **批量处理**：单次调用即可清理整列数据，效率最高提升 10 倍。
- **智能解析**：轻松处理两个分隔符之间的内容提取。
- **开发者友好**：Aspose.Cells Cloud 提供多种语言的 SDK，加速开发进程并提供详尽文档。相比自行构建文本处理逻辑，可大幅减少开发工作量。
- **成本效益高**：无需先上传工作簿即可删除字符，节省存储空间并降低成本。

## OpenAPI 规范

[OpenAPI 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/RemoveCharactersByPositionInRemoteSpreadsheet) 定义了一个公开可访问的编程接口，允许您直接从网页浏览器执行 REST 交互。

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加速开发的最佳方式。SDK 处理底层细节，使您能以极少代码实现单元格字符按位置删除功能。  
请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_RemoveCharactersByPosition.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_RemoveCharactersByPosition.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_RemoveCharactersByPosition.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_RemoveCharactersByPosition.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_RemoveCharactersByPosition.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_RemoveCharactersByPosition.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_RemoveCharactersByPosition.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_RemoveCharactersByPosition.go" >}}
{{</tab>}}
{{< /tabs >}}
---