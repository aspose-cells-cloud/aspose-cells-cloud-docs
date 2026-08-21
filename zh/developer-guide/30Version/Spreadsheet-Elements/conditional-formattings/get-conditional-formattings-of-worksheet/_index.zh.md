---
title: "获取条件格式规则"
type: docs
url: /conditional-formattings/get-all/
aliases: [/get-conditional-formattings-of-worksheet/]
keywords: "Aspose.Cells Cloud, REST API, Excel, 条件格式, 工作表, 条件格式 API"
description: "使用 Aspose.Cells Cloud REST API 获取应用于工作表的所有条件格式规则。包含请求语法、身份验证步骤、参数、简洁的响应示例以及错误处理。"
weight: 20
---

此 REST API 用于获取应用于工作表的条件格式规则。

## 安全与身份验证
Aspose.Cells Cloud API 采用安全机制，需要基于 [JWT 令牌的身份验证](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)。

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings
```

### 请求参数

| 参数名        | 类型   | 位置   | 描述                             |
| ------------- | ------ | ------ | -------------------------------- |
| name          | string | path   | Excel 文件的名称。               |
| sheetName     | string | path   | 工作表的名称。                   |
| folder        | string | query  | 文件所在的文件夹路径。           |
| storageName   | string | query  | 存储服务的名称（可选）。         |

### 错误响应

| HTTP 状态码 | 原因说明                                     | 示例响应体                                                           |
| ----------- | -------------------------------------------- | -------------------------------------------------------------------- |
| **400**     | 请求错误 — 缺少或无效参数。                  | `{ "Code":"400", "Message":"Invalid parameter value." }`            |
| **401**     | 未授权 — 缺少或无效 JWT 令牌。               | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404**     | 未找到 — 工作簿或工作表不存在。              | `{ "Code":"404", "Message":"File not found." }`                     |
| **500**     | 服务器内部错误 — 发生了意外的服务器故障。    | `{ "Code":"500", "Message":"An unexpected error occurred." }`       |

<a href="https://apireference.aspose.cloud/cells/#/ConditionalFormattings/GetWorksheetConditionalFormattings" target="_blank">OpenAPI 规范</a> 定义了一个公开可访问的编程接口，允许您直接从网页浏览器发起 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何通过 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet1/conditionalFormattings" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <access_token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Status": "OK",
  "ConditionalFormattings": {
    "Count": 1,
    "ConditionalFormattingList": [
      {
        "sqref": "A1:B10",
        "FormatConditions": [
          {
            "Priority": 1,
            "Type": "CellValue",
            "Operator": "GreaterThan",
            "Formula1": "100",
            "Style": {
              "Font": {
                "Color": { "A": 255, "R": 255, "G": 0, "B": 0 },
                "IsBold": true
              }
            }
          }
        ]
      }
    ]
  }
}
```

_上述示例仅展示了最相关的字段，以保持响应体简洁。_

**响应参数**

| 参数                                      | 类型     | 描述                                       |
| ----------------------------------------- | -------- | ------------------------------------------ |
| Status                                    | string   | 请求结果状态（例如 **OK**）。              |
| ConditionalFormattings                    | object   | 条件格式数据容器。                         |
| ConditionalFormattings.Count              | integer  | 返回的条件格式规则数量。                   |
| ConditionalFormattings.ConditionalFormattingList | array    | 条件格式对象列表。                         |
| ConditionalFormattingList[].sqref         | string   | 应用格式的单元格范围（例如 **A1:B10**）。  |
| ConditionalFormattingList[].FormatConditions | array    | 该范围内的格式条件对象集合。               |
| FormatConditions[].Priority               | integer  | 条件的评估优先级。                         |
| FormatConditions[].Type                   | string   | 条件类型（例如 **CellValue**）。           |
| FormatConditions[].Operator               | string   | 条件使用的运算符（例如 **GreaterThan**）。 |
| FormatConditions[].Formula1               | string   | 条件的第一个公式或值。                     |
| FormatConditions[].Style                  | object   | 条件满足时应用的样式。                     |
| Style.Font.Color                          | object   | 字体的 RGBA 颜色定义。                     |
| Style.Font.IsBold                         | boolean  | 表示字体是否加粗。                         |

**HTTP 状态码**

| 状态码 | 含义           | 描述                           |
| ------ | -------------- | ------------------------------ |
| 200    | OK（成功）     | 成功应用筛选；响应包含操作详情。 |
| 400    | 请求错误       | 缺少或无效参数（例如不支持的文件类型）。 |
| 401    | 未授权         | JWT 令牌无效或缺失。           |
| 413    | 负载过大       | 上传的文件超出大小限制。       |
| 500    | 服务器内部错误 | 发生了意外的服务器错误。       |

{{< /tab >}}

{{< /tabs >}}

## 云 SDK 家族

使用 SDK 是加快开发速度的最佳方式。SDK 处理底层细节，让您专注于项目任务。请查看 <a href="https://github.com/aspose-cells-cloud" target="_blank">GitHub 仓库</a>，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ConditionalFormatting-GetWorksheetConditionalFormatting-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-get-conditional-formatting-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-ConditionalFormatting-get_worksheet_conditional_formattings-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-ConditionalFormatting-GetWorksheetConditionalFormatting-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-ConditionalFormatting-GetWorksheetConditionalFormatting-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "b2a10009556f14d1f939a8433925c5f6" >}}

{{< /tab >}}

{{< /tabs >}}