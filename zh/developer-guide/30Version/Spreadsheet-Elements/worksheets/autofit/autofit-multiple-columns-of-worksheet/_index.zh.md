---
title: "在 Excel 工作表中自动调整多列列宽"
second_title: "文档"
linktitle: "列"
type: docs
url: /zh/worksheets/autofit/columns/
aliases: [/autofit-multiple-columns-of-worksheet/]
keywords: "Aspose.Cells, 自动调整列宽, Excel API, 云电子表格, REST"
description: "了解如何使用 Aspose.Cells Cloud REST API（v3.0）在 Excel 工作表中自动调整多列列宽。内容包括端点、参数、cURL 示例、错误处理以及 C#、Java、Python 等语言的 SDK 代码片段。"
weight: 20
---

此 REST API 可用于自动调整 Excel 工作表中的**多列**列宽。

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autofitcolumns
```

### **请求参数**

| 参数名称              | 类型    | 位置   | 描述                                                                                                                                   |
| --------------------- | ------- | ------ | -------------------------------------------------------------------------------------------------------------------------------------- |
| name                  | string  | path   | 文件名。                                                                                                                               |
| sheetName             | string  | path   | 工作表名称。                                                                                                                           |
| firstColumn           | integer | query  | 起始列索引。                                                                                                                           |
| lastColumn            | integer | query  | 结束列索引。                                                                                                                           |
| autoFitterOptions\*   | object  | body   | 自动调整选项（参见 [自动调整选项](/zh/cells/auto-fitter-options/)）。包含 `AutoFitMergedCells`（自动调整合并单元格）、`IgnoreHidden`（忽略隐藏行）和 `OnlyAuto`（仅自动调整）。 |
| firstRow              | integer | query  | 自动调整的起始行索引（**可选**）。                                                                                                     |
| lastRow               | integer | query  | 自动调整的结束行索引（**可选**）。                                                                                                     |
| folder                | string  | query  | 存储中的文件夹路径（**可选**）。                                                                                                       |
| storageName           | string  | query  | 存储名称（**可选**）。                                                                                                                 |

\* 参数名称显示为链接，指向相关文档。

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Worksheets/PostAutofitWorksheetColumns) 定义了一个公开可用的编程接口，可让您直接通过网页浏览器进行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleAutoFit.xlsx/worksheets/Sheet1/autofitcolumns?lastColumn=5&firstColumn=0" \
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

使用 SDK 是加快开发速度的最佳方式。SDK 会处理底层细节，使您能专注于项目任务。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

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