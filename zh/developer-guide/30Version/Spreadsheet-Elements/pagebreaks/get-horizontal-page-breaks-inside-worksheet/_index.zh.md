---
title: "获取水平分页符"
second_title: "文档"
linktitle: "获取水平分页符"
type: docs
url: /zh/page-breaks/get-horizontal-page-breaks/
aliases: [  /zh/get-horizontal-page-breaks-inside-worksheet/ ]
keywords: "水平分页符, Aspose.Cells Cloud, REST API, Excel 工作表, SDK"
description: "通过 Aspose.Cells Cloud API 从 Excel 工作表中检索水平分页符。包含端点、参数、cURL 示例、响应格式以及 C#、Java、Python 等多种语言的 SDK 代码片段。"
ArticleTitle: "获取水平分页符 - Aspose.Cells Cloud API 文档"
weight: 10
---

**水平分页符**——一种基于行的分页符，用于强制工作表在指定行之后开始新的打印页。此 REST API 用于检索这些水平分页符。

## 安全与身份验证

Aspose.Cells Cloud API 是安全的，需要基于 [JWT 令牌的身份验证](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)。

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/horizontalpagebreaks
```

### 请求参数

| 参数名        | 类型   | 位置   | 描述                                                    |
| ------------- | ------ | ------ | ------------------------------------------------------- |
| name          | string | path   | Excel 文件的名称。                                      |
| sheetName     | string | path   | 工作表的名称。                                          |
| folder        | string | query  | 存储中文件所在的文件夹路径。（可选）                   |
| storageName   | string | query  | 存储的名称。（可选）                                    |

<a href="https://apireference.aspose.cloud/cells/#/PageBreaks/GetHorizontalPageBreaks" rel="noopener" title="GetHorizontalPageBreaks 的 OpenAPI 规范">OpenAPI 规范</a> 定义了一个公开可访问的编程接口，允许您直接通过 Web 浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/horizontalpagebreaks" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "HorizontalPageBreaks": {
    "HorizontalPageBreakList": [
      {
        "Row": 6,
        "EndColumn": 16383,
        "StartColumn": 0
      }
    ],
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/HorizontalPageBreaks",
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

## 错误处理

| HTTP 状态码 | 描述                                     | 示例 JSON                                            |
| ----------- | ---------------------------------------- | ---------------------------------------------------- |
| 400         | 请求错误——缺少或无效的参数。             | `{ "Code": 400, "Message": "Invalid parameter." }`  |
| 401         | 未授权——JWT 令牌缺失或无效。             | `{ "Code": 401, "Message": "Authentication failed." }` |
| 404         | 未找到——指定的文件或工作表不存在。       | `{ "Code": 404, "Message": "Resource not found." }` |
| 500         | 服务器内部错误——服务器上出现意外情况。   | `{ "Code": 500, "Message": "Server error." }`       |

## 云 SDK 家族

使用 SDK 是加快开发速度的最佳方式。SDK 负责处理底层细节，让您专注于项目任务。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetHorizontalPageBreaks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetHorizontalPageBreaks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetHorizontalPageBreaks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetHorizontalPageBreaks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetHorizontalPageBreaks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetHorizontalPageBreaks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetHorizontalPageBreaks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetHorizontalPageBreaks.go" >}}

{{< /tab >}}

{{< /tabs >}}