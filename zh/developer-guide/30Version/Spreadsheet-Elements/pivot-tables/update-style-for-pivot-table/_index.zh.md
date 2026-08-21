---
title: "更新数据透视表样式"
second_title: "文档"
linktitle: "全部格式化"
type: docs
url: /zh/pivot-tables/format-all/
aliases: [  /zh/update-style-for-pivot-table/ ]
keywords: "数据透视表, 更新样式, Aspose.Cells Cloud, REST API, Excel, 电子表格, API, 数据透视表样式, 全部格式化"
description: "了解如何使用 Aspose.Cells Cloud REST API 更新整个数据透视表的样式。包含请求详情、cURL 示例以及多种编程语言的 SDK 代码片段。"
weight: 100
ArticleTitle: "更新数据透视表样式 - Aspose.Cells Cloud API"
---

此 REST API 用于更新数据透视表的样式。

## PostPivotTableStyle API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/FormatAll
```

**前置条件 / 身份验证**  
必须在 `Authorization` 请求头中提供有效的 JWT 访问令牌（例如：`Bearer <jwt token>`）。请确保该令牌具有访问指定工作簿和工作表的权限。

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，要求使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### **请求参数**

| 参数名称        | 类型    | 位置   | 描述                                                                 |
| --------------- | ------- | ------ | -------------------------------------------------------------------- |
| name            | string  | 路径参数 | 工作簿文件名称。                                                     |
| sheetName       | string  | 路径参数 | 包含数据透视表的工作表名称。                                         |
| pivotTableIndex | integer | 路径参数 | 待格式化数据透视表的从零开始的索引。                                 |
| style           | object  | 请求体 | 用于定义应应用格式的样式数据传输对象（DTO）。                        |
| needReCalculate | boolean | 查询参数 | 设置为 **true** 表示格式化后重新计算数据透视表；默认为 **false**。 |
| folder          | string  | 查询参数 | 工作簿所在文件夹路径。                                               |
| storageName     | string  | 查询参数 | 存储服务名称。                                                       |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/PivotTables/PostPivotTableStyle) 定义了一个公开可访问的编程接口，允许您直接通过 Web 浏览器发起 REST 请求。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0/FormatAll" \
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

**HTTP 状态码**

| 状态码 | 含义           | 描述                                       |
|--------|----------------|--------------------------------------------|
| 200    | OK（成功）     | 筛选器应用成功；响应包含操作详情。         |
| 400    | Bad Request（请求错误） | 缺少或无效参数（例如不支持的文件类型）。 |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                    |
| 413    | Payload Too Large（载荷过大） | 上传文件超出大小限制。               |
| 500    | Internal Server Error（服务器内部错误） | 发生意外服务器错误。              |

{{< /tab >}}

{{< /tabs >}}

## 云 SDK 开发工具包家族

使用 SDK 是调用 API 的最快开发方式。SDK 封装了底层细节，让您专注于业务逻辑。请参阅 <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub 仓库</a> 获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用 Go SDK 调用该 API：

{{< tabs tabTotal="1" tabID="4" tabName1="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "0b2caae7acfa3e947b856c07b6e8633a" >}}

{{< /tab >}}

{{< /tabs >}}