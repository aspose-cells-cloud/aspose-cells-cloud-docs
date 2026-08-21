---
title: "删除水平分页符"
ArticleTitle: "Aspose.Cells Cloud – 删除水平分页符（REST API）"
second_title: "文档"
linktitle: "删除水平分页符"
type: docs
url: /page-breaks/delete-horizontal-page-break/
aliases: [/delete-horizontal-page-break-inside-worksheet/]
keywords: "Aspose.Cells Cloud, 删除水平分页符, Excel 工作表, REST API, SDK"
description: "使用 Aspose.Cells Cloud REST API 从 Excel 工作表中删除水平分页符。提供 C#、Java、PHP、Ruby、Node.js、Python、Perl、Go 的 SDK。"
weight: 50
---

此 REST API 用于删除**水平**分页符。

**前提条件**：调用此接口前，您必须拥有有效的 Aspose Cloud JWT 访问令牌。请参考[身份验证指南](https://docs.aspose.cloud/cells/authentication/)获取令牌。

## DeleteHorizontalPageBreak API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/horizontalpagebreaks/{index}
```

*所有 API 调用必须通过 **HTTPS** 进行。*

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，需使用基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

### 请求参数

| 参数名        | 类型    | 位置   | 描述                                             |
| ------------- | ------- | ------ | ------------------------------------------------ |
| `name`        | string  | 路径   | Excel 文件（工作簿）的名称。                     |
| `sheetName`   | string  | 路径   | 包含分页符的工作表名称。                         |
| `index`       | integer | 路径   | 要删除的水平分页符的从零开始的索引。             |
| `folder`      | string  | 查询   | 可选，文件所在存储空间的文件夹路径。             |
| `storageName` | string  | 查询   | 可选，存储服务的名称。                           |

### 错误响应

| HTTP 状态码 | 描述                                                         |
| ----------- | ------------------------------------------------------------ |
| 401         | 未授权 — 缺少或无效的令牌。                                  |
| 404         | 未找到 — 指定的文件、工作表或分页符索引不存在。              |
| 400         | 错误请求 — 请求语法格式错误或参数无效。                      |
| 500         | 内部服务器错误 — 遇到意外情况。                              |

**另请参阅**：  
- [添加水平分页符](/page-breaks/add-horizontal-page-break/)  
- [获取水平分页符](/page-breaks/get-horizontal-page-breaks/)  
- [删除垂直分页符](/page-breaks/delete-vertical-page-break/)

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/PageBreaks/DeleteHorizontalPageBreak) 定义了一个公开可访问的编程接口，允许您直接从 Web 浏览器执行 REST 交互。

您可以使用 **cURL** 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 发起调用。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet1/horizontalpagebreaks/0" \
  -X DELETE \
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

**响应模式（Schema）**

| 字段    | 类型    | 描述                         |
|---------|---------|------------------------------|
| Code    | integer | HTTP 状态码（例如 200）。    |
| Status  | string  | 状态的文本描述（例如 "OK"）。|
| Message | string  | 可选，错误情况下的附加信息。 |

{{< /tab >}}

{{< /tabs >}}

## 云 SDK 开发工具包

使用 SDK 是加速开发的最佳方式。SDK 负责处理底层细节，使您能够专注于项目核心任务。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同语言的 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteHorizontalPageBreak.cs" >}}
*若示例加载失败，请在 [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/8a5b324fdf3e574dbd747c1a1e24b05d) 中查看。*

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteHorizontalPageBreak.java" >}}
*若示例加载失败，请在 [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/c59aa5c02f735466a5e34751cee73f5f) 中查看。*

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteHorizontalPageBreak.php" >}}
*若示例加载失败，请在 [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/84283c8ba766ed815f47e6dfb0891152) 中查看。*

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteHorizontalPageBreak.rb" >}}
*若示例加载失败，请在 [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/36ed8b8727561b92692939513d365fca) 中查看。*

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteHorizontalPageBreak.ts" >}}
*若示例加载失败，请在 [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/e82de2e4189bc27ae92abf73c36b4df0) 中查看。*

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteHorizontalPageBreak.py" >}}
*若示例加载失败，请在 [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/61e922de11e6e7144db88adcad6501c1) 中查看。*

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteHorizontalPageBreak.pl" >}}
*若示例加载失败，请在 [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/f82a3a00251e34ff8766116282c8c9ca) 中查看。*

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteHorizontalPageBreak.go" >}}
*若示例加载失败，请在 [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/2b824d4e13644368d12682856aa49185) 中查看。*

{{< /tab >}}

{{< /tabs >}}