---
title: "拆分文本 API – 将 Excel 单元格内容分段为多列 | Aspose.Cells Cloud"
second_title: "文档"
ArticleTitle: "Excel 文本分段器 – 将单元格内容分段为多列 | Aspose.Cells Cloud"
linktitle: "拆分文本"
type: docs
url: /zh/split-text/
keywords: "Aspose, Cells, 拆分文本 API, Excel, 分隔符, 文本分段, 云 API"
description: "使用 Aspose.Cells Cloud 轻松将 Excel 单元格文本拆分为独立的列或行。支持自定义分隔符、掩码、换行符以及可选的保留分隔符选项。几分钟内即可通过 curl 或 SDK 上手使用。"
weight: 100
---

使用自定义分段规则将 Excel 单元格文本拆分为多列。通过 Aspose.Cells Cloud 的文本拆分 Web API，按分隔符拆分内容，并输出至指定区域。

## **简介**：拆分文本

文本分段 API 可根据指定的分隔符、模式或换行符将单元格内容拆分为多个单元格，并将结果输出到目标区域。它支持灵活的拆分方式、方向性输出（列或行），以及保留分隔符的选项——非常适合解析拼接数据、CSV 样式内容或换行文本，将其转换为结构化格式。

- **按特定字符拆分单元格** – 选择任意字符作为分隔符（如逗号、空格、分号等），将单元格内容拆分为多个单元格。
- **按字符串拆分单元格** – 按您指定的任意字符组合拆分单元格。
- **按掩码拆分文本** – 使用通配符按特定模式拆分文本，提供更灵活、更强大的文本分割方法。
- **按换行符拆分单元格内容** – 通过换行符拆分，使内容呈现更清晰有序。
- **拆分为列或行** – 选择将拆分结果写入连续的列或行。
- **移除或保留分隔符** – 决定是否在结果单元格中移除或保留分隔符（如开头、结尾、文本前、文本后）。

## **SplitText API**

**前提条件**：使用本 API 需要有效的 Aspose Cloud 访问令牌，且待处理的工作簿必须已上传至 Aspose Cloud 存储，或直接在请求中提供。该 API 支持常见的电子表格格式，如 XLSX、XLS、ODS 和 CSV。

### Web API

```http
POST https://api.aspose.cloud/v4.0/cells/content/split/text
```

### **安全性与身份验证**

Aspose.Cells Cloud API 安全可靠，需通过 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

```bash
-H "Authorization: Bearer {access_token}"
```

### **splitText** API 的请求参数如下：

| 参数名称                           | 类型     | 位置       | 是否必需？ | 默认值   | 描述                                                                                                                                         |
| ---------------------------------- | -------- | ---------- | ---------- | -------- | -------------------------------------------------------------------------------------------------------------------------------------------- |
| spreadsheet                        | 文件     | FormData   | 是         | —        | 待处理的电子表格文件。支持格式包括 XLSX、XLS、ODS、CSV 等。                                                                                 |
| delimiters                         | 字符串   | Query      | 否         | —        | 用于拆分单元格内文本的一个或多个分隔符字符（例如 `","`、`";"`、`空格`、`换行符`、`Tab`、`Pipe`、`自定义`）。                                  |
| keepDelimitersInResultingCells     | 布尔值   | Query      | 否         | false    | 若为 `true`，则在拆分后的结果单元格中保留分隔符字符。                                                                                        |
| keepDelimitersPosition             | 字符串   | Query      | 否         | None     | 若 `keepDelimitersInResultingCells` 为 `true`，指定在何处保留分隔符。选项：`None`（不保留）、`AtTheBeginning`（开头）、`AtTheEnd`（结尾）、`BeforeText`（文本前）、`AfterText`（文本后）。 |
| howToSplit                         | 字符串   | Query      | 否         | SplitToColumns | 文本分段方式。选项：`None`（不拆分）、`SplitToColumns`（拆分为列）、`SplitToRows`（拆分为行）。                                             |
| outPositionRange                   | 字符串   | Query      | 是         | —        | 拆分结果写入的目标区域（例如 `"D1:F10"`）。                                                                                                  |
| worksheet                          | 字符串   | Query      | 否         | —        | 应用文本拆分的工作表名称。若省略，则默认使用第一张工作表。                                                                                   |
| range                              | 字符串   | Query      | 否         | —        | 应用拆分操作的源单元格范围（例如 `"A1:A10"`）。若省略，则处理工作表中所有已用单元格。                                                       |
| outPath                            | 字符串   | Query      | 否         | —        | 处理后工作簿保存至的云存储文件夹路径。若省略，则保存至源文件所在文件夹。                                                                     |
| outStorageName                     | 字符串   | Query      | 否         | —        | 输出文件将存储到的云存储名称。                                                                                                               |
| region                             | 字符串   | Query      | 否         | —        | 文本分段的区域设置，可能影响分隔符解析和字符编码（例如 `"en-US"`、`"ja-JP"`）。                                                              |
| password                           | 字符串   | Query      | 否         | —        | 打开受密码保护的电子表格所需的密码。                                                                                                         |

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

