---
title: "添加垂直分页符"
second_title: "文档"
linktitle: "添加垂直分页符"
type: docs
url: /page-breaks/add-vertical-page-break/
aliases: [/insert-vertical-page-break-inside-worksheet/]
keywords: "Aspose.Cells Cloud、垂直分页符、REST API、Excel、SDK、cURL"
description: "了解如何使用 Aspose.Cells Cloud REST API（v3.0）在 Excel 工作表中插入垂直分页符。包含请求语法、cURL 示例、SDK 示例、身份验证指南及错误处理详细信息。"
weight: 40
ArticleTitle: "添加垂直分页符 – Aspose.Cells Cloud API"
---

此 REST API 可在工作表中插入垂直分页符。

## 安全性与身份验证
Aspose.Cells Cloud API 安全可靠，需采用 [基于 JWT 令牌的身份验证](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)。

## REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/verticalpagebreaks
```

### 请求参数

| 参数名称   | 类型    | 位置   | 描述                                                         |
|------------|---------|--------|--------------------------------------------------------------|
| name       | string  | path   | Excel 工作簿的名称。                                         |
| sheetName  | string  | path   | 将添加分页符的工作表名称。                                   |
| cellname   | string  | query  | 定义分页符位置的单元格引用（例如 **A1**）。                  |
| column     | integer | query  | 分页符起始列的从零开始的索引。                               |
| row        | integer | query  | 分页符起始行的从零开始的索引。                               |
| startRow   | integer | query  | 分页符范围的第一行。                                         |
| endRow     | integer | query  | 分页符范围的最后一行。                                       |
| folder     | string  | query  | 工作簿所在存储空间的文件夹路径。                             |
| storageName| string  | query  | 存储服务的名称。                                             |

**必需参数**：必须提供 `cellname` **或** `column`。当使用 `column` 时，还可提供 `row`、`startRow` 和 `endRow` 来定义一个范围。其余字段均为可选。

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/PageBreaks/PutVerticalPageBreak) 定义了一个公开可访问的编程接口，可让您直接通过 Web 浏览器发起 REST 请求。

### cURL 示例

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/SampleBreaks.xlsx/worksheets/Sheet1/verticalpagebreaks?column=9" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

#### 响应

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**HTTP 状态码**

| 状态码 | 含义           | 描述                                                         |
|--------|----------------|--------------------------------------------------------------|
| 200    | OK（成功）     | 分页符插入成功；响应包含操作详细信息。                       |
| 400    | Bad Request（错误请求） | 缺失或无效的参数（例如不支持的文件类型）。                   |
| 401    | Unauthorized（未授权）  | JWT 令牌无效或缺失。                                         |
| 413    | Payload Too Large（请求实体过大） | 上传文件超出大小限制。                                     |
| 500    | Internal Server Error（服务器内部错误） | 服务器发生意外错误。                                     |

## 云 SDK 开发工具包（SDK Family）

使用 SDK 是加速开发的最佳方式。SDK 负责处理底层细节，使您能专注于项目任务。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutVerticalPageBreak.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutVerticalPageBreak.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutVerticalPageBreak.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutVerticalPageBreak.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutVerticalPageBreak.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutVerticalPageBreak.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutVerticalPageBreak.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutVerticalPageBreak.go" >}}

{{< /tab >}}

{{< /tabs >}}