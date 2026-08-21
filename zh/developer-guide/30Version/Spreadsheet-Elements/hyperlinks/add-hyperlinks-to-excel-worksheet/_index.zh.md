---
title: "向工作表添加超链接"
type: docs
url: /zh/hyperlinks/add/
aliases: [  /zh/add-hyperlinks-to-excel-worksheet/ ]
keywords: "Aspose.Cells, 添加超链接, Excel REST API, 云 SDK"
description: "了解如何使用 Aspose.Cells Cloud v3.0 REST API 向 Excel 工作表添加超链接。包含端点、完整参数说明、cURL 示例以及 C#、Java、Python 等语言的 SDK 代码片段。"
weight: 20
---

此 REST API 用于向 Excel 工作表添加超链接。

## REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks
```

### 请求参数

| 参数名称       | 类型    | 位置   | 描述                                                         |
| -------------- | ------- | ------ | ------------------------------------------------------------ |
| name           | string  | path   | 文档名称。                                                   |
| sheetName      | string  | path   | 工作表名称。                                                 |
| firstRow       | integer | query  | 超链接所应用范围的起始行索引（从 0 开始）。                  |
| firstColumn    | integer | query  | 超链接所应用范围的起始列索引（从 0 开始）。                  |
| totalRows      | integer | query  | 超链接范围所跨越的行数。                                     |
| totalColumns   | integer | query  | 超链接范围所跨越的列数。                                     |
| address        | string  | query  | 超链接指向的目标 URL（需进行 URL 编码）。                    |
| folder         | string  | query  | 文档所在文件夹。                                             |
| storageName    | string  | query  | 存储名称。                                                   |

请求体中也可包含相同的字段（`Address`、`FirstRow`、`FirstColumn`、`TotalRows`、`TotalColumns`）的 JSON 数据。当您更倾向于使用请求体而非查询参数时，可采用此方式。

### 错误响应

| HTTP 状态码 | 原因                                       | 示例响应体                                                          |
| ----------- | ------------------------------------------ | ------------------------------------------------------------------- |
| **400**     | 请求错误 — 缺少或无效的参数。              | `{ "Code":"400", "Message":"Invalid parameter value." }`            |
| **401**     | 未授权 — 缺少或无效的 JWT 令牌。           | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404**     | 未找到 — 工作簿或工作表不存在。            | `{ "Code":"404", "Message":"File not found." }`                     |
| **500**     | 服务器内部错误 — 发生意外的服务器故障。    | `{ "Code":"500", "Message":"An unexpected error occurred." }`       |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Hypelinks/PutWorksheetHyperlink) 定义了一个公开可访问的编程接口，您可直接在 Web 浏览器中发起 REST 请求。

您可使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用云 API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/hyperlinks?firstRow=1&firstColumn=6&totalRows=1&totalColumns=1&address=https%3A%2F%2Fwww.msnbc.com%2F" \
-X PUT \
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

若请求失败，API 将返回标准的 HTTP 错误状态码（如 400 请求错误、401 未授权、404 未找到、500 服务器内部错误），并附带包含错误信息和错误码的 JSON 响应体。

## 云 SDK 家族

使用 SDK 是开发速度最快的方式。SDK 负责处理底层细节，使您能专注于项目任务本身。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetHyperlink.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetHyperlink.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetHyperlink.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetHyperlink.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetHyperlink.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetHyperlink.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetHyperlink.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetHyperlink.go" >}}

{{< /tab >}}

{{< /tabs >}}