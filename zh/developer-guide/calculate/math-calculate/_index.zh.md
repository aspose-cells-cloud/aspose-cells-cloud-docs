---
title: "Aspose.Cells Cloud – 数学计算 API（加、减、乘、除、百分比）"
second_title: "文档"
ArticleTitle: "电子表格/Excel 中的加、减、乘、除与百分比运算"
linktitle: "数学计算"
type: docs
url: /zh/math-calculate/
keywords: "数学计算 API、Aspose.Cells Cloud、Excel 计算、加法、减法、乘法、除法、百分比、批量 Excel 处理、REST API"
description: "了解如何使用 Aspose.Cells Cloud 数学计算 API，对 Excel 区域批量执行加、减、乘、除或百分比运算。包含请求格式、示例代码与错误处理说明。"
weight: 100
---

## **简介**：电子表格快速计算 —— 单一运行 API 实现加、减、乘、除与百分比公式

*无需编写公式即可对整列、整行或整个表格批量执行计算。*

- **基础数学运算**：对指定区域中的每个单元格与任意数值执行加、减、乘或除运算  
- **百分比运算**：按百分比增加/减少数值，或计算某数的百分比（如 +15%、-8%、20% of…）  
- **批量处理**：瞬间对数千个单元格执行运算 —— 无需拖拽填充、无需数组公式、无需 VBA  

| **计算操作** | **说明** |
| :----------- | :------- |
| **Add（加法）**                 | +   |
| **Subtract（减法）**            | -   |
| **Multiply（乘法）**            | \*  |
| **Divide（除法）**              | /   |
| **Percentage（百分比）**        | %   |

## **数学计算 API**

```http
PUT https://api.aspose.cloud/v4.0/cells/calculate/math
```

### **安全性与身份验证**

Aspose.Cells Cloud API 安全可靠，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### **请求参数：**

| 参数名称      | 类型   | 路径/查询字符串/HTTP 请求体 | 说明                                               |
| :------------ | :----- | :-------------------------- | :------------------------------------------------- |
| Spreadsheet   | 文件   | FormData                    | 上传待处理的电子表格文件。                         |
| operation     | 字符串 | 查询字符串                  | 要执行的数学运算（Add、Subtract、Multiply、Divide、Percentage）。 |
| value         | 字符串 | 查询字符串                  | 计算中使用的数值（如适用）。                       |
| worksheet     | 字符串 | 查询字符串                  | 要操作的工作表名称。                               |
| range         | 字符串 | 查询字符串                  | 参与计算的单元格区域。                             |
| region        | 字符串 | 查询字符串                  | 电子表格的区域设置。                               |
| password      | 字符串 | 查询字符串                  | 若文件受密码保护，则提供打开文件所需的密码。       |

### **响应**

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

**HTTP 状态码**

| 状态码 | 含义                 | 说明                                       |
| ------ | -------------------- | ------------------------------------------ |
| 200    | OK（成功）           | 运算成功应用；响应中包含运算详情。         |
| 400    | Bad Request（错误请求） | 缺少或无效的参数（如不支持的文件类型）。   |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                       |
| 413    | Payload Too Large（载荷过大） | 上传的文件大小超出限制。               |
| 500    | Internal Server Error（内部服务器错误） | 发生意外服务器错误。               |

## **数学计算 API 的适用场景**

- **财务场景**：为整列采购价格统一添加 13% 的增值税（VAT）。  
- **库存管理**：将公斤（kg）列乘以 2.2046，批量转换为磅（lbs）。  
- **薪资管理**：为所有员工的奖金列统一增加固定奖金 1,000。  
- **外汇转换**：将销售列除以实时汇率，换算为美元（USD）金额。  
- **评分场景**：从每位学生的分数中统一减去 5 分，作为出勤惩罚。  
- **电商场景**：一键应用 15% 的促销折扣，批量降低商品价格。  

## **为何选择数学计算 API？**

- **快速 Excel 计算**：数秒内完成月度报表。  
- **批量百分比调整 Excel**：一键更新价格、预测值、佣金等。  
- **整列添加相同数值**：适用于库存、货币换算、单位换算等场景。  
- **无公式 Excel 操作**：非技术人员也能轻松上手。  
- **通过现有 SDK 快速完成开发**。

**注意事项**  
支持的最大文件大小为 200 MB。`range` 参数必须为有效的 Excel 单元格区域地址（如 A1:B10）。对于非常大的工作表，处理时间可能延长。

## **如何使用 SDK 调用数学计算 API**

### **数学计算 API 规范**

[Math Calculate 规范](https://reference.aspose.cloud/cells/#/CalculateController/MathCalculate) 定义了一个公开可访问的编程接口，允许开发者直接通过 Web 浏览器与 API 交互。

### **使用 Aspose.Cells Cloud SDK**

使用 SDK 是开发速度最快的方案，因为它屏蔽了底层细节，仅需简短代码即可实现单元格级别的数学计算。  
请访问 [Aspose.Cells Cloud SDK GitHub 仓库](https://github.com/aspose-cells-cloud)，获取完整的 Aspose.Cells Cloud SDK 列表。

以下示例展示了如何使用不同语言的 SDK 调用 Aspose.Cells 云服务：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MathCalculate.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MathCalculate.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MathCalculate.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MathCalculate.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MathCalculate.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MathCalculate.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MathCalculate.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MathCalculate.go" >}}
{{</tab>}}
{{< /tabs >}}