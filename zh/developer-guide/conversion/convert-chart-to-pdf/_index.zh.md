---
title: "Aspose.Cells Cloud API – 将 Excel 图表转换为 PDF"
second_title: "文档"
ArticleTitle: "如何将本地电子表格中的图表转换为 PDF 文件：分步指南"
linktype: "Convert Chart to PDF"
type: docs
url: /zh/convert-chart-to-pdf/
keywords: "Aspose Cells, 图表, PDF, Excel, 转换, 云 API"
description: "使用 Aspose.Cells Cloud REST API 将本地 Excel 文件中的图表导出为 PDF 格式。支持 XLSX 和 XLS 文件。"
weight: 100
---

使用云 API 将本地 Excel 文件中的图表导出为 [PDF](https://docs.fileformat.com/pdf/) 格式。

## **将图表转换为 PDF 的 Web API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/chart/pdf
```

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### **请求参数：**

| 参数名称         | 类型     | 路径/查询字符串/HTTP 请求体 | 描述                                                    |
| ---------------- | -------- | --------------------------- | ------------------------------------------------------- |
| Spreadsheet      | 文件     | FormData                    | 上传电子表格文件。                                      |
| worksheet        | 字符串   | 查询字符串                  | 包含目标图表的工作表名称。                              |
| chartIndex       | 整数     | 查询字符串                  | 要转换的图表索引。                                      |
| outPath          | 字符串   | 查询字符串                  | （可选）已转换文件的存储路径，默认为 null。             |
| outStorageName   | 字符串   | 查询字符串                  | 输出文件的存储名称。                                    |
| fontsLocation    | 字符串   | 查询字符串                  | 如有需要，指定自定义字体路径。                          |
| region           | 字符串   | 查询字符串                  | 电子表格的区域设置。                                    |
| password         | 字符串   | 查询字符串                  | 打开电子表格文件所需的密码。                            |

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

**HTTP 状态码**

| 状态码 | 含义                 | 描述                                     |
| ------ | -------------------- | ---------------------------------------- |
| 200    | 成功 (OK)            | 操作成功执行；响应包含操作详情。         |
| 400    | 请求错误 (Bad Request) | 缺少或参数无效（例如文件类型不支持）。   |
| 401    | 未授权 (Unauthorized) | JWT 令牌无效或缺失。                     |
| 413    | 请求实体过大 (Payload Too Large) | 上传文件超出大小限制。               |
| 500    | 内部服务器错误 (Internal Server Error) | 服务器发生意外错误。                 |

## 在哪些场景下应使用将图表转换为 PDF 的 API？

### **1. 商业报告与自动化**

- **财务部门**：月度财务报表图表 → PDF 归档
- **销售团队**：业绩趋势图表 → PDF 客户报告
- **市场分析**：活动效果图表 → PDF 高管简报
- **运营管理**：生产监控图表 → PDF 合规文档

### **2. 软件开发与集成**

- **SaaS 应用程序**：用户生成的图表数据 → 可下载的 PDF 报告
- **企业系统**：ERP/CRM 系统图表 → PDF 审计文档
- **移动应用**：应用内分析图表 → 可分享的 PDF 文件
- **Web 应用程序**：仪表盘图表 → PDF 导出功能

### **3. 文档处理工作流**

- **批处理**：同时将多个 Excel 文件中的图表转换为 PDF
- **定时任务**：自动每日/每周生成图表报告
- **模板化输出**：标准图表格式 → PDF 文档
- **文档组装**：将图表与其他内容合并为 PDF 文档

### **4. 行业特定应用场景**

- **科研机构**：实验数据图表 → PDF 论文插图
- **教育领域**：教材图表 → PDF 课程资料
- **咨询公司**：分析图表 → PDF 客户交付成果
- **制造业**：质量控制图表 → PDF 检验报告
- **医疗保健**：患者数据图表 → PDF 医疗记录
- **政府机构**：统计数据图表 → PDF 官方出版物

### **5. 内容管理与分发**

- **数字资产管理**：以标准化 PDF 格式归档图表
- **知识库**：嵌入图表 PDF 的技术文档
- **客户门户**：向利益相关者安全交付 PDF 报告
- **法规合规**：生成符合审计要求的 PDF 文档

## 为何应使用将图表转换为 PDF 的 API？

- 可在**无需预先上传工作簿**的前提下转换图表，节省存储空间并降低成本。
- 可通过现有的 Aspose.Cells Cloud SDK 快速完成开发。
- **集成简单**：REST API 提供清晰文档。
- **可扩展架构**：支持从小型到企业级的各种工作负载。

## 如何使用 SDK 调用将图表转换为 PDF 的 API？

### 将图表转换为 PDF 的 API 规范

[将图表转换为 PDF API 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertChartToPDF) 定义了一个公开可访问的编程接口，使您能够直接从 Web 浏览器发起 REST 请求。

## 使用 Aspose.Cells Cloud SDK

使用 SDK 是最快捷的开发方式，它屏蔽了底层细节，仅需少量代码即可将图表转换为 PDF 文件。  
以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertChartToPDF.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertChartToPDF.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertChartToPDF.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertChartToPDF.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertChartToPDF.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertChartToPDF.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertChartToPDF.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertChartToPDF.go" >}}
{{</tab>}}
{{< /tabs >}}