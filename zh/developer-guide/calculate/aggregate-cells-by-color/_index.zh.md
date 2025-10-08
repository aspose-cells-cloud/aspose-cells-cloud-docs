---
title: Aspose.Cells Cloud Web API - 在电子表格/Excel中按颜色求和、计数、平均值等
second_title: Documen
ArticleTitle: Sum, Count, Average Value, etc by color in Spreadsheet/Exce
LinkTitle: Aggregate Cells by Colo
type: docs
url: /zh/aggregate-cells-by-color/
keywords: Sum, Count, Average Value, Max Value, Min Value, Excel REST API, Spreadsheet Operations, Aspose.Cells, Excel Cloud AP
description: Aspose.Cells Cloud Web API（Excel Cloud API）可以执行数据计算、求和和平均，还可以根据单元格的填充或字体颜色查找 Excel 电子表格中的最大值和最小值
weight: 100
kwords: 总和、计数、平均值、最大值、最小值、Excel REST API、电子表格操作、Aspose.Cells、Excel 云 API
---
API 可以执行数据计算、求和和平均，还可以根据单元格的填充或字体颜色查找 Excel 电子表格中的最大值和最小值。

|计算操作|描述|
|:- |:- |
|数数|确定具有相同颜色的单元格的数量。|
|和|计算相同颜色单元格的总值。|
|最大值|确定相同颜色单元格中的最高值。|
|最小值|在相同颜色的单元格中找到最低值。|
|平均值|计算具有相同颜色的单元格的平均值。|

## **按颜色 API 聚合 Cells**

```http
PUT http://api.aspose.cloud/v4.0/cells/calculate/aggregate/color
```

### **请求参数：**

|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|电子表格|文件|表单数据|上传电子表格文件。|
|工作表|细绳|询问|指定工作表。|
|范围|细绳|询问|指定范围。|
|手术|细绳|询问|指定计算操作方法，包括Sum、Count、Average、Min、Max。|
|颜色位置|细绳|询问|指示根据背景颜色和/或字体颜色对内容进行求和和计数。|
|地区|细绳|询问|电子表格区域设置。|
|密码|细绳|询问|打开电子表格文件的密码。|

### **回复**

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
      "DataType": {
        "Identifier": "Integer",
      }
    },
    {
      "Name": "Status",
      "DataType": {
        "Identifier": "String",
      }
    }
  ]
}
```

### 错误代码

- **400 错误请求**：无效的 Apose.Cells Cloud API URI。
- **401 未授权**：访问令牌无效。或者客户端 ID 和密钥无效。
- **404 未找到**：电子表格文件无法访问。
- **500 服务器错误**：电子表格在获取计算数据时遇到异常。

## 我们应该在哪里使用按颜色聚合 API？

在电子表格中，不同类别的数据以不同的颜色显示，允许根据颜色进行求和、计数、计算平均值以及查找最大值和最小值等操作。

## 为什么要使用按颜色聚合 API？

- 提供颜色数据分析的方法。
- 根据颜色对数据进行分类计算，为数据分析提供基础数据。
- 通过现有的SDK即可快速完成开发。

## 如何通过 SDK 使用颜色聚合 API

### 按颜色聚合 API 规格

这[按颜色聚合 API 规格](https://reference.aspose.cloud/cells/#/CalculateController/AggregateCellsByColor)定义一个可公开访问的编程接口，并允许您直接从 Web 浏览器执行 REST 交互。

### 使用 Aspose.Cells 云 SDK

使用 SDK 是最快的开发方式，因为它抽象了低级细节，让您只需使用一小段代码即可按单元格颜色聚合计算。
请查看[GitHub 存储库](https://github.com/aspose-cells-cloud)以获取 Aspose.Cells Cloud SDKs 的完整列表。

以下代码示例演示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_AggregateCellsByColor.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_AggregateCellsByColor.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_AggregateCellsByColor.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_AggregateCellsByColor.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_AggregateCellsByColor.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_AggregateCellsByColor.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_AggregateCellsByColor.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_AggregateCellsByColor.go" >}}
{{< /tab >}}
{{< /tabs >}}
