---
title: "将 Excel 区域转换为 CSV — Aspose.Cells Cloud API"
second_title: "文档"
ArticleTitle: "如何将本地电子表格的指定区域转换为 CSV 文件：分步指南"
linktitle: "将区域转换为 CSV"
type: docs
url: /convert-range-to-csv/
keywords: "Aspose Cells, 将区域转换为 CSV, Excel 转 CSV, Excel API, 云电子表格, 转换, Excel, CSV, Aspose.Cells, 云 API"
description: "了解如何使用 Aspose.Cells Cloud REST API 将本地 Excel 工作簿（XLSX 或 XLS）中的指定区域转换为 CSV。包含请求语法、参数、错误处理及 SDK 示例。"
---

使用 Aspose.Cells Cloud API 将本地 Excel 文件中的指定区域导出为 CSV。

## **将区域转换为 CSV API**

### **前置条件**
调用此接口前，您需要具备有效的 Aspose Cloud **客户端 ID** 和 **客户端密钥**，获取 **JWT 访问令牌**，并确保源电子表格为 **XLSX** 或 **XLS** 格式。

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/csv
```

**cURL 示例**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/range/csv?worksheet=Sheet1&range=A1:C10" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@sample.xlsx"
```

### **安全性与身份验证**

Aspose.Cells Cloud API 采用安全机制，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### **请求参数：**

| 参数名           | 类型   | 位置（路径 / 查询字符串 / HTTP 请求体） | 描述                                             |
| :--------------- | :----- | :--------------------------------------- | :----------------------------------------------- |
| Spreadsheet      | 文件   | FormData                                 | 上传电子表格文件。                               |
| worksheet        | 字符串 | 查询字符串                               | 电子表格的工作表名称。                           |
| range            | 字符串 | 查询字符串                               | 指定单元格区域（例如 A1:C10）。                  |
| outPath          | 字符串 | 查询字符串                               | 工作簿的存储路径（可选）。默认为 null。          |
| outStorageName   | 字符串 | 查询字符串                               | 输出存储空间名称。                               |
| fontsLocation    | 字符串 | 查询字符串                               | 如有需要，指定自定义字体路径。                   |
| region           | 字符串 | 查询字符串                               | 定义电子表格的区域设置。                         |
| password         | 字符串 | 查询字符串                               | 打开电子表格文件所需的密码。                     |

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

_返回的示例 CSV 内容（前几行）：_

```csv
Name,Date,Amount
John Doe,2023-01-15,1250.00
Jane Smith,2023-01-16,980.50
```

**HTTP 状态码**

| 状态码 | 含义           | 描述                                               |
| ------ | -------------- | -------------------------------------------------- |
| 200    | 成功           | 区域筛选成功；响应包含操作详情。                   |
| 400    | 请求错误       | 缺少或无效的参数（例如不支持的文件类型）。         |
| 401    | 未授权         | JWT 令牌无效或缺失。                               |
| 413    | 请求实体过大   | 上传的文件超出大小限制。                           |
| 500    | 内部服务器错误 | 服务器发生意外错误。                               |

## 何处应使用将区域转换为 CSV API？

### **1. 数据导出与迁移场景**

- **数据库集成**：将指定 Excel 区域直接导出至数据库系统。
- **应用程序集成**：将选定的电子表格数据导入 SaaS 应用程序。
- **系统迁移**：在旧系统与现代系统之间迁移指定数据区域。
- **跨平台共享**：在不同平台间共享特定数据子集。

### **2. 报表与分析**

- **定向报表**：将特定报表部分导出为 CSV，以便深入分析。
- **仪表板数据源**：向商业智能（BI）仪表板工具提供指定数据区域。
- **绩效指标**：提取关键绩效指标（KPI）区域，供绩效追踪系统使用。
- **财务报表**：导出财务报表部分，用于外部审计。

### **3. 开发与测试**

- **测试数据管理**：导出指定数据区域用于测试目的。
- **开发环境**：向开发团队共享示例数据区域。
- **API 测试**：从指定电子表格区域生成 CSV 测试数据。
- **原型开发**：为应用程序原型提供特定数据集。

### **4. 业务运营**

- **选择性数据共享**：向外部合作伙伴共享指定数据区域。
- **部分数据备份**：以 CSV 格式备份关键数据区域。
- **部门间数据传输**：在各部门之间共享指定数据。
- **合规性报告**：导出合规性监管所需的数据区域。

### **5. 自动化工作流**

- **定时区域导出**：按计划自动导出指定区域。
- **触发式数据提取**：基于业务事件或触发条件导出区域。
- **工作流集成**：将区域导出集成至业务流程工作流中。
- **批量区域处理**：批量处理多个指定区域。

## 为何应使用将区域转换为 CSV API？

- 可直接转换电子表格区域，无需先上传整个工作簿，节省存储空间并降低费用。
- 可借助现有的 Aspose.Cells Cloud SDK 快速完成开发。
- **简单集成**：提供 REST API 及清晰文档。
- **可扩展架构**：支持从小型到企业级的各种规模操作。

## 如何结合 SDK 使用将区域转换为 CSV API？

### OpenAPI 规范

[OpenAPI 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToCSV) 定义了一个公开可访问的 API，允许直接从网页浏览器发起 REST 请求。

## 使用 Aspose.Cells Cloud SDK

使用 SDK 是最快捷的开发方式，它抽象了底层细节，使您能以极简代码将数据区域转换为 CSV 文件。  
请访问我们的 [GitHub 仓库](https://github.com/aspose-cells-cloud)，查看完整的 Aspose.Cells Cloud SDK 列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务。若 Gist 加载被屏蔽，您可直接从仓库下载示例。

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToCSV.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToCSV.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToCSV.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToCSV.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToCSV.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToCSV.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToCSV.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToCSV.go" >}}
{{</tab>}}
{{< /tabs >}}

---