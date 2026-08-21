---
title: "Aspose.Cells Cloud – 交换列、行和区域（v4.0）"
second_title: "文档"
ArticleTitle: "在 Excel 中交换列、行和单元格之间的数据"
linktype: "交换区域"
type: docs
url: /swap-range/
keywords: "Aspose Cells, Excel API, 交换区域, 云电子表格"
description: "使用 Aspose.Cells Cloud API 在 Excel 文件中交换列、行或区域。在单次请求中保留格式、公式和单元格引用。"
weight: 100
---

使用 Aspose.Cells Cloud API 自动交换 Excel 文件中任意两列、两行、两个区域或两个单元格之间的数据。交换区域 API 可在精确交换数据的同时保留所有格式、公式和单元格引用。它支持复杂数据重组、批量处理以及与企业工作流无缝集成的云功能。

## **交换区域 API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/swap/range
```

### **安全与身份验证**

Aspose.Cells Cloud API 具备安全性，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

```bash
-H "Authorization: Bearer {access_token}"
```

### **请求参数**

| 参数名称           | 类型   | 位置   | 描述                                                                                                                                     |
| ------------------ | ------ | ------ | ---------------------------------------------------------------------------------------------------------------------------------------- |
| **Spreadsheet**    | 文件   | FormData | **必填项。** 源 Excel 工作簿文件（`.xlsx`、`.xls`）。                                                                                  |
| **worksheet1**     | 字符串 | Query  | **必填项。** 包含第一个数据区域的工作表名称。                                                                                          |
| **range1**         | 字符串 | Query  | **必填项。** `worksheet1` 中待交换的单元格区域（例如 `A1:D10`）。                                                                      |
| **worksheet2**     | 字符串 | Query  | **必填项。** 包含第二个数据区域的工作表名称（可与 `worksheet1` 相同）。                                                                 |
| **range2**         | 字符串 | Query  | **必填项。** `worksheet2` 中待交换的单元格区域（例如 `F1:I10`）。**重要提示：** `range1` 与 `range2` 必须具有相同的维度。               |
| **outPath**        | 字符串 | Query  | **可选项。** 修改后的工作簿将保存到的云存储文件夹路径。                                                                                 |
| **outStorageName** | 字符串 | Query  | **必填项。** 已配置的云存储服务名称（例如 `MyCompanyStorage`）。                                                                        |
| **region**         | 字符串 | Query  | **可选项。** 区域设置（例如 `zh-CN`、`ja-JP`），可能影响格式化方式。                                                                    |
| **password**       | 字符串 | Query  | **可选项。** 解密受保护工作簿所需的密码。若文件未加密，请省略此项。                                                                     |

**示例请求（cURL）**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/swap/range?worksheet1=Sheet1&range1=A1:D10&worksheet2=Sheet2&range2=F1:I10&outStorageName=MyCompanyStorage" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@/path/to/workbook.xlsx"
```

### **响应**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**说明：**  
- API 将修改后的工作簿以文件流形式返回；若指定了 `outPath`，还会将文件保存至指定的云存储路径。  
- 若区域维度不匹配，将返回 **400 Bad Request（请求错误）** 错误。

### 错误码

| 代码                 | 描述                                               |
| -------------------- | -------------------------------------------------- |
| **400 Bad Request**  | 请求 URI 无效或区域维度不匹配。                    |
| **401 Unauthorized** | 访问令牌无效或已过期；client-id 或 secret 错误。   |
| **404 Not Found**    | 无法访问指定的工作簿文件。                         |
| **500 Server Error** | 处理工作簿时发生内部错误。                         |

## 何处应使用交换区域 API？

- **财务模型重构** – 重新组织数据块（例如将 Q3 预测移至 Q4），同时保留公式与条件格式。
- **数据管道与 ETL 流程** – 在最终输出前，将暂存工作表中的原始数据区域与清洗后的数据区域进行交换。
- **错误修正与数据恢复** – 快速纠正错位数据，避免手动复制粘贴。

## 为何使用交换区域 API？

- **开发者友好** – 提供多种语言的 SDK，相比自行开发可显著减少工作量。
- **降低人工成本** – 自动化数据重组操作，减少人工整合需求。
- **按使用量计费** – 仅对实际调用的 API 请求收费。
- **零维护负担** – 无需管理服务器，无软件更新，也无兼容性顾虑。

## 如何结合 SDK 使用交换区域 API

### 交换区域 API 规范

[交换区域 API 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Transform/SwapRange) 定义了公开可访问的编程接口，允许您直接从 Web 浏览器发起 REST 调用。

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是最快捷的开发方式，它屏蔽了底层细节，使您能以简洁代码完成区域交换。请访问 [GitHub 仓库](https://github.com/aspose-cells-cloud) 查看完整的 Aspose.Cells Cloud SDK 列表。

以下代码示例展示了如何使用多种语言的 SDK 调用 Aspose.Cells Web 服务：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SwapRange.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SwapRange.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SwapRange.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SwapRange.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SwapRange.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SwapRange.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SwapRange.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SwapRange.go" >}}
{{</tab>}}
{{< /tabs >}}