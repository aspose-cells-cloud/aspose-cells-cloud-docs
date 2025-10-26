---
title: Aspose.Cells Cloud Web API - 在电子表格/Excel 上进行加、减、乘、除和百分比运算
second_title: Documen
ArticleTitle: Add, Minus, Multiply, Divide and Percentage in Spreadsheet/Exce
linktitle: 数学计算
type: docs
url: /zh/math-calculate/
keywords: Math calculation,Cloud REST API, Add, Minus, Multiply, Divide, Percentage, Office Cloud, Aspose.Cell
description: 使用 Math Calculate API 在 Excel 电子表格中执行计算的综合指南
weight: 100
kwords: 数学计算，Cloud REST API，加，减，乘，除，百分比，Office 云，Aspose.Cells
---
开发人员可以使用此 API 对指定范围的电子表格/Excel 执行加法、减法、乘法、除法和百分比计算。

|**计算操作** |描述|
|:- |:- |
|**添加** |+ |
|**减** |-  |
|**乘** |*  |
|**划分** |/ |
|**百分比** |% |

## **数学计算 API**

```http
PUT http://api.aspose.cloud/v4.0/cells/calculate/math
```

### **请求参数：**

|参数名称|类型|路径/查询字符串/HTTP 正文|描述|
|:- |:- |:- |:- |
|电子表格|文件|表单数据|上传电子表格文件以供处理。|
|手术|细绳|询问|要执行的数学运算（加、减、乘、除和百分比）。|
|价值|细绳|询问|如果适用，则为计算中使用的值。|
|工作表|细绳|询问|要操作的工作表的名称。|
|范围|细绳|询问|计算中要包括的单元格范围。|
|地区|细绳|询问|定义电子表格的特定区域。|
|密码|细绳|询问|如果受保护，则打开电子表格文件的密码。|

### **回复**

```json
[
    {
        "Name": "ResponseFile",
        "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
        }
    }
]
```

### 错误代码

- **400 错误请求**：无效的 Apose.Cells Cloud API URI。
- **401 未授权**：访问令牌无效。或者客户端 ID 和密钥无效。
- **404 未找到**：电子表格文件无法访问。
- **500 服务器错误**：电子表格在获取计算数据时遇到异常。

## 我们应该在哪里使用数学计算 API？

数学计算 API 适用于电子表格上的批量计算。

## 为什么要使用数学计算 API？

- 执行批量数学计算。
- 通过现有的SDK即可快速完成开发。

## 如何通过 SDK 使用 Math Calculate API

### 数学计算 API 规格

这[数学计算规范](https://reference.aspose.cloud/cells/#/CalculateController/MathCalculate)定义一个可公开访问的编程接口，允许开发人员直接从 Web 浏览器与 API 进行交互。

### 使用 Aspose.Cells 云 SDK

使用 SDK 是最快的开发方式，因为它抽象了低级细节，让您仅使用一小段代码即可按单元格进行数学计算。
请查看[GitHub 存储库](https://github.com/aspose-cells-cloud)以获取 Aspose.Cells Cloud SDKs 的完整列表。

以下代码示例演示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MathCalculate.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MathCalculate.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MathCalculate.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MathCalculate.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MathCalculate.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MathCalculate.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MathCalculate.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MathCalculate.go" >}}
{{< /tab >}}
{{< /tabs >}}
