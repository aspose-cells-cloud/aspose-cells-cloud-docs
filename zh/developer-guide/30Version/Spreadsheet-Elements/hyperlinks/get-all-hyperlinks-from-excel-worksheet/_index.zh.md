---
title: "获取所有超链接 – Aspose.Cells Cloud REST API"
type: docs
url: /hyperlinks/get-all/
aliases:
  [/get-hyperlink-from-excel-worksheet/, /get-hyperlinks-from-excel-worksheet/]
keywords: "Aspose.Cells, 获取所有超链接, Excel API, REST API, 云 SDK, cURL 示例, 电子表格超链接"
description: "使用 Aspose.Cells Cloud REST API（v3.0）从 Excel 文件的工作表中检索所有超链接。包含 HTTPS 端点、必需参数、cURL 示例、响应模式及 SDK 代码示例。"
weight: 10
ArticleTitle: "获取所有超链接 – Aspose.Cells Cloud REST API 文档"
---

此 REST API 可从 Excel 工作簿中的指定工作表中检索**所有超链接**。

## 安全与身份验证

Aspose.Cells Cloud API 采用安全机制，需使用 [基于 JWT 令牌的身份验证](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)。

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks
```

### 请求参数

| 参数名        | 类型   | 位置   | 是否必需 | 默认值 | 描述                           |
| ------------- | ------ | ------ | -------- | ------ | ------------------------------ |
| name          | string | path   | 是       | –      | Excel 文档的名称。             |
| sheetName     | string | path   | 是       | –      | 工作表的名称。                 |
| folder        | string | query  | 否       | –      | 包含该文档的文件夹。           |
| storageName   | string | query  | 否       | –      | 要使用的存储服务的名称。       |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Hyperlinks/GetWorksheetHyperlinks) 定义了一个公开可访问的编程接口，支持您直接通过网页浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用该 API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/hyperlinks" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Hyperlinks": {
    "Count": 4,
    "HyperlinkList": [
      {
        "link": {
          "Href": "/0",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "link": {
          "Href": "/1",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "link": {
          "Href": "/2",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "link": {
          "Href": "/3",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      }
    ],
    "link": null
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

JSON 响应中包含一个 `Hyperlinks` 对象：

- **Count** – 工作表中超链接的总数。
- **HyperlinkList** – 一个数组，其中每一项包含一个 `link` 对象。`Href` 属性存储超链接地址，`Rel`、`Title` 和 `Type` 提供额外元数据（对于简单链接通常为 `null`）。

### 错误响应

| HTTP 状态码 | 原因                                       | 示例响应体                                                          |
| ----------- | ------------------------------------------ | ------------------------------------------------------------------- |
| **400**     | 请求错误 – 参数缺失或无效。                | `{ "Code":"400", "Message":"Invalid parameter value." }`            |
| **401**     | 未授权 – 缺失或无效的 JWT 令牌。           | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404**     | 未找到 – 工作簿或工作表不存在。            | `{ "Code":"404", "Message":"File not found." }`                     |
| **500**     | 服务器内部错误 – 意外的服务器故障。        | `{ "Code":"500", "Message":"An unexpected error occurred." }`       |

## 云 SDK 产品族

使用 SDK 是集成该功能的最快方式。SDK 负责处理底层细节，使您能够专注于业务逻辑。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud) 获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同语言的 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetHyperlinks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetHyperlinks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetHyperlinks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetHyperlinks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetHyperlinks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetHyperlinks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetHyperlinks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetHyperlinks.go" >}}

{{< /tab >}}

{{< /tabs >}}