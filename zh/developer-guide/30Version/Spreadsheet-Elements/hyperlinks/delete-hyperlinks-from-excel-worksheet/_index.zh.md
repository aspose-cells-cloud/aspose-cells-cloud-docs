---
title: "清除超链接"
type: docs
url: /zh/hyperlinks/clear/
aliases: [  /zh/add-hyperlinks-to-excel-worksheet/ ]
keywords: "Aspose.Cells Cloud, Excel, 清除超链接, 删除超链接, REST API, 工作表, SDK"
description: "了解如何使用 Aspose.Cells Cloud REST API 或任意支持的 SDK（C#、Java、Python、Node.js、Go、PHP、Ruby、Perl 等）从 Excel 工作表中移除所有超链接。"
weight: 40
ArticleTitle: "清除超链接 – Aspose.Cells Cloud API 文档"
---

此 REST API 用于删除 Excel 工作表上的**所有超链接**。

## 安全性与身份验证
Aspose.Cells Cloud API 采用安全机制，需要基于 [JWT 令牌的身份验证](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)。

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks
```

### 请求参数

| 参数名称      | 类型   | 位置   | 描述                             |
| ------------- | ------ | ------ | -------------------------------- |
| name          | string | path   | Excel 文件的名称。               |
| sheetName     | string | path   | 工作表的名称。                   |
| folder        | string | query  | 包含文档的文件夹。               |
| storageName   | string | query  | 存储服务的名称。                 |

### 错误响应

| HTTP 状态码 | 原因                                         | 示例响应体                                                             |
| ----------- | -------------------------------------------- | ---------------------------------------------------------------------- |
| **400**     | 请求无效 — 缺少或参数值非法。                | `{ "Code":"400", "Message":"Invalid parameter value." }`              |
| **401**     | 未授权 — 缺少或 JWT 令牌无效。               | `{ "Code":"401", "Message":"Access token is missing or invalid." }`  |
| **404**     | 未找到 — 工作簿或工作表不存在。              | `{ "Code":"404", "Message":"File not found." }`                       |
| **500**     | 内部服务器错误 — 服务器发生意外错误。        | `{ "Code":"500", "Message":"An unexpected error occurred." }`        |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Hyperlinks/DeleteWorksheetHyperlinks) 定义了一个公开可访问的编程接口，允许您直接从 Web 浏览器发起 REST 调用。

您可使用 **cURL** 命令行工具调用 Aspose.Cells 网络服务。以下示例展示了如何删除工作表中的所有超链接：

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test1.xlsx/worksheets/Sheet1/hyperlinks" \
  -X DELETE \
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

## 云 SDK 家族

使用 SDK 可加快开发速度，SDK 会自动处理底层细节。如需查看 Aspose.Cells Cloud SDK 的完整列表，请访问 [GitHub 仓库](https://github.com/aspose-cells-cloud)。

以下代码示例展示了如何使用多种 SDK 删除工作表超链接：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetHyperlinks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetHyperlinks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetHyperlinks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetHyperlinks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetHyperlinks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetHyperlinks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetHyperlinks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetHyperlinks.go" >}}

{{< /tab >}}

{{< /tabs >}}