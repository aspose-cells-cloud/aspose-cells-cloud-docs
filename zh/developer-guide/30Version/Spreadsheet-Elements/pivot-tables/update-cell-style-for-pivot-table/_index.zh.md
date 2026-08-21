---
title: "更新数据透视表单元格样式"
second_title: "文档"
linktype: 格式化
type: docs
url: /zh/pivot-tables/format/
aliases: [/zh/update-cell-style-for-pivot-table/]
keywords: "Aspose.Cells Cloud, 数据透视表样式, 更新单元格样式 API, REST API, Excel API, 电子表格格式化, 云 SDK, 单元格样式, 数据透视表"
description: "了解如何通过 REST API 更新 Aspose.Cells Cloud 数据透视表中特定单元格的样式。内容包括端点、参数、身份验证、cURL 示例、Go SDK 代码片段以及 SEO 优化的使用指南。"
weight: 90
ArticleTitle: "更新数据透视表单元格样式 - Aspose.Cells Cloud API 文档"
---

此 REST API 用于更新数据透视表中某单元格的**样式**。

**前提条件 / 身份验证**  
要调用此端点，您必须拥有有效的 Aspose Cloud JWT 访问令牌。请通过[身份验证指南](/authentication/)中描述的 OAuth 2.0 流程获取该令牌，并在请求头中包含该令牌：

```http
Authorization: Bearer <jwt token>
```

所有 Aspose.Cells Cloud API 调用均需提供 JWT 令牌。

## PostPivotTableCellStyle API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/Format
```

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，要求使用<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### **请求参数**

| 参数名            | 类型    | 位置   | 描述                                                                                         |
|-------------------|---------|--------|----------------------------------------------------------------------------------------------|
| name              | string  | 路径   | 文档名称（必填）。                                                                           |
| sheetName         | string  | 路径   | 工作表名称（必填）。                                                                         |
| pivotTableIndex   | integer | 路径   | 数据透视表索引（必填）。                                                                     |
| column            | integer | 查询   | 待格式化单元格的从零开始的列索引（必填）。                                                   |
| row               | integer | 查询   | 待格式化单元格的从零开始的行索引（必填）。                                                   |
| style             | object  | 请求体 | 样式 DTO（数据传输对象），用于定义新的单元格样式。                                           |
| needReCalculate   | boolean | 查询   | 指示样式应用后是否需重新计算数据透视表。默认值为 **false**。                                |
| folder            | string  | 查询   | 文档所在文件夹路径（可选）。                                                                 |
| storageName       | string  | 查询   | 存储名称（可选）。                                                                           |
| Method            | string  | N/A    | 请求所使用的 HTTP 方法（**POST**）。                                                        |

<a href="https://apireference.aspose.cloud/cells/#/PivotTables/PostPivotTableCellStyle" target="_blank" rel="noopener noreferrer">OpenAPI 规范</a>定义了一个公开可访问的编程接口，支持您直接通过网页浏览器与 REST 接口交互。

您可以使用 **cURL** 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何通过 cURL 调用云 API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0/Format?column=1&row=1" \
  -X POST \
  -d '{"Font":{"Name":"Arial","Size":10}}' \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**响应说明**  
成功时，服务返回 HTTP 200 状态码，响应体为空，表示样式已成功应用。若发生错误，则返回包含错误代码及消息的 JSON 响应体。

| HTTP 状态码 | 描述                                           |
|-------------|------------------------------------------------|
| 200         | 样式成功应用。                                 |
| 400         | 请求错误 — 例如，列/行索引无效。               |
| 401         | 未授权 — 缺失或无效的 JWT 令牌。               |
| 404         | 未找到 — 指定的文档、工作表或数据透视表不存在。 |
| 500         | 服务器内部错误 — 意外情况导致。                |

成功时响应体为空。

更多信息，请参见 **Get Pivot Table** API 文档。

## 云 SDK 开发工具集

使用 SDK 是最快捷的开发方式。SDK 封装了底层细节，让您专注于业务逻辑。请查阅 <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub 仓库</a> 以获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用 **Go SDK** 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="1" tabID="4" tabName1="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "3236805d26482f06f4656b14f2d00d79" >}}

{{< /tab >}}

{{< /tabs >}}

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "更新数据透视表单元格样式",
  "description": "指南：使用 REST API 更新 Aspose.Cells Cloud 数据透视表中特定单元格的样式。",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "datePublished": "2026-07-30",
  "keywords": "Aspose.Cells Cloud, 数据透视表, 单元格样式, REST API, Go SDK",
  "url": "https://docs.aspose.cloud/cells/pivot-tables/format/",
  "publisher": {
    "@type": "Organization",
    "name": "Aspose"
  }
}
</script>