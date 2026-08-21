---
title: "从工作表获取图表图例"
type: docs
url: /zh/charts/legend/get/
aliases: [  /zh/get-chart-legend-from-a-worksheet/ ]
weight: 80
keywords: "Aspose.Cells, 图表图例, REST API, Excel, 云 SDK, 获取图表图例, 工作表, 电子表格"
description: "使用 Aspose.Cells Cloud REST API（v3.0）从 Excel 工作簿中特定工作表的图表中检索图例信息。包含端点、参数、cURL 示例及 SDK 代码片段。"
---

**获取图表图例（Get Chart Legend）** 操作可返回 Excel 工作簿中某工作表内图表的图例信息。该端点属于 **Aspose.Cells Cloud API v3.0**，可用于读取图例的属性，如位置、字体、尺寸及格式设置等。

## **REST API**

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/legend
```

### 安全与身份验证

Aspose.Cells Cloud API 采用安全机制，需使用基于 [JWT 令牌的身份验证](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)。

### 请求参数

| 参数名        | 类型     | 位置   | 描述                           |
| ------------- | -------- | ------ | ------------------------------ |
| name          | string   | path   | 工作簿文件名。                 |
| sheetName     | string   | path   | 工作表名称。                   |
| chartIndex    | integer  | path   | 图表的从零开始的索引。         |
| folder        | string   | query  | 工作簿所在文件夹的路径。       |
| storageName   | string   | query  | 存储名称。                     |

### **响应示例**

```json
{
  "Legend": {
    "Position": "Right",
    "LegendEntries": {
      "link": {
        "Href": "/legendEntries",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "Area": {
      "BackgroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
      "FillFormat": {
        "Type": "Automatic",
        "SolidFill": null,
        "PatternFill": null,
        "TextureFill": null,
        "GradientFill": null,
        "ImageData": null
      },
      "ForegroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
      "Formatting": "Automatic",
      "InvertIfNegative": false,
      "Transparency": 0.0
    },
    "AutoScaleFont": true,
    "BackgroundMode": "Automatic",
    "Border": {
      "BeginArrowLength": "Medium",
      "BeginArrowWidth": "Medium",
      "BeginType": "None",
      "CapType": "Flat",
      "Color": { "A": 0, "R": 0, "G": 0, "B": 0 },
      "CompoundType": "Single",
      "DashType": "Solid",
      "EndArrowLength": "Medium",
      "EndArrowWidth": "Medium",
      "EndType": "None",
      "GradientFill": null,
      "IsAuto": true,
      "IsAutomaticColor": true,
      "IsVisible": true,
      "JoinType": "Round",
      "Style": "Solid",
      "Transparency": 0.0,
      "Weight": "HairLine",
      "WeightPt": 0.0
    },
    "Font": {
      "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
      "DoubleSize": 10.0,
      "IsBold": false,
      "IsItalic": false,
      "IsStrikeout": false,
      "IsSubscript": false,
      "IsSuperscript": false,
      "Name": "Arial",
      "Size": 10,
      "Underline": "None"
    },
    "IsAutomaticSize": true,
    "IsInnerMode": null,
    "Shadow": false,
    "ShapeProperties": null,
    "Width": 823,
    "Height": 1043,
    "X": 3125,
    "Y": 1466,
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/legend",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 0,
  "Status": "0"
}
```

**HTTP 状态码说明**

| 状态码 | 含义             | 描述                                               |
|--------|------------------|----------------------------------------------------|
| 200    | OK（成功）       | 过滤器应用成功；响应包含操作详情。                 |
| 400    | Bad Request（错误请求） | 缺少或参数无效（例如，文件类型不被支持）。         |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                               |
| 413    | Payload Too Large（载荷过大） | 上传文件超出大小限制。                           |
| 500    | Internal Server Error（内部服务器错误） | 服务器发生意外错误。                         |

## 如何使用 SDK 调用 GetWorksheetChartLegend API

### GetWorksheetChartLegend API 规范

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Charts/GetWorksheetChartLegend) 定义了一个公开可访问的编程接口，允许您直接从 Web 浏览器发起 REST 请求。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何通过 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/legend" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Legend": {
    "Position": "Right",
    "LegendEntries": {
      "link": {
        "Href": "/legendEntries",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "Area": {
      "BackgroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
      "FillFormat": {
        "Type": "Automatic",
        "SolidFill": null,
        "PatternFill": null,
        "TextureFill": null,
        "GradientFill": null,
        "ImageData": null
      },
      "ForegroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
      "Formatting": "Automatic",
      "InvertIfNegative": false,
      "Transparency": 0.0
    },
    "AutoScaleFont": true,
    "BackgroundMode": "Automatic",
    "Border": {
      "BeginArrowLength": "Medium",
      "BeginArrowWidth": "Medium",
      "BeginType": "None",
      "CapType": "Flat",
      "Color": { "A": 0, "R": 0, "G": 0, "B": 0 },
      "CompoundType": "Single",
      "DashType": "Solid",
      "EndArrowLength": "Medium",
      "EndArrowWidth": "Medium",
      "EndType": "None",
      "GradientFill": null,
      "IsAuto": true,
      "IsAutomaticColor": true,
      "IsVisible": true,
      "JoinType": "Round",
      "Style": "Solid",
      "Transparency": 0.0,
      "Weight": "HairLine",
      "WeightPt": 0.0
    },
    "Font": {
      "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
      "DoubleSize": 10.0,
      "IsBold": false,
      "IsItalic": false,
      "IsStrikeout": false,
      "IsSubscript": false,
      "IsSuperscript": false,
      "Name": "Arial",
      "Size": 10,
      "Underline": "None"
    },
    "IsAutomaticSize": true,
    "IsInnerMode": null,
    "Shadow": false,
    "ShapeProperties": null,
    "Width": 823,
    "Height": 1043,
    "X": 3125,
    "Y": 1466,
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/legend",
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

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加速开发的最佳方式。SDK 处理底层细节，让您专注于项目任务。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-GetChartLegend-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-GetChartLegend-get-chart-legend.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-GetWorksheetChartLegend-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-get_chart_legend-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetChartLegendFromWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-GetChartLegend-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-GetChartLegend-get-chart-legend.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-GetChartLegend-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "76b8d73d934c0f03675299687805040f" >}}

{{< /tab >}}

{{< /tabs >}}

---