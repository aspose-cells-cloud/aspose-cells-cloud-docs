---
title: "使用 Aspose.Cells Cloud API 在 Excel 中自动调整列宽 — 快速指南"
second_title: "文档"
linktitle: "列"
type: docs
url: /zh/worksheets/autofit/column/
aliases: [  /zh/autofit-single-column-of-worksheet/ ]
keywords: "Aspose.Cells Cloud, 自动调整列宽, Excel API, REST API, SDK, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go"
description: "了解如何使用 Aspose.Cells Cloud REST API 自动调整 Excel 工作表中单列或列范围的宽度。包含 cURL、SDK 示例（C#、Java、Python 等）以及完整的请求/响应详情。"
weight: 10
---

此 REST API 可自动调整 Excel 工作表中单列或连续多列的宽度。

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autofitcolumns
```

### 请求参数

| 参数名称          | 类型    | 位置   | 描述                                                                                             |
| ----------------- | ------- | ------ | ------------------------------------------------------------------------------------------------ |
| name              | string  | 路径   | Excel 文件的名称。                                                                               |
| sheetName         | string  | 路径   | 工作表的名称。                                                                                   |
| firstColumn       | integer | 查询   | 要自动调整宽度的第一列的从 0 开始的索引。                                                       |
| lastColumn        | integer | 查询   | 要自动调整宽度的最后一列的从 0 开始的索引。                                                     |
| autoFitterOptions | object  | 请求体 | 控制自动调整行为的选项（参见 [AutoFitterOptions](/cells/auto-filter-options)）。             |
| firstRow          | integer | 查询   | 计算列宽时所考虑的第一行的从 0 开始的索引。                                                     |
| lastRow           | integer | 查询   | 计算列宽时所考虑的最后一行的从 0 开始的索引。                                                   |
| folder            | string  | 查询   | 存储中文件所在的文件夹。                                                                         |
| storageName       | string  | 查询   | 存储服务的名称。                                                                                 |

### 错误响应

| HTTP 状态码 | 含义                                       | 示例 JSON 请求体                                          |
| ----------- | ------------------------------------------ | --------------------------------------------------------- |
| 400         | 参数无效                                   | `{"Code":400,"Message":"Invalid parameter 'firstColumn'."}` |
| 401         | 未授权 — 缺少或无效的 JWT 令牌             | `{"Code":401,"Message":"Authorization failed."}`          |
| 404         | 文件或工作表未找到                         | `{"Code":404,"Message":"Worksheet 'Sheet1' not found."}`  |
| 500         | 服务器内部错误                             | `{"Code":500,"Message":"An unexpected error occurred."}`  |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Worksheets/PostAutofitWorksheetColumns) 定义了一个公开可访问的编程接口，您可直接在网页浏览器中发起 REST 调用。

您可以使用 **cURL** 命令行工具调用 Aspose.Cells Cloud 服务。以下示例演示如何调用自动调整列宽接口。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleAutoFit.xlsx/worksheets/Sheet1/autofitcolumns?firstColumn=2&lastColumn=2" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"AutoFitMergedCells": true, "IgnoreHidden": true, "OnlyAuto": true}'
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

## 云 SDK 家族

使用 SDK 是将 API 集成到应用程序中的最快方式。SDK 处理底层细节，使您能够专注于业务逻辑。请参阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例演示如何使用 various SDK 调用自动调整列宽接口：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}