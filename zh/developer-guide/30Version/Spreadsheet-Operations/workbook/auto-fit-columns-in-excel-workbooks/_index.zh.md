---
title: "在 Excel 文件中自动调整列宽"
second_title: "文档"
linktype: "列"
type: docs
url: /autofit-columns-on-an-excel-file/
aliases:
  [
    /auto-fit-columns-in-excel-workbooks,
    /autofit-columns-in-excel-workbooks/,
    /columns/autofit/,
    /workbook/autofit/columns/,
  ]
keywords: "自动调整列宽, Excel, Aspose.Cells Cloud, REST API, SDK, cURL, API"
description: "了解如何使用 Aspose.Cells Cloud REST API 自动调整 Excel 工作簿中的列宽。包含请求详情、cURL 示例以及多种编程语言的 SDK 代码示例。"
weight: 90
---

此 REST API 支持自动调整 Excel 工作簿中的列宽。

## PostAutofitWorkbookColumns API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/autofitcolumns
```

请求参数如下：

| 参数名称          | 类型     | 位置   | 描述                                  |
| ----------------- | -------- | ------ | ------------------------------------- |
| **name**          | 字符串   | 路径   | 工作簿文件的名称。                    |
| **autoFitterOptions** | 对象   | 请求体 | 控制自动调整行为的选项。              |
| **startColumn**   | 整数     | 查询参数 | 需要自动调整的第一列的从零开始索引。 |
| **endColumn**     | 整数     | 查询参数 | 需要自动调整的最后一列的从零开始索引。 |
| **folder**        | 字符串   | 查询参数 | 包含该工作簿的文件夹。                |
| **storageName**   | 字符串   | 查询参数 | 存储服务的名称。                      |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Workbook/PostAutofitWorkbookColumns){:rel="noopener noreferrer"} 定义了一个公开可用的编程接口，可让您直接从网页浏览器发起 REST 请求。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例演示如何使用 cURL 调用云 API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/autofitcolumns" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-d '{"AutoFitMergedCells":true, "IgnoreHidden":true}'
```

> **注意**：生产环境中请始终使用 HTTPS 端点，并妥善保管您的 JWT 令牌。

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

### 前提条件
调用此操作前，请确保您已拥有有效的 Aspose Cloud API 密钥、已生成的 JWT 令牌，并且目标工作簿已存在于指定的存储位置中。

**HTTP 状态码**

| 状态码 | 含义             | 描述                                      |
|--------|------------------|-------------------------------------------|
| 200    | OK（成功）       | 成功应用筛选；响应中包含操作详情。        |
| 400    | Bad Request（错误请求） | 缺少或无效的参数（例如，不支持的文件类型）。 |
| 401    | Unauthorized（未授权） | 无效或缺失的 JWT 令牌。                  |
| 413    | Payload Too Large（请求体过大） | 上传文件超过大小限制。                  |
| 500    | Internal Server Error（内部服务器错误） | 意外的服务器错误。                    |

该 API 可返回以下 HTTP 状态码：

| 状态码 | 描述                         |
|--------|------------------------------|
| 200    | 成功 — 已自动调整列宽         |
| 400    | 错误请求 — 缺少或无效的参数   |
| 401    | 未授权 — 无效或过期的 JWT 令牌 |
| 500    | 服务器错误 — 内部处理失败     |

## 云 SDK 家族

使用 SDK 是加速开发的最高效方式。SDK 会处理底层细节，让您专注于业务逻辑。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud){:rel="noopener noreferrer"} 获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例演示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorkbookColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorkbookColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorkbookColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorkbookColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorkbookColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorkbookColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorkbookColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorkbookColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}