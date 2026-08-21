---
title: "更新图表属性"
type: docs
url: /zh/charts/properties/update/
aliases: [  /zh/update-chart-properties/ ]
weight: 160
keywords: "Aspose.Cells, 图表, 更新, Excel, REST API, SDK"
description: "了解如何使用 Aspose.Cells Cloud REST API（v3.0）更新 Excel 工作簿中的图表属性（类型、标题、图例等）。内容包括端点、参数、cURL 示例以及 C#、Java、PHP、Ruby、Node.js、Perl 和 Go 的 SDK 代码片段。"
ArticleTitle: "更新图表属性 – Aspose.Cells Cloud REST API"
---

此 REST API 用于更新图表属性。

### **安全与身份验证**

Aspose.Cells Cloud API 是安全的，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

## PostWorksheetChart API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}
```

### 请求参数

| 参数名称     | 类型   | 路径/查询字符串/HTTP 请求体 | 描述                                       |
| ------------ | ------ | -------------------------- | ------------------------------------------ |
| name         | string | path                       | Excel 文件的名称。                         |
| sheetName    | string | path                       | 包含图表的工作表名称。                     |
| chartIndex   | integer| path                       | 待更新图表的从零开始的索引。               |
| chart        | object | body                       | 定义要修改的图表属性的 JSON 对象。         |
| folder       | string | query                      | 存储中文件所在的文件夹。                   |
| storageName  | string | query                      | 存储服务的名称。                           |

### 请求体架构

**`chart`** 对象包含可修改的属性。以下是一个包含多个常用字段的代表性 JSON 示例：

```json
{
  "Title": {
    "Text": "季度销售额"
  },
  "ShowLegend": true,
  "Type": "Line",
  "DataLabels": {
    "ShowValue": true,
    "ShowPercentage": false
  },
  "ChartArea": {
    "BorderColor": "Blue",
    "FillColor": "White"
  }
}
```

> **注意：** 仅需提供您需要更改的字段。未提供的属性将保留其现有值。

<a href="https://apireference.aspose.cloud/cells/#/Charts/PostWorksheetChart" target="_blank" rel="noopener noreferrer">OpenAPI 规范</a> 定义了一个公开可访问的编程接口，让您能直接通过 Web 浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet4/charts/1" \
-d '{"Type": "line"}' \
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

{{< /tab >}}

{{< /tabs >}}

## 响应

API 返回一个 JSON 对象，指示操作结果。成功更新时返回：

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**成功状态码**

| HTTP 状态码 | 描述                             |
| ----------- | -------------------------------- |
| 200         | OK（成功）——图表属性已成功更新。 |

**响应头**

| 头部字段        | 描述                                   |
| --------------- | -------------------------------------- |
| `Content-Type`  | `application/json` —— 表示响应体为 JSON 格式。 |
| `X-RequestId`   | 请求的唯一标识符（有助于问题排查）。     |

可能的错误响应包括：

| HTTP 状态码 | 描述                             |
| ----------- | -------------------------------- |
| 400         | Bad Request（错误请求）——参数或请求体无效 |
| 401         | Unauthorized（未授权）——缺少或无效令牌 |
| 404         | Not Found（未找到）——文件、工作表或图表不存在 |
| 500         | Internal Server Error（内部服务器错误） |

有关其他图表相关操作，请参阅相关主题，例如 [更新图表标题](/charts/title/update/) 和 [更新图表图例](/charts/legend/update/)。

## 云 SDK 家族

使用 SDK 是加速开发的最佳方式。SDK 会处理底层细节，使您能专注于项目任务。请查阅 <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub 代码库</a>，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="6" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" tabName4="Node.js" tabName5="Perl" tabName6="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-Charts-UpdateChartProperties-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-CellsChartsPostWorksheetChart-.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-cells_charts_post_worksheet_chart-.rb" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-UpdateChartProperties-1.js" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-UpdateChartProperties-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "d554e51920e174943a60f4343a97e203" >}}

{{< /tab >}}

{{< /tabs >}}