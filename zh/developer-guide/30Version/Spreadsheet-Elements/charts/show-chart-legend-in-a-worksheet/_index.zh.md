---
title: "在工作表中显示图表图例"
type: docs
url: /charts/legend/show/
aliases: [/show-chart-legend-in-a-worksheet/]
weight: 100
keywords: "Aspose.Cells Cloud、图表图例 API、Excel 图表图例、REST PUT 图表图例、Aspose API v3.0"
description: "了解如何使用 Aspose.Cells Cloud REST API（v3.0）在 Excel 工作表中显示图表图例。包含端点详情、参数、cURL 示例以及 SDK 代码片段。"
---

此 REST API 可帮助您在 Excel 工作簿工作表中的图表内显示**图例**——即用于标识数据系列的说明性框。

## REST API

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/legend
```

### 请求参数

| 参数名称      | 类型     | 位置   | 描述                                    |
| ------------- | -------- | ------ | --------------------------------------- |
| name          | string   | path   | 工作簿文件名。                          |
| sheetName     | string   | path   | 包含图表的工作表名称。                  |
| chartIndex    | integer  | path   | 图表的从零开始的索引。                  |
| folder        | string   | query  | 包含工作簿的文件夹。                    |
| storageName   | string   | query  | 存储服务的名称。                        |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Charts/PutWorksheetChartLegend) 定义了一个公开可用的编程接口，可让您直接通过网页浏览器执行 REST 交互。

身份验证通过在 **Authorization** 请求头中提供的 Bearer JWT 令牌完成。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 发起该调用。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/legend" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

该 API 可返回以下 HTTP 状态码：

- **200 OK** – 图例已成功显示。
- **400 Bad Request** – 请求参数无效。
- **401 Unauthorized** – 身份验证失败。
- **404 Not Found** – 指定的工作簿、工作表或图表不存在。
- **500 Internal Server Error** – 发生了意外的服务器错误。

{{< /tab >}}

{{< /tabs >}}

## 云 SDK 家族

使用 SDK 是加速开发的最佳方式。SDK 会处理底层细节，让您专注于项目任务。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-ShowChartLegend-1.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-ShowChartLegend-show-chart-legend.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-PutWorksheetChartLegend-.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-show_legend_in_chart-.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "ShowChartLegendInAWorksheet.py" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-ShowChartLegend-1.js" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-ShowChartLegend-show-chart-legend.java" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-ShowChartLegend-1.pl" >}}
{{< /tab >}}

{{< tab tabNum="10" >}}
{{< gist "aspose-cells-cloud-gists" "f9f1d14e3b6985c0a44ec7acdd4f56b2" >}}
{{< /tab >}}

{{< /tabs >}}