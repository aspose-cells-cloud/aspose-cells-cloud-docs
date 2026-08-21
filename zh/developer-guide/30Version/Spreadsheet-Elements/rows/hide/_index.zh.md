---
title: "隐藏 Excel 工作表中的行"
second_title: "文档"
linktitle: "隐藏"
type: docs
url: /zh/rows/hide/
aliases: [  /zh/hide-rows-in-excel-worksheet/ ]
keywords: "隐藏行, Aspose.Cells Cloud, Excel API, REST, SDK"
description: "了解如何使用 Aspose.Cells Cloud REST API 隐藏 Excel 工作表中的一行或多行。包含 cURL 示例、SDK 代码片段、参数说明、身份验证方式、响应详情及错误处理。"
weight: 40
ArticleTitle: "使用 Aspose.Cells Cloud API 在 Excel 工作表中隐藏行"
---

此 REST API 可用于隐藏 Excel 工作表中的行。

**前置条件**：已从 Aspose Cloud OAuth 端点获取有效的 JWT Bearer 令牌；工作簿已存储于 Aspose Cloud 存储中；并已知包含待隐藏行的工作表名称。该 API 支持 XLS、XLSX 及其他受支持格式的 Excel 文件。

## PostHideWorksheetRows API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/hide
```

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数

| 参数名          | 类型    | 位置   | 描述                                                           |
| --------------- | ------- | ------ | -------------------------------------------------------------- |
| **name**        | string  | path   | 工作簿文件的名称。                                             |
| **sheetName**   | string  | path   | 包含待隐藏行的工作表名称。                                     |
| **startrow**    | integer | query  | 待隐藏首行的从零开始的索引。                                   |
| **totalRows**   | integer | query  | 从 **startrow** 开始连续隐藏的行数。                           |
| **folder**      | string  | query  | 工作簿所在的存储文件夹路径。                                   |
| **storageName** | string  | query  | 存储服务的名称。                                               |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Cells/PostHideWorksheetRows) 提供了一个公开可访问的编程接口，可让您直接通过网页浏览器执行 REST 交互。

您可以使用 **cURL** 命令行工具调用 Aspose.Cells Web 服务。该 API 要求提供从 Aspose Cloud OAuth 端点获取的 JWT Bearer 令牌，并将其包含在 `Authorization` 请求头中。以下示例演示了如何使用 cURL 隐藏一行。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/hide?startrow=1&totalRows=1" \
  -X POST \
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

**响应状态码**

| 状态码 | 描述                           |
|--------|--------------------------------|
| 200    | 成功 — 行已隐藏                |
| 400    | 错误请求 — 参数无效             |
| 401    | 未授权 — 缺失或无效的 JWT 令牌 |
| 404    | 未找到 — 工作簿或工作表不存在   |
| 500    | 服务器错误 — 内部处理失败       |

成功调用后返回的 JSON 对象包含 `Code` 和 `Status` 字段。发生错误时，响应中会包含额外字段，例如 `Message` 以及相应的 HTTP 状态码（如 400、401、404、500）。

**注意事项**：请确保 `startrow` 值在工作表的行范围内；否则 API 将返回 400 错误。行索引为从零开始，因此 `startrow=0` 表示第一行。

## 云 SDK 家族

使用 SDK 是将此功能快速集成到您应用程序中的最高效方式。SDK 处理底层细节，让您专注于业务逻辑。请参阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 隐藏行。（示例文件名中提及 “Unhide” 是由于历史命名原因；每个代码片段内部实际执行的是 **隐藏** 操作。）

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUnhideWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUnhideWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUnhideWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUnhideWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUnhideWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUnhideWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUnhideWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUnhideWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}