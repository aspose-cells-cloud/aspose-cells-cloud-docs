---
title: "更新工作表中的图表图例"
type: docs
url: /zh/charts/legend/update/
aliases: [  /zh/update-chart-legend-in-a-worksheet/ ]
weight: 160
keywords: "Aspose.Cells, 云, Excel, 图表, 图例, REST API, 更新, 工作表, cURL, SDK"
description: "如何使用 Aspose.Cells Cloud REST API 更新 Excel 工作表中的图表图例，包含 cURL 请求示例及多种编程语言的 SDK 代码片段。"
ArticleTitle: "更新工作表中的图表图例 – Aspose.Cells Cloud API 指南"
---

本 REST API 用于更新图表图例。

**前提条件**：要使用此接口，您必须拥有有效的 Aspose Cloud JWT 令牌，且目标工作簿需存储于受支持的存储位置（默认为 Aspose Cloud 存储）。请确保工作簿名称、工作表名称和图表索引正确无误。

图表图例用于显示图表中数据系列的名称和符号。更新图例可自定义其外观，例如字体样式、颜色和阴影效果。

## PostWorksheetChartLegend API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/legend
```

### **安全性与身份验证**

Aspose.Cells Cloud API 采用安全机制，需进行 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称      | 类型    | 位置   | 描述                                   |
| ------------- | ------- | ------ | -------------------------------------- |
| name          | string  | path   | 工作簿名称。                           |
| sheetName     | string  | path   | 工作表名称。                           |
| chartIndex    | integer | path   | 待修改图表的索引。                     |
| legend        | object  | body   | 定义图例设置的 JSON 对象。             |
| folder        | string  | query  | 包含工作簿的文件夹路径。               |
| storageName   | string  | query  | 存储空间名称。                         |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Charts/PostWorksheetChartLegend) 定义了一个公开可访问的编程接口，允许您直接通过 Web 浏览器发起 REST 请求。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.com/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/legend" \
-d '{"Font":{"Color":{"A":"1","R":"255","G":"0","B":"0"},"DoubleSize":10.0,"IsBold":true,"IsItalic":false,"IsStrikeout":false,"IsSubscript":false,"IsSuperscript":false,"Name":"Arial","Size":15,"Underline":"None"},"Shadow":true}' \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## 云 SDK 开发工具包（SDK Family）

使用 SDK 可加速开发进程。SDK 处理底层细节，让您专注于项目核心任务。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-UpdateChartLegend-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-UpdateChartLegend-update-chart-legend.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-PostWorksheetChartLegend-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-update_chart_legend-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-UpdateChartLegend-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "UpdateChartLegendInWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-UpdateChartLegend-update-chart-legend.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-UpdateChartLegend-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "74fffa317bc5ba65dc6536005e5bb683" >}}

{{< /tab >}}

{{< /tabs >}}