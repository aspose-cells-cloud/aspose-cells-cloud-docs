---
title: 从工作表获取图表图例
type: docs
url: /zh/charts/legend/get/
aliases: [/get-chart-legend-from-a-worksheet/]
weight: 80
kwords: Excel、Office 云、REST API、电子表格、PDF、CSV、Json、Markdown、从工作表获取图表图例
---
此 REST API 表示获取图表图例
 
## 重新设置 API
 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/legend
 
```
请求参数为：
 
|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|姓名|细绳|小路|工作簿名称。|
|工作表名称|细绳|小路|工作表名称。|
|图表索引|整数|小路|图表索引。|
|文件夹|细绳|询问|工作簿文件夹。|
|存储名称|细绳|询问|存储名称。|
 

这[OpenAPI规范](https://apireference.aspose.cloud/cells/#/Charts/GetWorksheetChartLegend)定义一个可公开访问的编程接口，并允许您直接从 Web 浏览器执行 REST 交互。
 
您可以使用 cURL 命令行工具轻松访问 Aspose.Cells 的 Web 服务。以下示例展示了如何使用 cURL 调用云端 API。
 
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```java

curl -v "http://api.aspose.com/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/legend" 
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```java

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

      "BackgroundColor": {

        "A": 0,

        "R": 0,

        "G": 0,

        "B": 0

      },

      "FillFormat": {

        "Type": "Automatic",

        "SolidFill": null,

        "PatternFill": null,

        "TextureFill": null,

        "GradientFill": null,

        "ImageData": null

      },

      "ForegroundColor": {

        "A": 0,

        "R": 0,

        "G": 0,

        "B": 0

      },

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

      "Color": {

        "A": 0,

        "R": 0,

        "G": 0,

        "B": 0

      },

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

      "Color": {

        "A": 255,

        "R": 0,

        "G": 0,

        "B": 0

      },

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

      "Href": "http://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/legend",

      "Rel": "self",

      "Title": null,

      "Type": null

    }

  },

  "Code": 0,

  "Status": "0"

}

```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK 系列
 
使用 SDK 是加速开发的最佳方式。SDK 负责处理底层细节，让您专注于项目任务。请查看[GitHub 存储库](https://github.com/aspose-cells-cloud)以获取 Aspose.Cells Cloud SDKs 的完整列表。
 
以下代码示例演示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：
 
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
