---
title: "添加水平分页符"
second_title: "文档"
linktitle: "添加水平分页符"
type: docs
url: /page-breaks/add-horizontal-page-break/
aliases: [/insert-horizontal-page-break-inside-worksheet/]
keywords: "水平分页符, Aspose.Cells Cloud, Excel API, REST, SDK, 工作表, cURL"
description: "了解如何使用 Aspose.Cells Cloud REST API 为 Excel 工作表添加水平分页符。包含请求详情、cURL 示例以及多种编程语言的 SDK 代码片段。"
weight: 30
ArticleTitle: "添加水平分页符 – Aspose.Cells Cloud API"
---

**添加水平分页符** API 可向 Excel 工作表中插入水平分页符。

**先决条件与身份验证**  
调用 Aspose.Cells Cloud API 前，必须提供有效的 JWT 令牌。请参考[身份验证指南](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)中所述的 OAuth 2.0 流程获取该令牌，并将其以 `Authorization: Bearer <jwt token>` 格式添加至请求头中。目标工作簿必须存放在 API 可访问的存储位置（默认存储或您指定的自定义 `storageName` 存储）。

## PutHorizontalPageBreak API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/horizontalpagebreaks
```

### **安全性与身份验证**

Aspose.Cells Cloud API 采用安全机制，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

### 请求参数

| 参数名        | 类型    | 位置   | 描述                                                                 |
| ------------- | ------- | ------ | -------------------------------------------------------------------- |
| name          | string  | path   | Excel 文件名。                                                       |
| sheetName     | string  | path   | 将添加分页符的工作表名称。                                           |
| cellname      | string  | query  | 标记分页符起始位置的单元格引用（例如 **A1**）。                      |
| row           | integer | query  | 分页符的从零开始的行索引。                                           |
| column        | integer | query  | 分页符的从零开始的列索引。                                           |
| startColumn   | integer | query  | 插入分页符时所选范围的起始列。                                       |
| endColumn     | integer | query  | 插入分页符时所选范围的结束列。                                       |
| folder        | string  | query  | 包含 Excel 文件的文件夹路径。                                        |
| storageName   | string  | query  | Aspose Cloud 存储名称。                                              |

<a href="https://apireference.aspose.cloud/cells/#/PageBreaks/PutHorizontalPageBreak" target="_blank" rel="noopener noreferrer">OpenAPI 规范</a> 定义了一个公开可访问的接口，使您能直接通过网页浏览器执行 REST 交互。

您可使用 **cURL** 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何通过 cURL 调用该 API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
# 使用 HTTPS 以确保通信加密
curl -v "https://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/horizontalpagebreaks?row=18" \
  -X PUT \
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

当 JWT 令牌缺失或无效时的错误响应示例：

```json
{
  "Code": 401,
  "Status": "Unauthorized",
  "Message": "无效或缺失的 JWT 令牌。"
}
```

**HTTP 状态码**

| 状态码 | 含义           | 描述                                           |
| ------ | -------------- | ---------------------------------------------- |
| 200    | OK（成功）     | 分页符添加成功；响应包含操作详情。             |
| 400    | Bad Request（错误请求） | 请求参数缺失或无效（例如，不支持的文件类型）。 |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                           |
| 413    | Payload Too Large（请求实体过大） | 上传文件超出大小限制。                        |
| 500    | Internal Server Error（内部服务器错误） | 服务器发生意外错误。                          |

有关相关操作的更多详情，请参阅 **[获取水平分页符](../get-horizontal-page-breaks/)** 和 **[删除水平分页符](../delete-horizontal-page-break/)** 的 API 页面。

## 云 SDK 开发套件

使用 SDK 是最快捷的开发方式。SDK 抽象了底层细节，让您能专注于项目本身。请查看 <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub 仓库</a>，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutHorizontalPageBreak.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutHorizontalPageBreak.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutHorizontalPageBreak.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutHorizontalPageBreak.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutHorizontalPageBreak.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutHorizontalPageBreak.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutHorizontalPageBreak.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutHorizontalPageBreak.go" >}}
{{< /tab >}}

{{< /tabs >}}