---
title: "Aspose.Cells Cloud 添加文本 API — 一次性为多个 Excel 单元格添加文本 — 插入前缀、后缀及标签"
second_title: "文档"
articleTitle: "Excel 批量文本插入 — 为单元格添加前缀、后缀及自定义文本 — 分步指南"
linktype: "AddText"
type: docs
url: /zh/add-text/
keywords: "Aspose Cells API, Excel 添加文本, 批量文本插入, Excel 前缀后缀, 电子表格文本替换, Excel 自动化, 云电子表格 API"
description: "通过 Aspose.Cells Cloud，一次调用即可向多个 Excel 单元格插入前缀、后缀或自定义标签。支持在文本开头、结尾、指定文本之前或之后插入。支持范围、工作表及空单元格处理。"
weight: 100
---

一次操作即可向多个 Excel 单元格插入文本。使用 Aspose.Cells API，可在单元格开头、结尾，或指定文本之前/之后添加前缀、后缀、标签或自定义字符。

## 概述

通过单次调用，将前缀、后缀或锚点字符串批量插入目标区域内的所有单元格 —— 无需公式，无需辅助列。

- 在每个单元格内的**任意位置**插入自定义文本

| 值               | 描述                                                                 |
| ---------------- | -------------------------------------------------------------------- |
| `None`           | 替换原始内容                                                        |
| `AtTheBeginning` | 在开头插入（前缀）                                                  |
| `AtTheEnd`       | 在结尾插入（后缀）                                                  |
| `BeforeText`     | 在 `selectText` 首次出现**之前**插入；若未找到则跳过               |
| `AfterText`      | 在 `selectText` 首次出现**之后**插入；若未找到则跳过               |

- 四种位置模式：前缀、后缀、在子字符串之前/之后插入。
- 跳过空白单元格以避免杂乱。
- API 仅处理**字符串类型**的值；数字、布尔值和公式将先转换为文本。
- **空单元格处理**：
  - `skipEmptyCells = true` → 跳过空单元格。
  - `skipEmptyCells = false` → 向空单元格插入文本（单元格变为文本类型）。

- **锚点未找到**：当 `position = BeforeText | AfterText` 且 `selectText` **不存在**时，单元格内容保持不变。

### **Web API**

```http
PUT https://api.aspose.cloud/v4.0/cells/content/add/text
```

### **安全与身份验证**

Aspose.Cells Cloud API 安全可靠，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

```bash
-H "Authorization: Bearer {access_token}"
```

### **AddText API 的请求参数**

| 参数名称         | 类型    | 路径/查询字符串/HTTP 请求体 | 描述                                                                                                                                                       | 必填 |
| :--------------- | :------ | :-------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------- | :--- |
| Spreadsheet      | File    | FormData                    | 待处理的电子表格文件。支持格式包括 XLSX、XLS、ODS、CSV 等。                                                                                               | 是   |
| text             | String  | Query                       | 要添加到电子表格指定单元格的文本内容。                                                                                                                    | 是   |
| position         | String  | Query                       | 指定相对于现有单元格内容的插入位置。选项：`AtTheBeginning`、`AtTheEnd`、`BeforeText`、`AfterText`、`None`。                                               | 是   |
| selectText       | String  | Query                       | _（可选）_ 若提供，仅在包含该精确子字符串的单元格中插入文本。需与 `position` 参数配合使用。                                                                | 否   |
| skipEmptyCells   | Boolean | Query                       | 若为 `true`，跳过空单元格；若为 `false`，向空单元格插入文本。                                                                                             | 否   |
| worksheet        | String  | Query                       | _（可选）_ 文本将被添加的工作表名称。若省略，默认作用于第一张工作表。                                                                                     | 否   |
| range            | String  | Query                       | _（可选）_ 文本将被添加的单元格范围（例如 `"A1:C10"`）。若省略，默认作用于指定工作表中的所有已用单元格。                                                 | 否   |
| outPath          | String  | Query                       | _（可选）_ 处理后工作簿的云存储文件夹路径。若省略，文件将保存在源文件夹中。                                                                               | 否   |
| outStorageName   | String  | Query                       | 输出文件将被存储到的云存储名称。                                                                                                                           | 否   |
| region           | String  | Query                       | _（可选）_ 设置输出文件中数字、日期和货币的区域设置（例如 `"en-US"`、`"zh-CN"`、`"de-DE"`）。                                                             | 否   |
| password         | String  | Query                       | _（可选）_ 若上传的电子表格受密码保护，请提供密码以打开并处理该文件。                                                                                    | 否   |

**cURL 示例**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/content/add/text?text=Report&position=AtTheBeginning&skipEmptyCells=true" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/workbook.xlsx" \
  -F "outPath=output/workbook_modified.xlsx"
```

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

| 代码  | 描述                                       |
| ----- | ------------------------------------------ |
| **400** | 请求无效（Bad Request）：Aspose.Cells Cloud API URI 无效或缺少必需参数。 |
| **401** | 未授权（Unauthorized）：访问令牌无效，或客户端 ID 和密钥无效。          |
| **404** | 未找到（Not Found）：电子表格文件不可访问。                            |
| **500** | 服务器错误（Server Error）：电子表格在获取计算数据时发生异常。          |

## Add Text for Spreadsheet API 的典型应用场景

- **动态报表标签**：为自动生成的财务报表和销售报告添加动态标题、日期标签或备注。
- **批量文件加水印**：为一批 Excel 文件添加公司 Logo、保密水印或版本信息。
- **模板数据填充**：自动在合同或发票模板的指定位置填充客户名称、金额等文本。
- **数据分类标记**：根据分析结果，为数据行自动添加分类标签或状态标签（例如“待审核”、“已批准”）。
- **数据质量标注**：在数据清洗过程中，为问题数据添加备注说明。
- **批量文本格式化**：统一为产品名称或客户名称添加前缀或后缀。

## 为何应使用 Add Text for Spreadsheet API？

- **批量文本添加**：一次性为数百个单元格或文件添加文本，相比手动操作最多可节省 95% 的时间。
- **精准位置控制**：支持在六个位置精准插入文本，包括开头、结尾或单元格内指定文本之前/之后。
- **智能条件处理**：可选择是否根据单元格是否为空或是否包含特定文本来添加文本。
- **多位置策略支持**：
  - `AtTheBeginning`：为所有选定单元格的内容前添加相同文本。
  - `AtTheEnd`：为所有选定单元格的内容后添加文本。
  - `BeforeText` / `AfterText`：仅在包含指定文本的单元格中，在该文本之前或之后插入文本。
  - `None`：替换原始内容。
- **精准范围控制**：支持指定特定工作表或单元格范围进行操作。
- **条件跳过选项**：支持跳过空单元格，避免不必要的文本添加。
- **开发者友好**：Aspose.Cells Cloud 提供多种语言的 SDK 库，便于快速开发，并配有详尽文档。相比构建自定义图表渲染方案，大幅降低开发工作量。
- **高性价比**：可直接向单元格追加文本，无需提前上传工作簿，节省存储空间并降低费用。

## OpenAPI 规范

[OpenAPI 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/AddText) 定义了一个公开可访问的编程接口，允许您直接通过网页浏览器执行 REST 交互。

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加速开发的最佳方式。SDK 处理底层细节，让您仅用最少代码即可实现单元格文本添加功能。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同语言的 SDK 调用 Aspose.Cells Web 服务：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_AddText.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_AddText.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_AddText.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_AddText.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_AddText.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_AddText.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_AddText.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_AddText.go" >}}
{{</tab>}}
{{< /tabs >}}