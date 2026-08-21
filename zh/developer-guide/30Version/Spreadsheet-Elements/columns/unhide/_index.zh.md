---
title: "取消隐藏 Excel 工作表中的列"
ArticleTitle: "取消隐藏 Excel 工作表中的列 - Aspose.Cells Cloud API"
second_title: "文档"
linktitle: "取消隐藏"
type: docs
url: /zh/columns/unhide/
aliases:
  [/unhide-columns-in-an-excel-worksheet/, /unhide-columns-in-excel-worksheet/]
keywords: "Aspose.Cells, 云 API, 取消隐藏列, Excel, REST, SDK"
description: "了解如何使用 Aspose.Cells Cloud REST API 取消隐藏 Excel 工作表中的列。包含请求详情、cURL 示例以及多种编程语言的 SDK 代码示例。"
weight: 50
---

此 REST API 用于取消隐藏工作表中的列。

**前置条件** – 所有 Aspose.Cells Cloud 端点均需通过 HTTPS 访问，并提供有效的 OAuth 2.0 访问令牌。请确保您已获取访问令牌，并将其包含在请求的 `Authorization` 头中。

## PostUnhideWorksheetColumns API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/unhide
```

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，需进行 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称       | 类型    | 位置   | 描述                                     |
| -------------- | ------- | ------ | ---------------------------------------- |
| name           | string  | path   | 工作簿名称。                             |
| sheetName      | string  | path   | 工作表名称。                             |
| startColumn    | integer | query  | 要处理的第一列的索引。                   |
| totalColumns   | integer | query  | 要处理的列数。                           |
| width          | number  | query  | 目标列宽（默认值 = 50.0）。              |
| folder         | string  | query  | 包含文档的文件夹。                       |
| storageName    | string  | query  | 存储服务的名称。                         |

<a href="https://apireference.aspose.cloud/cells/#/Cells/PostUnhideWorksheetColumns" target="_blank" rel="noopener noreferrer">OpenAPI 规范</a> 定义了一个公开可访问的编程接口，允许您直接从 Web 浏览器发起 REST 请求。

您可使用 **cURL** 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/unhide?startColumn=1&totalColumns=1&width=15" -H "accept: application/json"
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

**典型 HTTP 状态码**

| 状态码 | 描述                                     |
|--------|------------------------------------------|
| 200    | OK（成功）——列已成功取消隐藏。           |
| 400    | Bad Request（错误请求）——参数无效。      |
| 401    | Unauthorized（未授权）——缺少或令牌无效。 |
| 404    | Not Found（未找到）——工作簿或工作表不存在。 |
| 500    | Internal Server Error（内部服务器错误）——发生意外错误。 |

## 云 SDK 开发工具包（SDK Family）

使用 SDK 是加快开发速度的最佳方式。SDK 负责处理底层细节，使您能专注于项目任务本身。请查看 <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub 仓库</a> 以获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUnhideWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUnhideWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUnhideWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUnhideWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUnhideWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUnhideWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUnhideWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUnhideWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}