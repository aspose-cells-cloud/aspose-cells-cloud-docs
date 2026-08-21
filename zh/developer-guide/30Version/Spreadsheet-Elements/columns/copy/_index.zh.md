---
title: "在 Excel 工作表中复制列"
second_title: "文档"
linktype: "复制"
type: docs
url: /columns/copy/
aliases:
  [/copy-columns-in-excel-worksheet/, /copy-columns-in-an-excel-worksheet/]
keywords: "Aspose.Cells, 复制列, Excel API, REST, 云 SDK, cURL, C#, Java, Python, Ruby, Node.js, Go, Perl"
description: "了解如何使用 Aspose.Cells Cloud REST API（v3.0）在 Excel 工作表中复制一个或多个列。包含请求语法、所需参数、身份验证详情、错误处理以及 C#、Java、Python、Ruby、Node.js、Go、Perl 等语言的 SDK 示例。"
articleTitle: "使用 Aspose.Cells Cloud API 在 Excel 工作表中复制列"
weight: 30
---

此 REST API 可在 Excel 工作表中复制**列**。**复制列**操作允许您复制单个列或一列范围，并将副本插入同一工作表内的指定位置。在处理大型电子表格时，可使用此端点高效地复制列；有关其他列管理任务，请参考相关操作，例如[添加列](/columns/add/)和[隐藏列](/columns/hide/)。

## 安全性与身份验证
Aspose.Cells Cloud API 采用安全机制，需要 [基于 JWT 令牌的身份验证](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)。

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/copy
```

### 请求参数

| 参数名称                   | 类型    | 位置   | 描述                                                                 |
| -------------------------- | ------- | ------ | -------------------------------------------------------------------- |
| **name**                   | string  | path   | 工作簿名称。                                                         |
| **sheetName**              | string  | path   | 工作表名称。                                                         |
| **sourceColumnIndex**      | integer | query  | 要复制的列的从 0 开始的索引。                                        |
| **destinationColumnIndex** | integer | query  | 要插入复制列（或多列）的从 0 开始的索引。                            |
| **columnNumber**           | integer | query  | 要复制的连续列的数量。                                               |
| **worksheet**              | string  | query  | _（可选）_ 当工作表名称与路径不一致时使用的工作表标识符。            |
| **folder**                 | string  | query  | Aspose Cloud 存储中包含工作簿的文件夹路径。                          |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Cells/PostCopyWorksheetColumns)定义了此操作的完整契约。

### cURL 示例

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/copy?sourceColumnIndex=1&destinationColumnIndex=12&columnNumber=10" \
     -H "Authorization: Bearer $ASPOSE_TOKEN" \
     -H "accept: application/json"
```

### 响应

```json
{
  "Code": 200,
  "Status": "OK"
}
```

## 错误处理

API 返回标准 HTTP 状态码，并附带 JSON 格式的错误描述信息。

| 状态码 | 含义                                       | 示例 JSON 响应体                                                    |
| ------ | ------------------------------------------ | ------------------------------------------------------------------- |
| **400** | 错误请求 – 参数无效                         | `{ "Code": 400, "Message": "Invalid column index." }`               |
| **401** | 未授权 – 缺失或无效的令牌                   | `{ "Code": 401, "Message": "Access token is invalid or expired." }` |
| **404** | 未找到 – 工作簿或工作表不存在               | `{ "Code": 404, "Message": "Workbook not found." }`                 |
| **500** | 服务器内部错误 – 意外情况                   | `{ "Code": 500, "Message": "An unexpected error occurred." }`       |

> **故障排除方法：** 请确认访问令牌有效、工作簿和工作表名称正确，并且 `sourceColumnIndex`、`destinationColumnIndex` 和 `columnNumber` 均在工作表列范围内。

## 云 SDK 家族
使用 SDK 是加快开发速度的最佳方式。SDK 会处理底层细节，使您能专注于项目任务。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCopyWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCopyWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCopyWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCopyWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCopyWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCopyWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCopyWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCopyWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "调用复制列 API 时如何进行身份验证？",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "请使用您的客户端 ID 和密钥从 Aspose Cloud 获取 OAuth2 访问令牌，然后在请求头中以 `Authorization: Bearer <access_token>` 形式包含该令牌。"
      }
    },
    {
      "@type": "Question",
      "name": "`sourceColumnIndex` 与 `destinationColumnIndex` 的区别是什么？",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "`sourceColumnIndex` 是您要复制的列的从 0 开始的索引；`destinationColumnIndex` 是要插入复制列（或多列）的从 0 开始的索引。"
      }
    },
    {
      "@type": "Question",
      "name": "如果复制操作失败，我将收到什么响应？",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "API 将返回非 200 状态码（例如，400 表示错误请求，401 表示未授权）。响应体包含一个 JSON 对象，其中包含 `Code` 和 `Message` 字段，用于描述错误详情。"
      }
    }
  ]
}
</script>
---