---
title: "从 Excel 文件获取页数"
second_title: "文档"
linktitle: "页数"
type: docs
url: /zh/get-page-count-from-an-excel-file/
aliases: [  /zh/workbook/page-count/ , /zh/workbook/get/page-count/ ]
keywords: "Aspose.Cells, 云 API, Excel 页数, 工作簿分页"
description: "通过 Aspose.Cells Cloud REST API（v3.0）检索 Excel 工作簿中的可打印页总数。包含请求格式、必需参数、cURL 示例、响应模式、错误处理以及多种编程语言的 SDK 代码片段。"
weight: 10
version: "v3.0"
ArticleTitle: "使用 Aspose.Cells Cloud API 从 Excel 文件获取页数"
---

此 REST API 返回工作簿的**页数**。

## 安全与身份验证
Aspose.Cells Cloud API 是安全的，需要 [基于 JWT 令牌的身份验证](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)。

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/pagecount
```

### 请求参数

| 参数名称      | 类型   | 位置 | 必需 | 描述                             |
| ------------- | ------ | ---- | ---- | -------------------------------- |
| name          | string | path | 是   | Excel 文档的名称。               |
| folder        | string | query| 否   | 包含该文档的文件夹。             |
| storageName   | string | query| 否   | 要使用的存储空间的名称。         |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Workbook/GetPageCount) 定义了一个公开可访问的编程接口，允许您直接从网页浏览器中发起 REST 请求。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells REST API。以下示例展示了如何使用 cURL 调用该接口。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/YourFile.xlsx/pagecount" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

*请将 `YourFile.xlsx` 替换为您要查询的工作簿的实际文件名。*

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
13
```

{{< /tab >}}

{{< /tabs >}}

### 响应模式

| HTTP 状态码 | 数据类型 | 描述                                       |
| ----------- | -------- | ------------------------------------------ |
| 200         | integer  | 工作簿中的可打印页总数（例如 `13`）。     |
| 4xx‑5xx     | JSON     | 错误对象（参见“错误处理”部分）。           |

## 云 SDK 家族

使用 SDK 是加快开发速度的最佳方式。SDK 负责处理底层细节，让您专注于项目本身的任务。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetPageCount.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetPageCount.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetPageCount.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetPageCount.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82deb2e4189bc27ae92abf73c36b4df0" "Example_GetPageCount.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetPageCount.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetPageCount.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetPageCount.go" >}}

{{< /tab >}}

{{< /tabs >}}

## 错误处理

| HTTP 状态码 | 描述                         | 示例 JSON 正文                                                                 |
| ----------- | ---------------------------- | ------------------------------------------------------------------------------ |
| 401         | JWT 令牌无效或缺失。         | `{ "Code": "InvalidAuthenticationToken", "Message": "Access token is missing or invalid." }` |
| 404         | 未找到指定的工作簿。         | `{ "Code": "FileNotFound", "Message": "The requested file does not exist." }`                |
| 400         | 请求错误 — 缺少必需参数。    | `{ "Code": "BadRequest", "Message": "Required parameter 'name' is missing." }`               |
| 500         | 服务器内部错误。             | `{ "Code": "InternalError", "Message": "An unexpected error occurred." }`                    |