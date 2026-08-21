---
title: "删除单元格区域 – Aspose.Cells Cloud API 文档"
type: docs
url: /zh/conditional-formattings/delete-cell-area/
aliases: [  /zh/remove-cell-area-from-conditional-formatting/ ]
keywords: "Aspose.Cells Cloud, 删除单元格区域, 条件格式 API, Excel REST API"
description: "使用 Aspose.Cells Cloud REST API 从 Excel 工作表的条件格式中删除指定的单元格区域。包含 ASP.NET、Java 和 Python 示例。"
ArticleTitle: "删除单元格区域 – Aspose.Cells Cloud API 文档"
weight: 70
---

此 REST API 用于从条件格式规则中删除一个单元格区域。

## 安全性与身份验证
Aspose.Cells Cloud API 采用安全机制，需要基于 [JWT 令牌的身份验证](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)。

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/area
```

### 请求参数

| 参数名称       | 类型    | 位置   | 描述                                                         |
| -------------- | ------- | ------ | ------------------------------------------------------------ |
| `name`         | string  | 路径   | Excel 文件的名称。                                           |
| `sheetName`    | string  | 路径   | 包含条件格式的工作表名称。                                   |
| `startRow`     | integer | 查询   | 待删除区域首行的从 0 开始的索引。                            |
| `startColumn`  | integer | 查询   | 待删除区域首列的从 0 开始的索引。                            |
| `totalRows`    | integer | 查询   | 待删除区域的行数。                                           |
| `totalColumns` | integer | 查询   | 待删除区域的列数。                                           |
| `folder`       | string  | 查询   | 文件所在的云存储文件夹（可选）。                             |
| `storageName`  | string  | 查询   | 存储服务的名称（可选）。                                     |

### 错误响应

| HTTP 状态码 | 代码            | 描述                                   | 示例 JSON                                                    |
| ----------- | --------------- | -------------------------------------- | ------------------------------------------------------------ |
| 400         | `BadRequest`    | 缺失或无效的参数。                     | `{ "Code": "400", "Message": "Invalid request parameters." }` |
| 401         | `Unauthorized`  | 缺失或无效的 JWT 令牌。                | `{ "Code": "401", "Message": "Authentication failed." }`      |
| 404         | `NotFound`      | 文件、工作表或条件格式未找到。         | `{ "Code": "404", "Message": "Resource not found." }`         |
| 500         | `InternalError` | 服务器发生意外错误。                   | `{ "Code": "500", "Message": "Internal server error." }`      |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/ConditionalFormattings/DeleteWorksheetConditionalFormattingArea) 定义了一个公开可访问的编程接口，允许您直接从 Web 浏览器发起 REST 请求。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Cloud 服务。以下示例演示如何使用 cURL 调用 **删除单元格区域** 端点。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet1/conditionalFormattings/area?startRow=3&startColumn=3&totalRows=1&totalColumns=1" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## 云 SDK 家族

使用 SDK 是加速开发的最佳方式。SDK 会处理底层细节，让您专注于项目任务。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud){:target="_blank" rel="noopener noreferrer"}，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ConditionalFormatting-RemoveCellAreaFromConditionalFormatting-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-remove-cell-area-from-conditional-formatting.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-ConditionalFormatting-delete_worksheet_conditional_formatting_area-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-ConditionalFormatting-RemoveCellAreaFromConditionalFormatting-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-ConditionalFormatting-RemoveCellAreaFromConditionalFormatting-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "2bc4a93409f78b40b6bcf681c6a14bda" >}}

{{< /tab >}}

{{< /tabs >}}