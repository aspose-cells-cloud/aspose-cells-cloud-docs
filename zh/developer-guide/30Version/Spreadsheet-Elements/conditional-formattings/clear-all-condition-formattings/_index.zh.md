---
title: "清除条件格式"
type: docs
url: /zh/conditional-formattings/clear/
aliases: [  /zh/clear-all-condition-formattings/ ]
keywords: "Aspose.Cells Cloud, REST API, 清除条件格式, Excel, 工作表, JWT, v3.2"
description: "使用 Aspose.Cells Cloud API (v3.2) 从工作表中删除所有条件格式规则。了解请求语法、所需参数、认证步骤，并查看多种 SDK 的示例代码。"
weight: 80
---

此 REST API 用于从工作表中清除所有条件格式规则。

## REST API

```bash
DELETE https://api.aspose.cloud/v3.2/cells/{name}/worksheets/{sheetName}/conditionalFormattings
```

### 请求参数

| 参数名称        | 类型   | 位置   | 描述                                                       |
| --------------- | ------ | ------ | ---------------------------------------------------------- |
| **name**        | string | path   | 工作簿文件的名称（例如：`Book1.xlsx`）。                   |
| **sheetName**   | string | path   | 要移除条件格式的工作表名称。                               |
| **folder**      | string | query  | （可选）工作簿所在的存储文件夹路径。                       |
| **storageName** | string | query  | （可选）存储服务的名称。                                   |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/ConditionalFormattings/DeleteWorksheetConditionalFormattings) 定义了一个公开可访问的编程接口，**OpenAPI 规范**还允许您直接从 Web 浏览器发起 REST 请求。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.2/cells/Book1.xlsx/worksheets/sheet1/conditionalFormattings" \
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

### 错误响应

| HTTP 状态码 | 原因                                         | 示例响应正文                                                     |
| ----------- | -------------------------------------------- | ---------------------------------------------------------------- |
| **400**     | 请求错误 — 缺少或无效的参数。                | `{ "Code":"400", "Message":"Invalid parameter value." }`         |
| **401**     | 未授权 — 缺少或无效的 JWT 令牌。             | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404**     | 未找到 — 工作簿或工作表不存在。              | `{ "Code":"404", "Message":"File not found." }`                  |
| **500**     | 服务器内部错误 — 服务器发生意外故障。        | `{ "Code":"500", "Message":"An unexpected error occurred." }`    |

## SDK 示例

使用 SDK 是加速开发的最佳方式。SDK 会处理底层细节，让您专注于项目任务。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ConditionalFormatting-ClearConditionFormattings-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-clear-all-formatting.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-ConditionalFormatting-delete_worksheet_conditional_formattings-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-ConditionalFormatting-ClearConditionFormattings-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-ConditionalFormatting-ClearConditionFormattings-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "63fda1be9e5149f83edca47ce58dac87" >}}

{{< /tab >}}

{{< /tabs >}}