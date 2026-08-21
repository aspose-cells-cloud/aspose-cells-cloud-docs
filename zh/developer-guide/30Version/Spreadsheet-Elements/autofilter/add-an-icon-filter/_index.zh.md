---
title: "为 Excel 工作表添加图标筛选器"
second_title: "文档"
linktitle: "添加图标筛选器"
type: docs
url: /autofilter/add-icon-filter/
aliases: [/add-an-icon-filter/,/autofilter/add-an-icon-filter/]
keywords: "Aspose.Cells Cloud、Excel、图标筛选器、自动筛选、REST API"
description: "了解如何使用 Aspose.Cells Cloud REST API 为 Excel 工作表添加图标筛选器，包括请求详情、cURL 示例、SDK 代码示例以及错误处理。"
weight: 65
ArticleTitle: "为 Excel 工作表添加图标筛选器 – Aspose.Cells Cloud 文档"
---

## REST API

本 REST API 使用 **Aspose.Cells Cloud REST API** 为 Excel 工作表添加**图标筛选器**。

**背景说明**：图标筛选器根据单元格的值应用视觉图标集，从而实现对数据趋势的快速可视化分析。常见应用场景包括高亮显示绩效指标、状态指示符，或直接在 Excel 工作表中使用红绿灯图标对值进行分类。

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/iconFilter
```

### **安全与身份验证**

Aspose.Cells Cloud API 是安全的，需要使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数：

| 参数名称       | 类型     | 位置   | 描述 |
|----------------|----------|--------|------|
| name           | string   | Path   | 工作簿名称。 |
| sheetName      | string   | Path   | 工作表名称。 |
| range          | string   | Query  | 将应用筛选器的单元格区域（例如 `A1:B1`）。 |
| fieldIndex     | integer  | Query  | 筛选器目标列的从零开始的索引。 |
| iconSetType    | string   | Query  | 要使用的图标集。允许值包括：`Arrows3`、`ArrowsGray3`、`Flags3`、`Signs3`、`Symbols3`、`Symbols32`、`TrafficLights31`、`TrafficLights32`、`Arrows4`、`ArrowsGray4`、`Rating4`、`RedToBlack4`、`TrafficLights4`、`Arrows5`、`ArrowsGray5`、`Quarters5`、`Rating5`、`Stars3`、`Boxes5`、`Triangles3`、`None`、`CustomSet`、`Smilies3`、`ColorSmilies3`。 |
| iconId         | integer  | Query  | 所选图标集中特定图标的标识符。 |
| matchBlanks    | boolean  | Query  | 是否包含空白单元格（`true` 或 `false`）。 |
| refresh        | boolean  | Query  | 应用筛选器后是否刷新筛选器（`true` 或 `false`）。 |
| folder         | string   | Query  | 包含原始工作簿的文件夹。 |
| storageName    | string   | Query  | 工作簿所在的存储名称。 |

### **响应**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP 状态码**

| 状态码 | 含义         | 描述 |
|--------|--------------|------|
| 200    | OK（成功）   | 筛选器已成功应用；响应包含操作详情。 |
| 400    | Bad Request（错误请求） | 缺失或无效的参数（例如，不支持的文件类型）。 |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。 |
| 413    | Payload Too Large（载荷过大） | 上传的文件超出大小限制。 |
| 500    | Internal Server Error（内部服务器错误） | 意外的服务器错误。 |

## 如何使用 SDK 调用 PutWorksheetIconFilter API

### PutWorksheetIconFilter API 规范

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetIconFilter) 定义了一个公开可访问的编程接口，允许您直接从 Web 浏览器发起 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/iconFilter?range=A1:B1&fieldindex=0&iconsettype=ArrowsGray3&iconid=1" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

可能的响应状态码：

| 状态码 | 描述 |
|--------|------|
| 200    | 筛选器已成功应用。 |
| 400    | 错误请求 — 缺失或无效的参数。 |
| 401    | 未授权 — 无效或缺失的身份验证令牌。 |
| 404    | 工作簿、工作表或指定区域未找到。 |
| 500    | 内部服务器错误。 |
{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加速开发的最佳方式。SDK 负责处理底层细节，让您专注于项目任务。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用 various SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetIconFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetIconFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetIconFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetIconFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetIconFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetIconFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetIconFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetIconFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}

有关其他自动筛选功能，请参阅文档中的 **[添加颜色筛选器](/autofilter/add-color-filter/)**、**[添加日期筛选器](/autofilter/add-date-filter/)** 和 **[清除自动筛选](/autofilter/clear-autofilter/)**。