---
title: "获取工作表超链接"
type: docs
url: /hyperlinks/get/
keywords: "Aspose.Cells Cloud, 获取工作表超链接, Excel 超链接 API, REST, JWT 身份验证, Excel 工作表, API 端点"
description: "使用 Aspose.Cells Cloud API (v3.0) 从 Excel 工作表中检索特定超链接。包含端点、参数、cURL 示例、身份验证详情、错误处理及 SDK 代码片段。"
weight: 10
ArticleTitle: "Aspose.Cells Cloud API – 获取工作表超链接"
---

此 REST API 通过 **Aspose.Cells 获取超链接 API** 检索工作表中的**超链接**。

## 安全与身份验证

Aspose.Cells Cloud API 采用安全机制，需使用 [基于 JWT 令牌的身份验证](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)。  
调用端点前，请使用您的客户端 ID 和密钥获取 JWT 访问令牌，并将其包含在 `Authorization: Bearer <jwt token>` 请求头中。

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks/{hyperlinkIndex}
```

### 请求参数

| 参数名称        | 类型    | 位置   | 描述                           |
| --------------- | ------- | ------ | ------------------------------ |
| name            | string  | path   | Excel 文件名称。               |
| sheetName       | string  | path   | 包含超链接的工作表名称。       |
| hyperlinkIndex  | integer | path   | 待检索超链接的从零开始的索引。 |
| folder          | string  | query  | 文档所在文件夹。               |
| storageName     | string  | query  | 存储服务的名称。               |

### 错误响应

| HTTP 状态码 | 原因说明                               | 示例响应体                                                         |
| ----------- | -------------------------------------- | ------------------------------------------------------------------ |
| **400**     | 请求错误 — 缺少或无效的参数。          | `{ "Code":"400", "Message":"Invalid parameter value." }`          |
| **401**     | 未授权 — 缺少或无效的 JWT 令牌。       | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404**     | 未找到 — 工作簿或工作表不存在。        | `{ "Code":"404", "Message":"File not found." }`                   |
| **500**     | 服务器内部错误 — 发生意外服务器故障。  | `{ "Code":"500", "Message":"An unexpected error occurred." }`     |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Hyperlinks/GetWorksheetHyperlink) 定义了一个公开可访问的编程接口，允许您直接通过 Web 浏览器发起 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用云 API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/hyperlinks/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Hyperlink": {
    "Address": "https://docs.aspose.cloud/display/cellscloud/Get+Hyperlink+from+Excel+Worksheet",
    "Area": {
      "EndColumn": 0,
      "EndRow": 1,
      "StartColumn": 0,
      "StartRow": 1
    },
    "ScreenTip": null,
    "TextToDisplay": "https://docs.aspose.cloud/display/cellscloud/Get+Hyperlink+from+Excel+Worksheet",
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet1/hyperlinks/1",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## 云 SDK 家族

使用 SDK 是加快开发速度的最佳方式。SDK 负责处理底层细节，使您能够专注于项目任务。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，查看 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetHyperlink.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetHyperlink.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetHyperlink.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetHyperlink.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetHyperlink.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetHyperlink.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetHyperlink.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetHyperlink.go" >}}

{{< /tab >}}

{{< /tabs >}}