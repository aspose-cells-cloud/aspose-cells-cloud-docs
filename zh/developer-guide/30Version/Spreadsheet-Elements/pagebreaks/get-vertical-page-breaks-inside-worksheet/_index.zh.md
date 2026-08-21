---
title: "获取垂直分页符"
second_title: "文档"
linktitle: "获取垂直分页符"
type: docs
url: /page-breaks/get-vertical-page-breaks/
aliases: [/get-vertical-page-breaks-inside-worksheet/]
keywords: "Aspose.Cells, 垂直分页符, Excel API, 云电子表格, REST API"
description: "使用 Aspose.Cells Cloud REST API（v3.0）从 Excel 工作表中检索垂直分页符。包含 HTTPS 端点、必需参数、cURL 示例、响应详情、错误处理及 SDK 示例。"
weight: 20
---

此 REST API 用于从工作表中获取**垂直**分页符。

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/verticalpagebreaks
```

### 请求参数

| 参数名称       | 类型   | 位置 | 描述                                               | 是否必需 |
| -------------- | ------ | ---- | -------------------------------------------------- | -------- |
| `name`         | string | path | Excel 文件的名称。                                 | 是       |
| `sheetName`    | string | path | 要从中读取分页符的工作表名称。                     | 是       |
| `folder`       | string | query| 存储中包含该文件的文件夹。                         | 否       |
| `storageName`  | string | query| 要使用的 Aspose Cloud 存储名称。                   | 否       |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/PageBreaks/GetVerticalPageBreaks) 定义了一个公开可用的编程接口，可让您直接从 Web 浏览器执行 REST 交互。

您可以使用 **cURL** 轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用云 API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/verticalpagebreaks" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "VerticalPageBreaks": {
    "VerticalPageBreakList": [
      {
        "Column": 3,
        "EndRow": 1048575,
        "StartRow": 0
      }
    ],
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/VerticalPageBreaks",
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

### 响应详情

| 字段                    | 类型   | 描述                                                                    |
| ----------------------- | ------ | ----------------------------------------------------------------------- |
| `VerticalPageBreakList` | array  | 垂直分页符对象集合。                                                    |
| `Column`                | int    | 分页符发生的列索引（从 0 开始）。                                       |
| `StartRow`              | int    | 分页范围的第一行（从 0 开始）。                                         |
| `EndRow`                | int    | 分页范围的最后一行（从 0 开始，通常为 `1048575`，代表最后一行）。     |
| `link.Href`             | string | 资源的自引用 URL（HTTPS）。                                             |
| `Code`                  | int    | 服务返回的 HTTP 状态码。                                                |
| `Status`                | string | HTTP 状态的文字描述。                                                   |

### 错误处理

| HTTP 状态码 | 含义         | 常见原因                       |
| ----------- | ------------ | ------------------------------ |
| 401         | 未授权       | 缺失或无效的 JWT 令牌。        |
| 404         | 未找到       | 指定的文件或工作表不存在。     |
| 400         | 请求错误     | 查询参数无效或格式错误。       |
| 500         | 服务器内部错误 | 服务器端意外情况。             |

请检查 JSON 响应中的 `Code` 和 `Status` 字段以获取更多详细信息。

## 云 SDK 家族

使用 SDK 是开发 Aspose.Cells Cloud 应用的最快方式。SDK 抽象了底层细节，让您能专注于业务逻辑。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetVerticalPageBreaks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetVerticalPageBreaks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetVerticalPageBreaks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetVerticalPageBreaks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetVerticalPageBreaks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetVerticalPageBreaks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetVerticalPageBreaks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetVerticalPageBreaks.go" >}}

{{< /tab >}}

{{< /tabs >}}