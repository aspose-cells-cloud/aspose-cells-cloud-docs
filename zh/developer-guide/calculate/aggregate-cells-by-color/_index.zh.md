---
title: "Aspose.Cells Cloud Web API – 按颜色汇总 Excel 中的单元格（求和与计数）"
second_title: "文档"
ArticleTitle: "按颜色汇总电子表格/Excel 中的单元格：求和、计数、平均值、最大值、最小值"
LinkTitle: "按颜色汇总单元格"
type: docs
url: /zh/aggregate-cells-by-color/
keywords: "Aspose, Cells, Excel, API, 汇总, 颜色, 求和, 计数, 平均值, 最小值, 最大值"
description: "使用 Aspose.Cells Cloud API 按单元格背景色或字体颜色（求和、计数、平均值、最小值、最大值）汇总 Excel 单元格。了解接口端点、参数、身份验证及 SDK 示例。"
weight: 100
---

## 概述

该 API 可根据单元格**颜色**执行数据计算。它可根据单元格的填充色或字体色，对 Excel 电子表格执行求和、计数、计算平均值，以及查找最大值和最小值。

| 计算操作 | 描述                                               |
| :------- | :------------------------------------------------- |
| 计数     | 统计具有相同颜色的单元格数量。                     |
| 求和     | 计算具有相同颜色的单元格数值总和。                 |
| 最大值   | 找出具有相同颜色的单元格中的最大数值。             |
| 最小值   | 找出具有相同颜色的单元格中的最小数值。             |
| 平均值   | 计算具有相同颜色的单元格数值的平均值。             |

## Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/calculate/aggregate/color
```

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数

| 参数名          | 类型     | 位置     | 描述                                                         |
| :-------------- | :------- | :------- | :----------------------------------------------------------- |
| Spreadsheet     | 文件     | FormData | 待处理的 Excel 工作簿文件。                                  |
| Worksheet       | 字符串   | Query    | 包含目标区域的工作表名称。                                   |
| Range           | 字符串   | Query    | A1 样式区域（例如：`A1:B10`）。                              |
| Operation       | 字符串   | Query    | 计算方式：`Sum`（求和）、`Count`（计数）、`Average`（平均值）、`Min`（最小值）或 `Max`（最大值）。 |
| ColorPosition   | 字符串   | Query    | 指定需评估的颜色类型：`Background`（背景色）或 `Font`（字体色）。 |
| Region          | 字符串   | Query    | 电子表格所在区域设置（例如：`us-east-1`）。                  |
| Password        | 字符串   | Query    | 打开受保护工作簿所需的密码（可选）。                         |

#### 枚举值

- **ColorPosition**

  | 值         | 含义           |
  | :--------- | :------------- |
  | Background | 使用单元格填充色 |
  | Font       | 使用单元格字体色 |

**multipart/form‑data 请求示例**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/calculate/aggregate/color?Worksheet=Sheet1&Range=A1:B10&Operation=Sum&ColorPosition=Background" \
  -H "Authorization: Bearer <access_token>" \
  -F "Spreadsheet=@/path/to/workbook.xlsx"
```

### 响应

下述 Schema 描述了响应对象结构，其后附有具体示例。

```json
{
  "Name": "AggregateResultByColorResponse",
  "Type": "Class",
  "ParentName": "CellsCloudResponse",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "AggregateResults",
      "DataType": {
        "Identifier": "Array",
        "Reference": "AggregateResultByColor",
        "ElementDataType": {
          "Reference": "AggregateResultByColor"
        }
      }
    },
    {
      "Name": "Code",
      "DataType": { "Identifier": "Integer" }
    },
    {
      "Name": "Status",
      "DataType": { "Identifier": "String" }
    }
  ]
}
```

**示例响应（实际值）**

```json
{
  "Code": 200,
  "Status": "OK",
  "AggregateResults": [
    {
      "Color": "#FF0000",
      "Count": 12,
      "Sum": 345.67,
      "Average": 28.8,
      "Min": 5.0,
      "Max": 80.0
    },
    {
      "Color": "#00FF00",
      "Count": 7,
      "Sum": 210.0,
      "Average": 30.0,
      "Min": 10.0,
      "Max": 50.0
    }
  ]
}
```

**HTTP 状态码**

| 状态码 | 含义                 | 描述                                               |
| :----- | :------------------- | :------------------------------------------------- |
| 200    | OK（请求成功）       | 成功应用筛选条件；响应中包含操作详情。             |
| 400    | Bad Request（请求错误） | 参数缺失或无效（例如：不支持的文件类型）。         |
| 401    | Unauthorized（未授权）  | JWT 令牌无效或缺失。                               |
| 413    | Payload Too Large（载荷过大） | 上传文件超过大小限制。                           |
| 500    | Internal Server Error（内部服务器错误） | 服务器内部发生意外错误。                     |

## 在何处应使用“按颜色汇总” API？

在电子表格中，不同类别的数据通常以颜色编码。该 API 可对每种颜色组分别执行求和、计数、平均值、最小值和最大值计算，从而简化基于颜色的数据分析流程。

## 为何应使用“按颜色汇总” API？

该 API 提供了一种快速、可靠的方式，无需编写自定义解析逻辑即可完成颜色相关的计算。它与 Aspose.Cells Cloud SDK 无缝集成，开发者仅需编写少量代码即可实现颜色聚合功能。

## 如何使用 SDK 调用“按颜色汇总” API

### “按颜色汇总” API 规范

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Calculate/AggregateCellsByColor" rel="noopener noreferrer">“按颜色汇总” API 规范</a> 定义了一个公开可访问的编程接口，允许您直接从 Web 浏览器发起 REST 调用。

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是最快捷的开发方式，因其已对底层细节进行了封装，您只需编写简短代码即可实现按单元格颜色进行汇总计算。  
请查阅 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 仓库</a> 以获取 Aspose.Cells Cloud SDK 完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_AggregateCellsByColor.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_AggregateCellsByColor.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_AggregateCellsByColor.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_AggregateCellsByColor.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_AggregateCellsByColor.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_AggregateCellsByColor.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_AggregateCellsByColor.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_AggregateCellsByColor.go" >}}
{{</tab>}}
{{< /tabs >}}

**注意事项：**

- 处理受保护的工作簿时，请包含可选的 `Password` 查询参数，否则请求将因未授权（401）错误而失败。
- `Spreadsheet` 文件的最大请求大小为 100 MB。若需处理更大的文件，建议先将工作簿上传至 Aspose Cloud 存储空间，再通过 `Path` 参数引用（此处未展示该方式）。