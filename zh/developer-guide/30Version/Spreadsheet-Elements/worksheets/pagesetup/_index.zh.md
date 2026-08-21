---
title: "工作表页面设置"
second_title: "文档"
linktitle: "页面设置"
type: docs
url: /page-setup/
keywords: "Aspose.Cells, pageSetup, 工作表, 打印设置, 边距, 方向, 纸张大小, 页眉, 页脚, 缩放比例"
description: "了解如何使用 Aspose.Cells Cloud 的 PageSetup 对象配置 Excel 工作表的打印布局。包含属性列表、默认值、取值范围以及 C#、Java 和 Python 的代码示例。"
weight: 20
ArticleTitle: "工作表页面设置 – 使用 Aspose.Cells Cloud 配置打印布局"
---

# **PageSetup（页面设置）**

Excel 打印页面设置

## 概述

**PageSetup** 对象用于定义 Excel 工作表的打印布局选项，例如边距、页面方向、缩放比例、页眉、页脚以及其他与打印相关的设置。通过配置这些属性，开发者可生成符合预期外观和分页效果的可打印工作簿。

以下是一个简短的 C# 示例，演示如何使用 Aspose.Cells Cloud SDK 设置常见的页面设置属性：

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

// 初始化 API 客户端（请替换为您的凭据）
var apiInstance = new CellsApi("YOUR_CLIENT_ID", "YOUR_CLIENT_SECRET");

// 定义 PageSetup（页面设置）参数
var pageSetup = new PageSetup()
{
    Orientation = "Landscape",
    PaperSize = "A4",
    CenterHorizontally = true,
    CenterVertically = true,
    Zoom = 100
};

// 将设置应用于工作簿的第一个工作表
apiInstance.PutWorksheetPageSetup("Sample.xlsx", "Sheet1", pageSetup);
```

该代码段将工作表设置为横向打印，使用 A4 纸张，内容水平和垂直居中，并应用 100% 的缩放比例。

## 属性说明

| 属性名称                | 属性类型 | 可为空 | 只读 | 默认值           | 描述                                                                         |
| ----------------------- | -------- | ------ | ---- | ---------------- | ---------------------------------------------------------------------------- |
| BlackAndWhite           | bool     | false  | false| false            | 以黑白模式打印工作表。                                                       |
| BottomMargin            | float    | true   | false| 2.54 cm          | 底边距大小（单位：厘米）。                                                   |
| CenterHorizontally      | bool     | false  | false| false            | 打印时使工作表在页面中水平居中。                                             |
| CenterVertically        | bool     | false  | false| false            | 打印时使工作表在页面中垂直居中。                                             |
| FirstPageNumber         | int      | true   | false| 1                | 打印工作表时使用的第一页页码。                                               |
| FitToPagesTall          | int      | false  | false| 1                | 工作表在垂直方向上缩放至的页数。                                             |
| FitToPagesWide          | int      | false  | false| 1                | 工作表在水平方向上缩放至的页数。                                             |
| FooterMargin            | float    | true   | false| 2.54 cm          | 页脚底部到页面底部的距离（单位：厘米）。                                     |
| HeaderMargin            | float    | true   | false| 2.54 cm          | 页眉顶部到页面顶部的距离（单位：厘米）。                                     |
| IsAutoFirstPageNumber   | bool     | false  | false| false            | 是否自动分配第一页页码。                                                     |
| IsHFAlignMargins        | bool     | false  | false| true             | 为 true 时，页眉/页脚边距与页面边距对齐。                                    |
| IsHFDiffFirst           | bool     | false  | false| false            | 表示首页的页眉/页脚与其他页不同。                                            |
| IsHFDiffOddEven         | bool     | false  | false| false            | 表示奇数页与偶数页的页眉/页脚不同。                                          |
| IsHFScaleWithDoc        | bool     | false  | false| false            | 页眉和页脚随文档一起缩放（适用于 Excel 2007 及更高版本）。                   |
| IsPercentScale          | bool     | false  | false| true             | 为 false 时，`FitToPagesWide` 和 `FitToPagesTall` 控制缩放比例。            |
| LeftMargin              | float    | true   | false| 2.54 cm          | 左边距大小（单位：厘米）。                                                   |
| Order                   | string   | true   | false| "DownThenOver"   | Excel 在打印大型工作表时对页面编号的顺序。                                   |
| Orientation             | string   | false  | false| "Portrait"       | 页面方向：**Landscape（横向）** 或 **Portrait（纵向）**。                    |
| PaperSize               | string   | true   | false| "A4"             | 打印所用的纸张大小。                                                         |
| PrintArea               | string   | true   | false| （无）           | 需打印的单元格区域（例如 `"A1:D20"`）。                                     |
| PrintComments           | string   | true   | false| "NoComments"     | 打印工作表时如何处理批注。                                                   |
| PrintCopies             | int      | true   | false| 1                | 打印份数。                                                                   |
| PrintDraft              | bool     | false  | false| false            | 以草稿模式打印工作表（不包含图形）。                                         |
| PrintErrors           | string   | true   | false| "Display"        | 打印错误的显示类型。                                                         |
| PrintGridlines          | bool     | false  | false| false            | 打印单元格网格线。                                                           |
| PrintHeadings           | bool     | false  | false| false            | 打印行标题和列标题。                                                         |
| PrintQuality            | int      | true   | false| 600              | 打印质量设置（单位：每英寸点数 DPI）。                                       |
| PrintTitleColumns       | string   | true   | false| （无）           | 每页左侧重复打印的列范围。                                                   |
| PrintTitleRows          | string   | true   | false| （无）           | 每页顶部重复打印的行范围。                                                   |
| RightMargin             | float    | true   | false| 2.54 cm          | 右边距大小（单位：厘米）。                                                   |
| TopMargin               | float    | true   | false| 2.54 cm          | 顶边距大小（单位：厘米）。                                                   |
| Zoom                    | int      | false  | false| 100              | 缩放比例（百分比），取值范围为 10–400。                                      |
| Header                  | object   | true   | false| （无）           | 页面页眉配置。                                                               |
| Footer                  | object   | true   | false| （无）           | 页面页脚配置。                                                               |

## 相关对象

- **Header** – 用于配置工作表页眉。  
- **Footer** – 用于配置工作表页脚。  
- **PrintOptions** – 其他打印相关设置，例如分页符和打印区域。  
---