### 错误码

- **400 Bad Request（错误请求）** – Aspose.Cells Cloud API URI 无效或参数格式错误。
- **401 Unauthorized（未授权）** – 缺少或无效的访问令牌（或 client-id/secret）。
- **404 Not Found（未找到）** – 无法访问指定的电子表格文件。
- **500 Server Error（服务器错误）** – 处理电子表格时发生内部异常。

## Split Text API 适用于哪些场景？

### **CSV 与文本文件导入清理**

从外部系统导入数据时，字段通常被拼接到单个单元格中：

- **ERP/CRM 数据导入** – 将 `"John Doe;johndoe@email.com;555-1234"` 拆分为独立的姓名、邮箱和电话列。
- **数据库导出** – 解析组合键，如 `"ORD-2024-001|Premium|Express"`，拆分为订单 ID、等级和运输方式。
- **日志文件分析** – 拆分半结构化日志，如 `"2024-01-15 10:30:00|ERROR|ConnectionTimeout"`，便于筛选。

### **遗留系统迁移**

- 旧系统将多值字段转储至单个单元格；通过拆分使其匹配新数据库模式。
- 将平面文件导出转换为标准化的 Excel 表格，以便用于 Power BI 或 Tableau。

### **数据清洗与标准化**

- **分隔符统一化** – 使用多分隔符拆分，将混合分隔符（如 `"A,B;C|D"`）转换为统一格式。
- **空白字符清理** – 按空格拆分，识别并移除单词间的多余空格。
- **财务数据** – 将组合交易代码（如 `"DEP-CHK-3847"`）拆分为交易类型、来源和参考号。
- **医疗记录** – 解析患者数据（如 `"Smith,Jane_F_1985"`），拆分为姓、名、性别和出生年份。

## 为何应使用 Split Text API？

- **特定字符拆分** – 可按任意单字符拆分（逗号、分号、Tab、空格）。
- **字符串组合拆分** – 使用多字符分隔符，如 `||`、`->` 或自定义分隔符。
- **换行符拆分** – 立即将多行单元格内容拆分为独立行（地址、注释、描述等）。
- **自定义分隔符** – 定义任意字符组合为分隔符，适配专有数据格式。
- **开发者友好** – Aspose.Cells Cloud 提供多语言 SDK 库，便于快速开发，并附带详尽文档；相比自行构建解决方案，可显著减少开发工作量。
- **成本效益高** – 可在不提前上传工作簿的情况下移除重复字符，节省存储空间并降低成本。

## OpenAPI 规范

[OpenAPI 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/SplitText) 定义了一个公开可访问的编程接口，允许您直接从 Web 浏览器执行 REST 调用。

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加速开发的最佳方式。SDK 处理底层细节，让您仅需少量代码即可实现单元格文本拆分功能。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SplitText.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SplitText.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SplitText.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SplitText.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SplitText.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SplitText.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SplitText.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SplitText.go" >}}  
{{</tab>}}  
{{< /tabs >}}