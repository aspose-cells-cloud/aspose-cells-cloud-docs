---
title: "向工作表添加图表"
type: docs
url: /charts/add/
aliases: [/add-a-chart-in-a-worksheet/]
weight: 20
description: "了解如何使用 Aspose.Cells Cloud API v3.0 向 Excel 工作表添加图表。内容包括端点、参数、cURL 示例和 SDK 代码片段。"
keywords:
  - "Aspose.Cells 添加图表"
  - "Aspose.Cells 添加图表 API"
  - "图表 API REST"
  - "Aspose.Cells SDK 示例"
ArticleTitle: "向工作表添加图表 – Aspose.Cells Cloud API 指南"
---

此 REST API 可向工作表添加新图表。

**前置条件**  
调用此操作前，请先获取有效的 JWT 访问令牌，并确保目标工作簿已存储在指定文件夹或存储位置中。

## PutWorksheetAddChart API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts
```

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，需进行 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称                | 类型    | 位置   | 描述                                                                                                                                                                                      |
| ----------------------- | ------- | ------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **name**                | string  | 路径   | 工作簿名称。                                                                                                                                                                              |
| **sheetName**           | string  | 路径   | 工作表名称。                                                                                                                                                                              |
| **chartType**           | string  | 查询   | 图表类型（参见图表资源中的 **Type** 属性）。支持的图表类型包括 **Bar**（柱状图）、**Column**（条形图）、**Line**（折线图）、**Pie**（饼图）、**Scatter**（散点图）、**Area**（面积图）、**Doughnut**（圆环图）、**Radar**（雷达图）等。 |
| **upperLeftRow**        | integer | 查询   | 图表区域左上角行索引（从 0 开始）。                                                                                                                                                       |
| **upperLeftColumn**     | integer | 查询   | 图表区域左上角列索引（从 0 开始）。                                                                                                                                                       |
| **lowerRightRow**       | integer | 查询   | 图表区域右下角行索引（从 0 开始）。                                                                                                                                                       |
| **lowerRightColumn**    | integer | 查询   | 图表区域右下角列索引（从 0 开始）。                                                                                                                                                       |
| **area**                | string  | 查询   | 提供绘图数据的单元格范围（例如 `A1:B5`）。                                                                                                                                                 |
| **isVertical**          | boolean | 查询   | 指示图表方向是否为纵向。                                                                                                                                                                  |
| **categoryData**        | string  | 查询   | 类别轴数据范围（例如 `D1:E10`）。                                                                                                                                                          |
| **isAutoGetSerialName** | boolean | 查询   | 若为 **true**，则自动生成系列名称。                                                                                                                                                        |
| **title**               | string  | 查询   | 图表标题。                                                                                                                                                                                |
| **folder**              | string  | 查询   | 包含工作簿的文件夹。                                                                                                                                                                      |
| **storageName**         | string  | 查询   | 存储名称。                                                                                                                                                                                |
| **dataLabels**          | boolean | 查询   | 为 **true** 时显示数据标签。                                                                                                                                                              |
| **dataLabelsPosition**  | string  | 查询   | 数据标签位置（例如 `Above`）。                                                                                                                                                            |
| **pivotTableSheet**     | string  | 查询   | 包含数据透视表的工作表名称。                                                                                                                                                              |
| **pivotTableName**      | string  | 查询   | 数据透视表名称。                                                                                                                                                                          |

### **响应**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP 状态码**

| 状态码 | 含义           | 描述                                     |
|--------|----------------|------------------------------------------|
| 200    | OK（成功）     | 筛选器应用成功；响应包含操作详细信息。       |
| 400    | Bad Request（请求错误） | 缺少或无效的参数（例如不支持的文件类型）。 |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                     |
| 413    | Payload Too Large（负载过大） | 上传文件超出大小限制。                   |
| 500    | Internal Server Error（内部服务器错误） | 服务器发生意外错误。                    |

## 如何使用 PutWorksheetAddChart API 及 SDK

### PutWorksheetAddChart API 规范

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Charts/PutWorksheetAddChart) 定义了一个公开可访问的编程接口，可让您直接通过网页浏览器发起 REST 请求。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何通过 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/charts?chartType=Bar&area=B1:F2&title=SalesState" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
# 此操作无需请求体
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

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加速开发的最佳方式。SDK 封装了底层细节，让您专注于项目任务。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Objective C" tabName8="Perl" tabName9="Android" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-AddChart-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-AddChart-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-PutWorksheetAddChart-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-add_new_chart_to_worksheet-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "AddChartToWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-AddChart-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-AddChart-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Examples-Android-chart-AddChart-AddChart.jave" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "7fa79c30fca0c594c18c0f3937b6bcc9" >}}

{{< /tab >}}

{{< /tabs >}}