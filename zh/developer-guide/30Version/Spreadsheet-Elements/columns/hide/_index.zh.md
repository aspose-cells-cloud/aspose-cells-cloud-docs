---
title: "隐藏 Excel 工作表中的列"
second_title: "文档"
linktitle: "隐藏"
type: docs
url: /zh/columns/hide/
aliases:
  - /hide-columns-in-excel-worksheet/
  - /hide-columns-in-an-excel-worksheet/
keywords: "Aspose.Cells Cloud, 隐藏列 API, Excel 列隐藏, REST API 隐藏列, Aspose.Cells SDK, 电子表格自动化"
description: "了解如何使用 Aspose.Cells Cloud REST API（v3.0）隐藏 Excel 工作表中的一列或多列。内容包括端点、参数、cURL 示例、SDK 代码示例以及错误处理。"
weight: 40
---

此 REST API 用于隐藏工作表中的列。

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/hide
```

### 请求参数

| 参数名          | 类型    | 位置   | 描述                                                             |
| --------------- | ------- | ------ | ---------------------------------------------------------------- |
| name            | string  | path   | 工作簿文件的名称。                                               |
| sheetName       | string  | path   | 将隐藏列的工作表名称。                                           |
| startColumn     | integer | query  | 要隐藏的第一列的从零开始的索引。                                 |
| totalColumns    | integer | query  | 从 **startColumn** 开始连续要隐藏的列数。                        |
| folder          | string  | query  | 包含工作簿的文件夹路径。                                         |
| storageName     | string  | query  | 存储服务的名称（文件所在位置）。                                 |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Cells/PostHideWorksheetColumns) 定义了一个公开可访问的编程接口，可让您直接从网页浏览器执行 REST 交互。

您可以使用 **cURL** 命令行工具轻松调用 Aspose.Cells Web 服务。下面的示例展示了如何使用 cURL 隐藏一列。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/hide?startColumn=1&totalColumns=1" \
     -H "accept: application/json" \
     -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**可能的响应码**

| HTTP 状态码 | 含义                           | 示例 JSON（错误）                                     |
| ----------- | ------------------------------ | ----------------------------------------------------- |
| 200         | 成功                           | `{ "Code": 200, "Status": "OK" }`                     |
| 400         | 错误请求（例如参数无效）       | `{ "Code": 400, "Message": "无效的列范围。" }`        |
| 401         | 未授权（缺少/无效的令牌）      | `{ "Code": 401, "Message": "无效的访问令牌。" }`      |
| 404         | 未找到（工作簿或工作表不存在） | `{ "Code": 404, "Message": "文件未找到。" }`          |
| 500         | 服务器内部错误                 | `{ "Code": 500, "Message": "意外错误。" }`            |

{{< /tab >}}

{{< /tabs >}}

## 云 SDK 家族

使用 SDK 是开发速度最快的方式。SDK 抽象了底层细节，让您专注于业务逻辑。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostHideWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostHideWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostHideWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostHideWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostHideWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostHideWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostHideWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostHideWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}