---
title: "添加格式条件"
type: docs
url: /zh/conditional-formattings/add-format-condition/
aliases: [  /zh/add-a-format-condition/ ]
keywords: "Aspose.Cells Cloud, 条件格式 API, 添加格式条件, Excel REST API, Cells API"
description: "了解如何使用 Aspose.Cells Cloud REST API（v3.0）向 Excel 工作表添加格式条件。包括请求语法、参数、安全的 cURL 示例和 SDK 代码片段。"
ArticleTitle: "添加格式条件 – Aspose.Cells Cloud API 文档"
weight: 50
---

此 REST API 可向工作表添加格式条件。

## 安全与身份验证
Aspose.Cells Cloud API 是安全的，需要基于 [JWT 令牌的身份验证](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)。

## REST API

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}
```

### 请求参数

| 参数名称   | 类型    | 位置   | 描述                                                         |
| ---------- | ------- | ------ | ------------------------------------------------------------ |
| name       | string  | path   | Excel 工作簿的名称。                                         |
| sheetName  | string  | path   | 包含要设置格式区域的工作表名称。                             |
| index      | integer | path   | 要添加或替换的格式条件的从零开始的索引。                     |
| cellArea   | string  | query  | 条件适用的单元格区域（例如 `A1:C3`）。                       |
| type       | string  | query  | 条件类型（例如 `Expression`、`CellValue`）。                |
| operatorType | string  | query  | 条件运算符（例如 `Between`、`Equal`）。                     |
| formula1   | string  | query  | 条件使用的第一个公式或值。                                   |
| formula2   | string  | query  | 第二个公式或值（某些运算符如 `Between` 是必需的）。         |
| folder     | string  | query  | 存储中工作簿所在的文件夹。                                   |
| storageName | string  | query  | 存储服务的名称（例如 `Default`）。                          |

### 错误响应

| HTTP 状态码 | 原因                                   | 示例响应体                                                         |
| ----------- | -------------------------------------- | ------------------------------------------------------------------ |
| **400**     | 错误请求 – 缺少或无效的参数。          | `{ "Code":"400", "Message":"Invalid parameter value." }`            |
| **401**     | 未授权 – 缺少或无效的 JWT 令牌。       | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404**     | 未找到 – 工作簿或工作表不存在。        | `{ "Code":"404", "Message":"File not found." }`                     |
| **500**     | 内部服务器错误 – 意外的服务器故障。    | `{ "Code":"500", "Message":"An unexpected error occurred." }`       |

### 成功响应

| HTTP 状态码 | 原因                           | 示例响应体                            |
| ----------- | ------------------------------ | ------------------------------------- |
| **200**     | 成功 – 条件已添加或更新成功。  | `{ "Code": "200", "Status": "OK" }`   |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/ConditionalFormattings/PutWorksheetFormatCondition) 定义了一个公开可访问的编程接口，可让您直接从 Web 浏览器执行 REST 交互。

您可以使用 **cURL** 调用 Aspose.Cells API。以下示例展示了完整请求，包括空的 JSON 请求体。

### cURL 示例

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet1/conditionalFormattings/0?cellArea=A1:C3&type=Expression&operatorType=Between&formula1=v1&formula2=v2" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{}'
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

## 云 SDK 开发工具包系列

使用 SDK 是加快开发速度的最佳方式。SDK 处理底层细节，让您专注于项目任务。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ConditionalFormatting-AddFormatCondition-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-add-cells-area-for-format-condition.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-ConditionalFormatting-put_worksheet_format_condition-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-ConditionalFormatting-AddFormatCondition-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-ConditionalFormatting-AddFormatCondition-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "caa13d019b3c7c3b5c14110ccd217e99" >}}

{{< /tab >}}

{{< /tabs >}}